# 🌐 Work-case 8: Робота в терміналі Linux без графічної оболонки та використання консольних утиліт  
**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис

---

## 1. Робота з сервісними та обмеженими системами через CLI

У ситуаціях, коли графічна оболонка (GUI) вимкнена для економії ресурсів або безпеки, термінал Linux надає повний спектр інструментів для виконання будь-яких задач.

### Перегляд файлів та папок
* **Інструмент:** `mc` (Midnight Commander)
* **Пояснення:** Це потужний двопанельний файловий менеджер. Він дозволяє зручно навігувати по файловій системі, копіювати, переміщувати та редагувати файли за допомогою гарячих клавіш (F3-F8).
* **Команда:** `mc`

> <a href="https://ibb.co/LDJQRDHs"><img src="https://i.ibb.co/Xf3yLfMG/image.png" alt="image" border="0"></a>

### Веб-серфінг у терміналі
* **Інструмент:** `lynx` (або `links2`)
* **Пояснення:** Текстовий браузер, який рендерить контент сайтів без зображень та скриптів. Це ідеально для читання документації або пошуку інформації на слабких каналах зв'язку.
* **Команда:** `lynx https://google.com`

> <a href="https://ibb.co/BVzrCvWD"><img src="https://i.ibb.co/27nskRV2/image.png" alt="image" border="0"></a>

### Електронна пошта
* **Інструмент:** `mutt`
* **Пояснення:** Гнучкий поштовий клієнт (MUA), який підтримує MIME, GPG, поштові скриньки у форматах Maildir та mbox.
* **Команда:** `mutt`
> <a href="https://ibb.co/hRY8WDLS"><img src="https://i.ibb.co/JR3k75m9/image.png" alt="image" border="0"></a>
### Прослуховування музики
* **Інструмент:** `cmus` (C* Music Player)
* **Пояснення:** Легкий та швидкий аудіоплеєр з підтримкою бібліотек, фільтрів та плейлистів.
* **Команда:** `cmus`

> <a href="https://ibb.co/S7Q2M6XT"><img src="https://i.ibb.co/tPZSvHMf/image.png" alt="image" border="0"></a>

### Скачування торентів
* **Інструмент:** `transmission-cli`
* **Пояснення:** Клієнт BitTorrent, написаний на C++, що фокусується на високій продуктивності та стабільності.
* **Команда:** `transmission-cli`

> <a href="https://ibb.co/BKYxzf7Y"><img src="https://i.ibb.co/S7Z8s61Z/image.png" alt="image" border="0"></a>

### Календар та планувальник
* **Інструмент:** `calcurse`
* **Пояснення:** Текстова утиліта для керування особистим розкладом. Вона поєднує в собі календар, список справ та систему сповіщень.
* **Команда:** `calcurse`
> <a href="https://ibb.co/20ksz2GG"><img src="https://i.ibb.co/8n7dy311/image.png" alt="image" border="0"></a>
### Перегляд зображень
* **Інструмент:** `cacaview` (пакет `caca-utils`)
* **Пояснення:** Програма відображає графічні файли в терміналі, конвертуючи їх у ASCII-арт.
* **Команда:** `cacaview image.jpg`

> <a href="https://ibb.co/3Y704kfD"><img src="https://i.ibb.co/PzN5FtT7/image.png" alt="image" border="0"></a>

---

## 2. Класичні дії системного адміністратора

Нижче наведено основні інструменти для роботи з текстом та моніторингу системи.

* **Редагування тексту:** `vim` (або `nano`).
    * **Опис:** `vim` — це стандарт де-факто для професійних адміністраторів. Він дозволяє редагувати конфігураційні файли з величезною швидкістю завдяки режимам роботи та гарячим клавішам.
    * **Команда:** `vi mayhem.conf`
> <a href="https://ibb.co/hFQrG0Qm"><img src="https://i.ibb.co/HTwRcZwH/image.png" alt="image" border="0"></a>

* **Моніторинг процесів:** `htop`.
    * **Опис:** Аналог "Диспетчера завдань". Показує завантаження кожного ядра процесора, використання оперативної пам'яті (RAM), Swap та список процесів з можливістю їх сортування та миттєвого завершення (kill).
    * **Команда:** `htop`
> <a href="https://ibb.co/7tMTPvWH"><img src="https://i.ibb.co/xq9cWhjy/image.png" alt="image" border="0"></a>
---

## 3. «Пасхалки» та інтерактив для настрою

Linux має багато вбудованих жартів, які допомагають трохи відпочити під час роботи.

* **Подорож (Паровоз):** Команда `sl` (Steam Locomotive). Якщо ви випадково вводите `sl` замість `ls`, через весь термінал проїде анімований паровоз.
    * *Встановлення:* `sudo apt install sl`
> <a href="https://ibb.co/C5RqgpQS"><img src="https://i.ibb.co/Z6q35Rxb/image.png" alt="image" border="0"></a>
* **Pacman:** Граємо в того самого Pacman.
    * *Команда:* `pacman`
>  <a href="https://ibb.co/7tdTQkJg"><img src="https://i.ibb.co/VYchxwWH/image.png" alt="image" border="0"></a>
* **Діалог з коровою:** Команда `cowsay`. Корова "виголошує" будь-який ваш текст.
    * *Команда:* `cowsay "IN THE AIR TONIGHT!"`
>  <a href="https://imgbb.com/"><img src="https://i.ibb.co/tMCYyzLT/image.png" alt="зображення" border="0"></a>
* **"Матриця":** Утиліта `cmatrix`. Створює ефект падаючого зеленого коду, як у однойменному фільмі.
    * *Команда:* `cmatrix`
>  <a href="https://ibb.co/JWcVsxHt"><img src="https://i.ibb.co/9mp6rwWg/image.png" alt="image" border="0"></a>
---

## Висновок / Conclusion
У ході виконання даної роботи було досліджено можливості термінала Linux як повноцінного робочого середовища. Було встановлено, що відсутність графічної оболонки (GUI) не обмежує функціональність системи, а навпаки — дозволяє значно економити системні ресурси та підвищує ефективність адміністрування. Отримані навички роботи з текстовими браузерами, файловими менеджерами та системними моніторами є критично важливими для роботи з серверами та вбудованими системами.

During this practical work, the Linux terminal's capabilities were explored as a fully functional working environment. It was established that the absence of a Graphical User Interface (GUI) does not restrict system functionality; instead, it allows for significant savings in system resources and enhances administrative efficiency. The skills acquired in operating text-based browsers, file managers, and system monitors are critically important for managing servers and embedded systems.
