# **Emmet abbreviations** 
 طريقة مختصرة وسحرية لكتابة **HTML (وأحيانًا CSS)** بسرعة داخل أي محرر حديث
زي VS Code, WebStorm, Sublime Text … إلخ.

---

## ⚡️ أشهر اختصارات Emmet في HTML:

### 🧱 التكرار (Multiplication)

```html
div*3
```

🔹 ينشئ 3 عناصر `<div>`:

```html
<div></div>
<div></div>
<div></div>
```

---

### 🧩 إضافة كلاس

```html
div.card
```

🔹 ينشئ:

```html
<div class="card"></div>
```

---

### 🆔 إضافة ID

```html
div#header
```

🔹 ينشئ:

```html
<div id="header"></div>
```

---

### 🧱 تكرار مع كلاس متغير

```html
div.item$*3
```

🔹 ينشئ:

```html
<div class="item1"></div>
<div class="item2"></div>
<div class="item3"></div>
```

---

### 🪜 التداخل (Nesting)

```html
ul>li*3
```

🔹 ينشئ:

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

---

### 🧱 أخوة العناصر (Siblings)

```html
header+main+footer
```

🔹 ينشئ:

```html
<header></header>
<main></main>
<footer></footer>
```

---

### 🧬 النص داخل العنصر

```html
p{Hello World}
```

🔹 ينشئ:

```html
<p>Hello World</p>
```

---

### 🧭 الدمج بين كل دا 😎

```html
ul>li.item$*3>a{Link $}
```

🔹 النتيجة:

```html
<ul>
  <li class="item1"><a>Link 1</a></li>
  <li class="item2"><a>Link 2</a></li>
  <li class="item3"><a>Link 3</a></li>
</ul>
```

---

### 🧱 مع الـ attributes

```html
input[type="text" placeholder="Enter name"]
```

🔹 ينشئ:

```html
<input type="text" placeholder="Enter name">
```

---

### 💡 ملاحظات سريعة:

* VS Code بيفعل Emmet **تلقائيًا** في ملفات `.html`, `.css`, `.jsx`, `.tsx`
* تقدر تفعله يدويًا من الإعدادات لو مش شغال.
* لو كتبت اختصار واضغطت:

  ```
  Tab
  ```

  أو

  ```
  Ctrl + E
  ```

  بيتوسع تلقائيًا إلى الكود الكامل.

---

 فعلاً Emmet مش بس “اختصارات”، دي طريقة **تضاعف إنتاجيتك 3x–5x** وانت بتكتب HTML.
خليني أوريك **أمثلة قوية** بتوضح الإيمباكت الحقيقي 👇

---

## ⚡️ أمثلة Emmet قوية فعلاً (بتوفر وقت رهيب)

### 🧱 1. إنشاء هيكل صفحة أساسي في ثانية واحدة

```emmet
html:5
```

🔹 النتيجة:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

⏱️ بدل ما تكتب 10 أسطر يدويًا.

---

### 🧩 2. Navbar جاهز في سطر واحد

```emmet
nav>ul>li*4>a[href="#"]{Link $}
```

🔹 النتيجة:

```html
<nav>
  <ul>
    <li><a href="#">Link 1</a></li>
    <li><a href="#">Link 2</a></li>
    <li><a href="#">Link 3</a></li>
    <li><a href="#">Link 4</a></li>
  </ul>
</nav>
```

⏱️ 1 ثانية بدل من 12–15 سطر كتابة يدوية.

---

### 🧠 3. Card Component جاهز

```emmet
div.card*3>img[src="img$.jpg" alt="Image $"]+h2{Title $}+p{This is card $ description}+button{Read More}
```

🔹 النتيجة:

```html
<div class="card">
  <img src="img1.jpg" alt="Image 1">
  <h2>Title 1</h2>
  <p>This is card 1 description</p>
  <button>Read More</button>
</div>
<div class="card">
  <img src="img2.jpg" alt="Image 2">
  <h2>Title 2</h2>
  <p>This is card 2 description</p>
  <button>Read More</button>
</div>
<div class="card">
  <img src="img3.jpg" alt="Image 3">
  <h2>Title 3</h2>
  <p>This is card 3 description</p>
  <button>Read More</button>
</div>
```

⏱️ وفّرت كتابة **15–20 سطر** يدوي.

---

### 💬 4. نموذج (Form) كامل في لحظة

```emmet
form>label[for="name"]{Name:}+input#name[type="text" required]+br+label[for="email"]{Email:}+input#email[type="email" required]+br+button[type="submit"]{Send}
```

🔹 النتيجة:

```html
<form>
  <label for="name">Name:</label>
  <input id="name" type="text" required>
  <br>
  <label for="email">Email:</label>
  <input id="email" type="email" required>
  <br>
  <button type="submit">Send</button>
</form>
```

⏱️ كتابة 12 سطر في 3 ثواني فقط.

---

### 🧬 5. صفحة Blog Section كاملة

```emmet
section.blog>article.post*3>h2{Post $}+p{Lorem ipsum dolor sit amet, consectetur adipiscing elit.}+a[href="#"]{Read more}
```

🔹 النتيجة:

```html
<section class="blog">
  <article class="post">
    <h2>Post 1</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <a href="#">Read more</a>
  </article>
  <article class="post">
    <h2>Post 2</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <a href="#">Read more</a>
  </article>
  <article class="post">
    <h2>Post 3</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <a href="#">Read more</a>
  </article>
</section>
```

⏱️ أكثر من **25 سطر** في ثانية واحدة 😎

---

### 💡 6. Footer منظم بسرعة

```emmet
footer>ul>li*3>a[href="#"]{Footer Link $}+p{© 2025 Gemax}
```

---

### 🧠 ملاحظة استراتيجية

لو بتشتغل على مشاريع Front-end زي PureLearn:

* استخدم Emmet في إنشاء **الهيكل الأساسي (HTML skeleton)**.
* بعدين ركّز على الـ CSS/JS والتصميم.
* بيخليك تدخل في المرحلة “الإبداعية” أسرع بدل ما تضيع وقت في boilerplate code.

---

هل تحب أجهزلك **cheat sheet بصري** لأهم اختصارات Emmet (بالعربي + الكود الجاهز)، يكون ملف HTML صغير تتدرب عليه؟
