```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Kali Cyber Guide - Sabry</title>

<style>
*{box-sizing:border-box}
body{
    margin:0;
    font-family:Arial,Tahoma,sans-serif;
    background:#080b10;
    color:#eee;
}
header{
    padding:25px 15px;
    text-align:center;
    background:linear-gradient(135deg,#101820,#18252f);
    border-bottom:1px solid #26343d;
}
header h1{
    margin:0 0 8px;
    color:#00ff9d;
}
header p{color:#aaa}

.container{
    max-width:1100px;
    margin:auto;
    padding:20px;
}

.search{
    width:100%;
    padding:15px;
    border-radius:12px;
    border:1px solid #34434d;
    background:#11171d;
    color:white;
    font-size:17px;
    outline:none;
}

.categories{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
    margin:15px 0;
}

.categories button{
    background:#121a20;
    color:#ddd;
    border:1px solid #34434d;
    padding:10px 14px;
    border-radius:10px;
    cursor:pointer;
}

.categories button:hover,
.categories button.active{
    background:#00a66a;
    color:#fff;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:15px;
}

.card{
    background:#10161b;
    border:1px solid #26343d;
    border-radius:15px;
    padding:18px;
    transition:.2s;
}

.card:hover{
    transform:translateY(-3px);
    border-color:#00b878;
}

.card h2{
    margin-top:0;
    color:#00e890;
    font-size:20px;
}

.tag{
    display:inline-block;
    font-size:12px;
    background:#17252c;
    color:#6fffc2;
    padding:5px 8px;
    border-radius:7px;
    margin-bottom:10px;
}

.desc{
    color:#bbb;
    line-height:1.7;
}

code{
    display:block;
    direction:ltr;
    text-align:left;
    background:#05080a;
    border:1px solid #202b31;
    padding:12px;
    border-radius:9px;
    color:#8cffd1;
    overflow:auto;
    margin-top:10px;
}

.copy{
    margin-top:8px;
    background:#00a66a;
    color:white;
    border:0;
    padding:8px 12px;
    border-radius:8px;
    cursor:pointer;
}

.copy:hover{background:#00c982}

.warning{
    margin:20px 0;
    padding:15px;
    background:#241e0d;
    border:1px solid #66531d;
    border-radius:12px;
    color:#e8d58b;
    line-height:1.7;
}

footer{
    text-align:center;
    padding:25px;
    color:#777;
}
</style>
</head>

<body>

<header>
    <h1>🛡️ Kali Cyber Guide</h1>
    <p>دليل تعليمي لأوامر وأدوات الأمن السيبراني — Sabry</p>
</header>

<div class="container">

<input
    id="search"
    class="search"
    placeholder="🔎 ابحث عن أداة أو أمر..."
>

<div class="categories">
    <button class="active" onclick="filterCategory('all',this)">الكل</button>
    <button onclick="filterCategory('linux',this)">Linux</button>
    <button onclick="filterCategory('network',this)">الشبكات</button>
    <button onclick="filterCategory('web',this)">الويب</button>
    <button onclick="filterCategory('dns',this)">DNS</button>
    <button onclick="filterCategory('security',this)">الأمن</button>
    <button onclick="filterCategory('forensics',this)">Forensics</button>
</div>

<div class="warning">
<b>⚠️ تنبيه:</b>
استخدم الأوامر فقط على جهازك أو شبكة أو مختبر لديك تصريح باختباره.
هذا الموقع مخصص للتعلم وفهم أدوات Kali Linux.
</div>

<div id="tools" class="grid"></div>

</div>

<footer>
    Kali Cyber Guide © 2026 — Sabry
</footer>

<script>

const tools = [

{
name:"pwd",
category:"linux",
tag:"Linux",
desc:"عرض المسار الحالي داخل الطرفية.",
cmd:"pwd"
},

{
name:"ls",
category:"linux",
tag:"Linux",
desc:"عرض الملفات والمجلدات الموجودة.",
cmd:"ls -la"
},

{
name:"cd",
category:"linux",
tag:"Linux",
desc:"الانتقال إلى مجلد آخر.",
cmd:"cd /home/kali"
},

{
name:"mkdir",
category:"linux",
tag:"Linux",
desc:"إنشاء مجلد جديد.",
cmd:"mkdir lab"
},

{
name:"cp",
category:"linux",
tag:"Linux",
desc:"نسخ ملف أو مجلد.",
cmd:"cp file.txt backup.txt"
},

{
name:"mv",
category:"linux",
tag:"Linux",
desc:"نقل أو إعادة تسمية ملف.",
cmd:"mv old.txt new.txt"
},

{
name:"grep",
category:"linux",
tag:"Linux",
desc:"البحث عن نص داخل الملفات أو المخرجات.",
cmd:"grep \"error\" log.txt"
},

{
name:"find",
category:"linux",
tag:"Linux",
desc:"البحث عن ملفات داخل النظام.",
cmd:"find . -name \"*.txt\""
},

{
name:"ip",
category:"network",
tag:"Network",
desc:"عرض معلومات واجهات الشبكة وعناوين IP الخاصة بجهازك.",
cmd:"ip addr"
},

{
name:"ss",
category:"network",
tag:"Network",
desc:"عرض اتصالات الشبكة والمنافذ المحلية.",
cmd:"ss -tuln"
},

{
name:"ping",
category:"network",
tag:"Network",
desc:"اختبار الاتصال بعنوان أو جهاز تملكه أو لديك تصريح لاختباره.",
cmd:"ping 127.0.0.1"
},

{
name:"traceroute",
category:"network",
tag:"Network",
desc:"عرض المسار الشبكي إلى وجهة.",
cmd:"traceroute example.com"
},

{
name:"curl",
category:"web",
tag:"Web",
desc:"إرسال طلب HTTP وعرض الاستجابة.",
cmd:"curl https://example.com"
},

{
name:"wget",
category:"web",
tag:"Web",
desc:"جلب ملف أو صفحة من الإنترنت.",
cmd:"wget https://example.com/file.txt"
},

{
name:"whatweb",
category:"web",
tag:"Web",
desc:"التعرف على تقنيات موقع ويب تملكه أو تختبره بتصريح.",
cmd:"whatweb https://example.com"
},

{
name:"nmap",
category:"network",
tag:"Network Security",
desc:"استكشاف الخدمات والمنافذ في مختبر أو نظام مصرح لك بفحصه.",
cmd:"nmap 127.0.0.1"
},

{
name:"whois",
category:"dns",
tag:"DNS / OSINT",
desc:"عرض معلومات WHOIS المتاحة عن نطاق.",
cmd:"whois example.com"
},

{
name:"dig",
category:"dns",
tag:"DNS",
desc:"الاستعلام عن سجلات DNS.",
cmd:"dig example.com"
},

{
name:"nslookup",
category:"dns",
tag:"DNS",
desc:"الاستعلام عن معلومات DNS.",
cmd:"nslookup example.com"
},

{
name:"openssl",
category:"security",
tag:"Security",
desc:"أداة للعمل مع الشهادات والتشفير وTLS.",
cmd:"openssl version"
},

{
name:"sha256sum",
category:"security",
tag:"Security",
desc:"حساب SHA-256 لملف للتحقق من سلامته.",
cmd:"sha256sum file.iso"
},

{
name:"file",
category:"forensics",
tag:"Forensics",
desc:"التعرف على نوع الملف.",
cmd:"file suspicious.bin"
},

{
name:"strings",
category:"forensics",
tag:"Forensics",
desc:"استخراج السلاسل النصية المقروءة من ملف.",
cmd:"strings sample.bin"
},

{
name:"xxd",
category:"forensics",
tag:"Forensics",
desc:"عرض محتوى الملف بصيغة hexadecimal.",
cmd:"xxd sample.bin"
},

{
name:"hexdump",
category:"forensics",
tag:"Forensics",
desc:"عرض البيانات بصيغة hexadecimal للتحليل.",
cmd:"hexdump -C sample.bin"
},

{
name:"tcpdump",
category:"network",
tag:"Network",
desc:"التقاط وتحليل حركة الشبكة في مختبرك.",
cmd:"sudo tcpdump -i lo"
},

{
name:"git",
category:"linux",
tag:"Development",
desc:"إدارة مشاريع Git.",
cmd:"git status"
},

{
name:"python3",
category:"linux",
tag:"Programming",
desc:"تشغيل Python على Kali.",
cmd:"python3 --version"
},

{
name:"man",
category:"linux",
tag:"Help",
desc:"قراءة دليل استخدام أمر.",
cmd:"man nmap"
},

{
name:"help",
category:"linux",
tag:"Help",
desc:"عرض المساعدة الخاصة بالأمر.",
cmd:"nmap --help"
}

];

const toolsBox = document.getElementById("tools");
const search = document.getElementById("search");

let currentCategory = "all";

function render(){

    const query = search.value.toLowerCase().trim();

    const result = tools.filter(t => {

        const categoryOK =
            currentCategory === "all" ||
            t.category === currentCategory;

        const text =
            (t.name + " " + t.tag + " " + t.desc + " " + t.cmd)
            .toLowerCase();

        return categoryOK && text.includes(query);
    });

    toolsBox.innerHTML = "";

    if(result.length === 0){
        toolsBox.innerHTML =
        "<p>❌ لا توجد نتائج.</p>";
        return;
    }

    result.forEach(t => {

        const card = document.createElement("div");
        card.className = "card";

        card.innerHTML = `
            <span class="tag">${t.tag}</span>
            <h2>${t.name}</h2>
            <div class="desc">${t.desc}</div>
            <code>${escapeHTML(t.cmd)}</code>
            <button class="copy"
                onclick="copyCommand(${JSON.stringify(t.cmd)})">
                📋 نسخ الأمر
            </button>
        `;

        toolsBox.appendChild(card);
    });
}

function escapeHTML(text){
    return text
        .replaceAll("&","&amp;")
        .replaceAll("<","&lt;")
        .replaceAll(">","&gt;");
}

function copyCommand(command){

    navigator.clipboard.writeText(command)
    .then(() => alert("✅ تم نسخ الأمر"));
}

function filterCategory(category,button){

    currentCategory = category;

    document
    .querySelectorAll(".categories button")
    .forEach(b => b.classList.remove("active"));

    button.classList.add("active");

    render();
}

search.addEventListener("input",render);

render();

</script>

</body>
</html>
```
