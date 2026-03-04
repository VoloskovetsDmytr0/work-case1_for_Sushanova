# 🌐 Work-case 5: Робота з флеш-накопичувачем в ОС Ubuntu
**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис

---

# 📘 Словник термінів

**Монтування (Mounting)** — процес підключення файлової системи пристрою до каталогу в структурі Linux.

**Файлова система (File System)** — спосіб організації та збереження даних на носії інформації.

**Точка монтування (Mount Point)** — каталог, у який підключається зовнішній пристрій.

**Ядро (Kernel)** — основна частина операційної системи, що керує пристроями та ресурсами.

**Термінал (Terminal)** — програма для виконання команд у текстовому режимі.

**lsblk** — команда для перегляду підключених блочних пристроїв.

**mount / umount** — команди для підключення та відключення файлових систем.

---

# 📖 1. Теоретична частина

## 1.1 Як Linux працює з флешкою 🔌

Після підключення флеш-накопичувача:

1. Ядро Linux визначає пристрій (наприклад `/dev/sdb1`).
2. Система створює вузол пристрою.
3. Файлова система монтується у відповідний каталог.
4. Користувач отримує доступ до файлів.

У Linux всі файлові системи об’єднані в єдину структуру каталогів, яка починається з `/`.

Зазвичай флешка автоматично монтується в:

```
/media/ім'я_користувача/назва_пристрою
```

---

## 1.2 Суть операції монтування ⚙️

Монтування — це процес підключення файлової системи пристрою до каталогу в ієрархії Linux.

Без монтування:
- система не бачить файли
- неможливо працювати з даними

### Основні команди:

```bash
lsblk
sudo mkdir /mnt/usb
sudo mount /dev/sdb1 /mnt/usb
```

Відмонтування:

```bash
sudo umount /mnt/usb
```

---

## 1.3 Відмінність Linux та Windows 🆚

| Linux | Windows |
|--------|----------|
| Використовує монтування | Автоматично створює диск (E:, F:) |
| Єдина файлова структура | Окремі логічні диски |
| Можлива робота через термінал | Переважно GUI |

У Windows флешка автоматично з’являється як окремий диск.  
У Linux вона підключається до існуючої файлової структури.

---

# 🛠 2. Практична частина
<a href="https://ibb.co/hJvbGFV8"><img src="https://i.ibb.co/fz7f3dH0/image.png" alt="image" border="0"></a>
<a href="https://ibb.co/NdDYKQ22"><img src="https://i.ibb.co/5gpcLthh/image.png" alt="image" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/fzhJFVsx/image.png" alt="зображення" border="0"></a>
## 2.1 Підключення флешки до VirtualBox

1. Флешка підключена до фізичного комп’ютера.
2. У віртуальній машині обрано:

```
Devices → USB → Обрати пристрій
```

📸 **Скрін 1 — Підключення флешки у VirtualBox**  
<a href="https://ibb.co/cchH6pST"><img src="https://i.ibb.co/5Whyrzgc/image.png" alt="image" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/Q34DYJbc/image.png" alt="зображення" border="0"></a>

---

## 2.2 Копіювання через графічний інтерфейс 🖱

1. Відкрито файловий менеджер "Files".
2. Обрано флешку.
3. Скопійовано файл.
4. Вставлено у домашній каталог.

📸 **Відкрита флешка**  
<a href="https://ibb.co/1f1xscBY"><img src="https://i.ibb.co/GvyjsmGf/image.png" alt="image" border="0"></a>

📸 **Копіювання файлу**  
<a href="https://imgbb.com/"><img src="https://i.ibb.co/WvdVvPbG/image.png" alt="зображення" border="0"></a>

📸 **Файл у домашній папці**  
<a href="https://ibb.co/zHnVWz2z"><img src="https://i.ibb.co/JFBjW9p9/image.png" alt="image" border="0"></a>

---

## 2.3 Робота через термінал 💻

### Перевірка пристрою

```bash
lsblk
```

📸 **Результат lsblk**  
<a href="https://imgbb.com/"><img src="https://i.ibb.co/rKXYwhGY/image.png" alt="зображення" border="0"></a>

---

### Створення точки монтування

```bash
sudo mkdir /mnt/usb
```

---

### Монтування

```bash
sudo mount /dev/sdb1 /mnt/usb
```

📸 **Монтування флешки**  
<a href="https://ibb.co/N2Ydj7mM"><img src="https://i.ibb.co/v4z6PDQS/image.png" alt="image" border="0"></a>

---

### Перегляд вмісту

```bash
ls /mnt/usb
```

📸 **Вміст флешки**  
<a href="https://imgbb.com/"><img src="https://i.ibb.co/GLHWJNF/image.png" alt="зображення" border="0"></a>

---

### Копіювання файлу

```bash
cp /mnt/usb/назва_файлу ~/
```

📸 **Копіювання через cp**  
<a href="https://ibb.co/N64D2LzY"><img src="https://i.ibb.co/pvmVj3pX/image.png" alt="image" border="0"></a>

---

### Відмонтування

```bash
sudo umount /mnt/usb
```

📸 **Відмонтування**  
<a href="https://ibb.co/b5PZTXcg"><img src="https://i.ibb.co/hFyjbV3R/image.png" alt="image" border="0"></a>

---

# ✅ Висновок / Conclusion

У ході виконання роботи було досліджено механізм підключення флеш-накопичувача в операційній системі Linux. Було встановлено, що Linux використовує механізм монтування для інтеграції зовнішніх пристроїв у єдину файлову структуру. Практично було виконано підключення флешки, копіювання файлу через графічний інтерфейс та через термінал, а також безпечне відмонтування пристрою.

During this work, the mechanism of connecting a USB flash drive in the Linux operating system was studied. It was determined that Linux uses the mounting mechanism to integrate external devices into a unified file system structure. In practice, the USB drive was connected, a file was copied using both the graphical interface and terminal commands, and the device was safely unmounted.
