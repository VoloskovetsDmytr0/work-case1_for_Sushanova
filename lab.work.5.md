# 🐧 Лабораторна робота №5: "Знайомство з командами навігації по файловій системі та керування файлами та каталогами"

**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис  

---

## 1. Словник термінів
| Термін | Опис |
| :--- | :--- |
| **CLI (Command Line Interface)** | Інтерфейс командного рядка для взаємодії з ОС. |
| **Root (/)** | Корінь файлової системи, початок усієї ієрархії. |
| **FHS** | Стандарт ієрархії файлової системи Linux. |
| **Argument** | Дані, які передаються команді (наприклад, ім'я файлу). |
| **Option (Flag)** | Параметр, що змінює дію команди (наприклад, `-l` для списку). |
| **Absolute Path** | Повний шлях від кореня `/`. |
| **Relative Path** | Шлях відносно поточної директорії. |

---

## 2. Відповіді на теоретичні питання

### 2.1 Порівняння Windows та Linux
* **Windows:** Використовує розділи (диски C:, D:), зворотний слеш (`\`). Регістр символів зазвичай не має значення.
* **Linux:** Єдине дерево каталогів від кореня `/`. Використовує прямий слеш (`/`). Регістр символів має значення (case-sensitive).

### 2.2 Поняття FHS
**FHS (Filesystem Hierarchy Standard)** — це стандарт, що визначає призначення основних каталогів у Linux, забезпечуючи уніфікацію структури незалежно від дистрибутива.

### 2.3 Основні команди
* `mkdir` / `touch` — створення каталогів/файлів.
* `mv` — переміщення або перейменування.
* `cp` — копіювання.
* `rm` — видалення.

---
Хід роботи:
---

## 🔹 1. Визначення поточного робочого каталогу

```bash
pwd
```

<a href="https://ibb.co/N2n2c24m"><img src="https://i.ibb.co/qYFYTYZW/image.png" alt="image" border="0"></a>

---

## 🔹 2. Перехід до кореневого каталогу та перевірка

```bash
cd /
pwd
```

<a href="https://ibb.co/SXqmghrD"><img src="https://i.ibb.co/VWXCG7m0/image.png" alt="image" border="0"></a>

---

## 🔹 3. Перегляд вмісту у довгому форматі

```bash
ls -l
```

<a href="https://ibb.co/4gfY39N6"><img src="https://i.ibb.co/sJP6zk30/image.png" alt="image" border="0"></a>

---

## 🔹 4. Перехід до `/usr/share` та перевірка

```bash
cd /usr/share
pwd
```

<a href="https://ibb.co/4RrFJzC3"><img src="https://i.ibb.co/zVvmNpCD/image.png" alt="image" border="0"></a>

---

## 🔹 5. Перегляд включаючи приховані файли

```bash
ls -a
```

<a href="https://ibb.co/GvnDpt6n"><img src="https://i.ibb.co/N6tqCmvt/image.png" alt="image" border="0"></a>

---

## 🔹 6. Перехід до каталогу `/etc`

```bash
cd /etc
```

<a href="https://ibb.co/mCk83Cz3"><img src="https://i.ibb.co/8DqcHD8H/image.png" alt="image" border="0"></a>

---

## 🔹 7. Файли, що починаються з літери імені (d)

```bash
ls d*
```

<a href="https://ibb.co/sJzBpLtL"><img src="https://i.ibb.co/YTwr4vbv/image.png" alt="image" border="0"></a>

---

## 🔹 8. Файли, назви яких складаються з 6 літер

```bash
ls ??????
```

<a href="https://ibb.co/9HKDLzHH"><img src="https://i.ibb.co/RTrFmZTT/image.png" alt="image" border="0"></a>

---

## 🔹 9. Файли, що закінчуються на літери імен (о / с)

Дмитро → O
Денис → S

```bash
ls *[os]
```

<a href="https://ibb.co/hRjbdFzZ"><img src="https://i.ibb.co/SX8bmwCd/image.png" alt="image" border="0"></a>

---

## 🔹 10. Перехід до домашнього каталогу та рекурсивний перегляд (зворотний порядок)

```bash
cd ~
ls -R | sort -r
```

<a href="https://ibb.co/tTqhyy7D"><img src="https://i.ibb.co/0RCXPPgr/image.png" alt="image" border="0"></a>

---

## 🔹 11. Створення директорії з назвою групи

```bash
mkdir БІКС-33
```

<a href="https://ibb.co/ZpCJppSQ"><img src="https://i.ibb.co/39Hs99vx/image.png" alt="image" border="0"></a>

---

## 🔹 12. Перегляд оновленого вмісту домашнього каталогу

```bash
ls -r
```

ℹ️ Ключ `-r` виводить список у зворотному алфавітному порядку.

<a href="https://ibb.co/ZpWnwLts"><img src="https://i.ibb.co/B5qX7zdD/image.png" alt="image" border="0"></a>

---

## 🔹 13. Створення файлу під назвою lab5

```bash
cd БІКС-33
touch lab5
```

<a href="https://ibb.co/1fMGFDk4"><img src="https://i.ibb.co/mC05fL3P/image.png" alt="image" border="0"></a>

---

## 🔹 14. Створення директорій студентів

```bash
mkdir Волосковець Перевишко
```

<a href="https://ibb.co/DffLf4qf"><img src="https://i.ibb.co/ZzzNzdZz/image.png" alt="image" border="0"></a>

---

## 🔹 15. Робота з першим студентом (Волосковець Дмитро)

```bash
cd Волосковець
touch Dmytro
```

<a href="https://ibb.co/0RqwftJR"><img src="https://i.ibb.co/jPhpLR4P/image.png" alt="image" border="0"></a>

---

## 🔹 16. Запис інформації у файл

```bash
echo "Hello, my name is Dmytro" > Dmytro
```

<a href="https://ibb.co/mFPXBPwy"><img src="https://i.ibb.co/JFSydS4p/image.png" alt="image" border="0"></a>

---

## 🔹 17. Перегляд файлу

```bash
cat Dmytro
```

<a href="https://ibb.co/Gfncw4kJ"><img src="https://i.ibb.co/Y4Pp9F8W/image.png" alt="image" border="0"></a>

---

## 🔹 18. Копія для другого студента

```bash
cp Dmytro Denys
ls
cat Denys
```

<a href="https://ibb.co/hFWJh6dG"><img src="https://i.ibb.co/b5BMq0v4/image.png" alt="image" border="0"></a>

---

## 🔹 19. Заміна вмісту Denys

```bash
echo "Hello, my name is Denys" > Denys
cat Denys
```

<a href="https://imgbb.com/"><img src="https://i.ibb.co/4wkrvmjg/image.png" alt="зображення" border="0"></a>

---

## 🔹 20. Переміщення файлу Denys

```bash
mv Denys ../Перевишко
```

<a href="https://ibb.co/4n4dVN4P"><img src="https://i.ibb.co/KpVwryVF/image.png" alt="image" border="0"></a>

---

## 🔹 21. Виведення каталогу БІКС-33 та всього його вмісту з кольорами

```bash
ls -R --color=auto БІКС-33*
```

<a href="https://ibb.co/jZM7F6tk"><img src="https://i.ibb.co/XksmT2Hx/image.png" alt="image" border="0"></a>

---

### Опис команд для переміщення по системі каталогів (навігація)

| Команда | Дія та опис |
| :--- | :--- |
| **`cd /`** | **Перехід у кореневий каталог.** Переміщує користувача у найвищу точку ієрархії файлової системи Linux. |
| **`cd /home`** | **Перехід у каталог користувачів.** Перехід за абсолютною адресою до папки, де зберігаються домашні директорії всіх користувачів системи. |
| **`cd ~`** | **Перехід у домашній каталог.** Символ `~` (тильда) є системним скороченням для шляху до особистої папки поточного користувача (наприклад, `/home/dmytro`). |
| **`cd`** | **Швидке повернення додому.** Виконання команди `cd` без аргументів автоматично повертає вас у ваш домашній каталог (аналог `cd ~`). |
| **`cd ..`** | **Перехід на один рівень вгору.** Переміщує у "батьківський" каталог відносно вашого поточного місцезнаходження. |
| **`cd ../..`** | **Перехід на два рівні вгору.** Дозволяє піднятися по дереву каталогів одразу на дві сходинки вище. |
| **`cd -`** | **Повернення до попереднього каталогу.** Переміщує у директорію, в якій ви перебували безпосередньо перед останньом зміною каталогу (як кнопка "Назад"). |

---

### Відповіді на контрольні запитання

#### 1. Як переглянути шлях до домашньої директорії за допомогою `echo`?

Існує два основних способи звернення до домашнього каталогу через змінні оточення або спеціальні символи:

* **Спосіб 1 (через зміну $HOME):**
```bash
echo $HOME

```


* **Спосіб 2 (через символ тильда `~`):**
```bash
echo ~

```



*Обидві команди виведуть повний шлях, наприклад: `/home/dmytro`.*

#### 2. Чи можна переглянути вміст кореня, не виходячи з дому?

Так, це можливо. Команда `ls` дозволяє переглядати вміст будь-якого каталогу, якщо вказати шлях до нього як аргумент. Перебуваючи в `~`, просто введіть:

```bash
ls /

```

Це виведе список папок у корені системи (`bin`, `etc`, `usr` тощо), не змінюючи вашу поточну робочу директорію.

#### 3. Яким чином можна додати інформацію в порожній файл?

Є три основні методи:

* **Перенаправлення виводу (найпростіший):**
```bash
echo "Ваш текст" > filename.txt

```


* **Використання текстового редактора:**
```bash
nano filename.txt  # (або vi / vim)

```


* **Команда `cat` з перенаправленням:**
```bash
cat > filename.txt
# після введення тексту натисніть Ctrl+D для збереження

```



#### 4. Як скопіювати та видалити існуючий каталог? Чи є різниця, якщо він не порожній?

Для роботи з каталогами (особливо не порожніми) обов'язково використовувати прапор **рекурсії `-r**`.

* **Копіювання:**
```bash
cp -r folder_source folder_destination

```


* **Видалення:**
```bash
rm -r folder_name

```


**Важливо:** Якщо каталог порожній, його можна видалити командою `rmdir`. Але якщо в ньому є хоча б один файл, `rmdir` видасть помилку. Тому команда `rm -r` є універсальною, оскільки вона видаляє каталог разом з усім його вмістом.

#### 5. Аналіз прикладів використання команди `mv`:

Команда `mv` (move) виконує різні ролі залежно від того, що вказано в другому аргументі:

1. `mv /work/tech/comp.png /Desktop`
* **Дія:** **Переміщення**. Файл переноситься з однієї директорії в іншу, зберігаючи свою назву.


2. `mv /work/tech/comp.png /work/tech/my_car.png`
* **Дія:** **Перейменування**. Оскільки шлях (директорія) залишається незмінним, змінюється лише ім'я самого файлу.


3. `mv /work/tech/comp.png /Desktop/computer.png`
* **Дія:** **Одночасно обидві дії**. Файл переміщується в іншу директорію і одночасно отримує нове ім'я.


---

## 4. 📝 Висновок / Conclusion

Під час виконання лабораторної роботи було здобуто практичний досвід роботи з інтерфейсом командного рядка (**CLI**) ОС Linux. Основну увагу приділено вивченню архітектури файлової системи за стандартом **FHS** та автоматизації рутинних завдань.

**Ключові досягнення:**
* **Навігація та маніпуляції:** Опановано інструменти створення, копіювання, переміщення та видалення об'єктів файлової системи.
* **Ефективність:** Вивчено механізми використання шаблонів (**globbing**) для швидкої фільтрації та обробки великих масивів даних.
* **Розуміння структури:** Досліджено призначення основних системних каталогів, що є базою для подальшого адміністрування.

---

During this laboratory work, I have gained hands-on experience with the Linux **Command Line Interface (CLI)**. The focus was on understanding the **Filesystem Hierarchy Standard (FHS)** and automating routine tasks.

**Key Takeaways:**
* **Navigation & Manipulation:** Mastered tools for creating, copying, moving, and deleting filesystem objects.
* **Efficiency:** Learned how to apply **globbing patterns** for rapid data filtering and batch processing.
* **Structural Insight:** Explored the roles of core system directories, establishing a foundation for advanced system administration.
