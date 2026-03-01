# 🐧 Лабораторна робота №5: Робота з файловою системою Linux

**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис  
**Група:** БІКС-33  

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

## 3. Хід роботи

### Практичне виконання в терміналі

#### 1. Навігація та фільтрація в /etc
```bash
pwd
cd /etc
ls -d d* # Файли на літеру 'd' (Dmytro, Denys)
ls ??????     # Файли з 6 символів
ls *[id]      # Закінчуються на 'i' або 'd'

```

#### 2. Створення структури БІКС-33

```bash
cd ~
mkdir BIKS-33
cd BIKS-33
touch lab5
mkdir Voloskovets Perevyshko Unknown

```

#### 3. Робота з файлами

```bash
cd Voloskovets
echo "Hello, my name is Dmytro" > Dmytro
cp Dmytro Denys
echo "Hello, my name is Denys" > Denys
mv Denys ../Perevyshko/

```

#### 4. Рекурсивний вивід структури

```bash
cd ~
ls -R BIKS-33

```

---

## 4. Висновок / Conclusion

У ході виконання лабораторної роботи я опанував базові навички роботи в командному рядку (CLI) операційної системи Linux. Було вивчено стандарт ієрархії файлової системи (FHS) та практично відпрацьовано команди навігації, маніпуляції з файлами та каталогами, а також використання шаблонів для фільтрації даних.

During this laboratory work, I have acquired fundamental skills in working with the Linux Command Line Interface (CLI). I explored the Filesystem Hierarchy Standard (FHS) and gained practical experience with navigation, file and directory manipulation, and the use of globbing patterns for data filtering.

```
