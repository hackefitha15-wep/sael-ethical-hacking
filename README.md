```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SA EL CYBER | منصة الأمن السيبراني التعليمية</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family:Tahoma,Arial,sans-serif;
    background:#05080d;
    color:#fff;
    line-height:1.8;
}

header{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:30px;
    background:
        radial-gradient(circle at top,#12352d 0,#05080d 45%);
}

.hero{
    max-width:850px;
}

.logo{
    font-size:55px;
    font-weight:bold;
    color:#00ff9d;
    letter-spacing:2px;
    text-shadow:0 0 25px #00ff9d55;
}

.hero h2{
    margin-top:15px;
    font-size:28px;
}

.hero p{
    margin:20px auto;
    color:#b9c4c8;
    max-width:650px;
    font-size:18px;
}

.btn{
    display:inline-block;
    margin-top:20px;
    padding:13px 25px;
    background:#00b878;
    color:white;
    border-radius:10px;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.btn:hover{
    background:#00e89a;
    transform:translateY(-3px);
}

section{
    padding:70px 20px;
    max-width:1150px;
    margin:auto;
}

.title{
    text-align:center;
    margin-bottom:45px;
}

.title h2{
    color:#00ff9d;
    font-size:32px;
}

.title p{
    color:#8e9ba0;
    margin-top:10px;
}

.cards{
    display:grid;
    grid-template-columns:
        repeat(auto-fit,minmax(280px,1fr));
    gap:22px;
}

.card{
    background:#0c1218;
    border:1px solid #1d3036;
    border-radius:18px;
    padding:28px;
    transition:.3s;
}

.card:hover{
    transform:translateY(-7px);
    border-color:#00c982;
    box-shadow:0 10px 35px #00ff9d12;
}

.icon{
    font-size:42px;
    margin-bottom:15px;
}

.card h3{
    color:#00e890;
    margin-bottom:12px;
    font-size:23px;
}

.card p{
    color:#b8c1c5;
}

.learning{
    background:#091016;
    border-top:1px solid #16252b;
    border-bottom:1px solid #16252b;
}

.steps{
    display:grid;
    grid-template-columns:
        repeat(auto-fit,minmax(220px,1fr));
    gap:15px;
}

.step{
    padding:22px;
    background:#0e171d;
    border-radius:14px;
    border:1px solid #1c2d33;
}

.step span{
    display:block;
    font-size:28px;
    color:#00ff9d;
    font-weight:bold;
}

.warning{
    margin-top:35px;
    padding:20px;
    background:#211d0d;
    border:1px solid #66551e;
    border-radius:14px;
    color:#e4d794;
}

footer{
    text-align:center;
    padding:35px 20px;
    color:#68757a;
    border-top:1px solid #17242a;
}

footer strong{
    color:#00d889;
}

@media(max-width:600px){
    .logo{
        font-size:38px;
    }

    .hero h2{
        font-size:22px;
    }

    .hero p{
        font-size:16px;
    }
}
</style>
</head>

<body>

<header>

<div class="hero">

<div class="logo">
🛡️ SA EL CYBER
</div>

<h2>
منصة الأمن السيبراني التعليمية
</h2>

<p>
تعلّم أساسيات الأمن السيبراني، حماية الشبكات،
أمان تطبيقات الويب، والوعي بالمخاطر الرقمية
بطريقة تعليمية ومسؤولة.
</p>

<a href="#courses" class="btn">
ابدأ التعلم 🚀
</a>

</div>

</header>


<section id="courses">

<div class="title">

<h2>مجالات التعلم</h2>

<p>
استكشف أهم أساسيات الأمن السيبراني
</p>

</div>


<div class="cards">


<div class="card">

<div class="icon">
🌐
</div>

<h3>
أمن الشبكات
</h3>

<p>
تعرّف على كيفية حماية الشبكات،
فهم البروتوكولات، اكتشاف المشكلات
الأمنية، وكيفية اختبار الأنظمة
داخل بيئات تملك تصريحًا لاختبارها.
</p>

</div>


<div class="card">

<div class="icon">
🔐
</div>

<h3>
أمان الويب
</h3>

<p>
افهم نقاط الضعف الشائعة في تطبيقات
الويب، وكيف يمكن للمطورين اكتشافها
والوقاية منها وبناء مواقع أكثر أمانًا.
</p>

</div>


<div class="card">

<div class="icon">
🧠
</div>

<h3>
الوعي السيبراني
</h3>

<p>
تعلّم كيفية الحفاظ على سلامتك على
الإنترنت، حماية حساباتك، إنشاء كلمات
مرور قوية، والتعامل مع رسائل التصيد.
</p>

</div>


<div class="card">

<div class="icon">
🐧
</div>

<h3>
Kali Linux
</h3>

<p>
تعرّف على بيئة Kali Linux وأدواتها
المستخدمة في التعلم واختبار الأمن
داخل المختبرات والأنظمة المصرح بها.
</p>

</div>


<div class="card">

<div class="icon">
🔎
</div>

<h3>
جمع المعلومات
</h3>

<p>
تعلم أساسيات OSINT وكيفية جمع
المعلومات المتاحة للعامة وتحليلها
بشكل قانوني ومسؤول.
</p>

</div>


<div class="card">

<div class="icon">
💻
</div>

<h3>
Linux Terminal
</h3>

<p>
ابدأ بتعلم أوامر Linux الأساسية
والتعامل مع الملفات والمجلدات
والشبكات من خلال الطرفية.
</p>

</div>

</div>

</section>


<section class="learning">

<div class="title">

<h2>
خطة التعلم
</h2>

<p>
ابدأ من الأساسيات وتقدم خطوة بخطوة
</p>

</div>


<div class="steps">

<div class="step">
<span>01</span>
أساسيات الإنترنت والشبكات
</div>

<div class="step">
<span>02</span>
أساسيات Linux
</div>

<div class="step">
<span>03</span>
مبادئ الأمن السيبراني
</div>

<div class="step">
<span>04</span>
أمن تطبيقات الويب
</div>

<div class="step">
<span>05</span>
الاختبار داخل مختبرات آمنة
</div>

<div class="step">
<span>06</span>
الحماية والتحليل
</div>

</div>


<div class="warning">

⚠️ <strong>الاستخدام المسؤول:</strong>

جميع المعلومات والأدوات الموجودة في المنصة
مخصصة للتعلم والأبحاث الأمنية واختبار الأنظمة
التي تملكها أو لديك تصريح باختبارها.
لا تستخدم المعلومات للوصول غير المصرح به
إلى حسابات أو أجهزة أو شبكات الآخرين.

</div>

</section>


<footer>

<p>
<strong>SA EL CYBER</strong>
</p>

<p>
منصة تعليمية للأمن السيبراني © 2026
</p>

</footer>


</body>
</html>
```
