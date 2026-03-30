# 🌐 Work-case 6: Командні інтерпретатори
**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис

---
## Glossary of Terms (Словник термінів)
* **Shell (Командна оболонка / Інтерпретатор):** Програма, що забезпечує інтерфейс для взаємодії користувача з операційною системою.
* **Command Line Interface / CLI (Інтерфейс командного рядка):** Текстовий інтерфейс для керування комп'ютером за допомогою команд.
* **User (Користувач) / Group (Група):** Базові сутності в операційних системах Linux для управління доступом.
* **Permissions (Права доступу):** Правила, що визначають, хто може читати, змінювати або виконувати системні файли.
* **nologin:** Спеціальна оболонка, яка технічно існує, але забороняє користувачу інтерактивний вхід у систему.

---

## Завдання 1. Встановлення додаткових командних інтерпретаторів
В якості додаткових командних інтерпретаторів для системи (на базі Ubuntu) було обрано **Zsh** та **Fish**.

**Команди для встановлення:**
```bash
sudo apt install zsh fish -y
```

<a href="https://ibb.co/zHRrXQFj"><img src="https://i.ibb.co/bRBPsQFq/image.png" alt="image" border="0"></a>

**Короткий опис можливостей:**
1. **Zsh (Z shell):** Має величезну екосистему плагінів (наприклад, Oh My Zsh), потужне автодоповнення команд, підсвічування синтаксису та гнучкі можливості кастомізації рядка запрошення.
2. **Fish (Friendly Interactive Shell):** "Розумний" інтерпретатор з коробки. Пропонує автодоповнення на основі історії команд (сірим кольором), відмінне підсвічування синтаксису без необхідності додаткових налаштувань.

---

## Завдання 2 та 3. Створення користувачів, груп та призначення оболонок

**Створення груп:**
```bash
sudo groupadd technical_support
sudo groupadd developers
sudo groupadd financiers
sudo groupadd founders
sudo groupadd guests
```

<a href="https://ibb.co/YBZnbpH7"><img src="https://i.ibb.co/5hFp2BbW/image.png" alt="image" border="0"></a>

**Створення користувачів та призначення інтерпретаторів (за замовчуванням):**

1. **Technical support** (Інтерпретатор: `bash`):
```bash
sudo useradd -m -g technical_support -s /bin/bash tech1
sudo useradd -m -g technical_support -s /bin/bash tech2
```

2. **Developers** (Інтерпретатор: `zsh`):
```bash
sudo useradd -m -g developers -s /usr/bin/zsh dev1
sudo useradd -m -g developers -s /usr/bin/zsh dev2
```

3. **Financiers** (Заборона доступу — оболонка `nologin`):
```bash
sudo useradd -m -g financiers -s /usr/sbin/nologin fin1
sudo useradd -m -g financiers -s /usr/sbin/nologin fin2
```

4. **Founders** (Інтерпретатор: `fish`):
```bash
sudo useradd -m -g founders -s /usr/bin/fish found1
sudo useradd -m -g founders -s /usr/bin/fish found2
```

5. **Guests** (Заборона доступу — оболонка `nologin`):
```bash
sudo useradd -m -g guests -s /usr/sbin/nologin guest1
sudo useradd -m -g guests -s /usr/sbin/nologin guest2
```

<a href="https://ibb.co/jkmr9Q1B"><img src="https://i.ibb.co/VYRq0zPr/image.png" alt="image" border="0"></a>

---

## Завдання 4. Демонстрація роботи користувачів

### Група Technical support (оболонка bash)
```bash
root@Linux:~# su - tech1
tech1@Linux:~$ echo $SHELL
tech1@Linux:~$ uname -a
tech1@Linux:~$ date
```

<a href="https://ibb.co/XxHyFccr"><img src="https://i.ibb.co/0y5BYHHR/image.png" alt="image" border="0"></a>

### Група Developers (оболонка zsh)
```zsh
root@Linux:~# su - dev1
Linux% echo $SHELL
Linux% lscpu | grep "Model name"
```

<a href="https://ibb.co/6cdQK314"><img src="https://i.ibb.co/JWhZYfyz/image.png" alt="image" border="0"></a>

### Група Founders (оболонка fish)
```fish
root@Linux:~# su - found1
found1@Linux ~> echo $SHELL
found1@Linux ~> df -h /
```

<a href="https://ibb.co/gLnQGP8G"><img src="https://i.ibb.co/dwhXSLvS/image.png" alt="image" border="0"></a>

### Групи Financiers та Guests (заборонений доступ)
```bash
root@Linux:~# su - fin1
root@Linux:~# su - guest1
```

<a href="https://ibb.co/C3n9khCd"><img src="https://i.ibb.co/FLBYSgZv/image.png" alt="image" border="0"></a>

---

## Висновок / Conclusion


Під час виконання самостійної роботи над Ворк-кейсом №6 було успішно отримано практичні навички управління командними інтерпретаторами та обліковими записами користувачів у середовищі Linux. Було встановлено та проаналізовано додаткові оболонки, зокрема Zsh та Fish. Загалом створено 10 нових користувачів, яких розподілено на 5 функціональних груп. Кожній групі призначено відповідну оболонку за замовчуванням на основі їхніх технічних потреб. Очікувана поведінка перевірена шляхом авторизації в різних середовищах (`bash`, `zsh`, `fish`) та виконання базових системних команд. Вимоги безпеки також виконані: успішно заблоковано доступ до командного рядка для груп Financiers та Guests за допомогою оболонки `/usr/sbin/nologin`. Систему налаштовано коректно відповідно до завдання.

During the independent work on Work-case №6, practical skills in managing command-line interpreters and user accounts in a Linux environment were successfully acquired. Additional shells, specifically Zsh and Fish, were installed and analyzed. A total of 10 new users were created and categorized into 5 functional groups. Each group was assigned an appropriate default shell based on their technical requirements. Expected operational behavior was verified by successfully logging into different environments (`bash`, `zsh`, `fish`) and executing basic system commands. Security requirements were also met, successfully restricting CLI access for the Financiers and Guests groups by implementing the `/usr/sbin/nologin` shell. The system is configured correctly according to the provided instructions.
