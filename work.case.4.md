# 🖥️ WORK-CASE 4  
## 👨‍💻 Виконали: Волосковець Дмитро та Перевишко Денис  

---

# 1. Теоретична частина

## 1.1 Що таке пакет?

**Пакет** — це спеціальний архів із програмою або бібліотекою, який містить:
- виконувані файли;
- залежності;
- службові скрипти;
- метадані.

В Ubuntu використовується формат **.deb**.

---

## 1.2 Що таке репозиторій?

**Репозиторій** — це сервер або онлайн-сховище, де зберігаються пакети програмного забезпечення.

---

## 1.3 Огляд менеджерів пакетів у Linux

| Дистрибутив | Менеджер | Формат | Основні можливості |
|------------|----------|--------|--------------------|
| Ubuntu, Debian | APT | .deb | Автоматичне вирішення залежностей, оновлення системи |
| Fedora | DNF | .rpm | Керування репозиторіями, швидке встановлення |
| Arch Linux | Pacman | .pkg.tar.zst | Простота, швидкість |
| openSUSE | Zypper | .rpm | Потужна система управління |
| Універсальний | Snap | .snap | Ізольовані пакети |
| Універсальний | Flatpak | .flatpak | Контейнерна ізоляція |

В Ubuntu використовується **APT (Advanced Package Tool)**.

---

# 2. Робота з APT

## 2.1 Оновлення списку пакетів

```bash
sudo apt update
```

[🔎 Переглянути скріншот](https://ibb.co/WWnYHMsD)  
<img src="https://i.ibb.co/PZxfrPtT/image.png" width="700">

---

## 2.2 Пошук пакета

```bash
apt search vlc
```

[🔎 Переглянути скріншот](https://ibb.co/tT25TMzG)  
<img src="https://i.ibb.co/NdNzd6rv/image.png" width="700">

---

## 2.3 Встановлення пакета

```bash
sudo apt install vlc
```

[🔎 Переглянути скріншот](https://ibb.co/ppJYZPt)  
<img src="https://i.ibb.co/MLMFphY/image.png" width="700">

---

## 2.4 Інформація про пакет

```bash
apt show vlc
```

[🔎 Переглянути скріншот](https://ibb.co/4wMrqZHW)  
<img src="https://i.ibb.co/Myp0vDmn/image.png" width="700">

---

## 2.5 Список встановлених пакетів

```bash
apt list --installed
```

[🔎 Переглянути скріншот](https://ibb.co/Kxzwd7GF)  
<img src="https://i.ibb.co/Dfgphkb5/image.png" width="700">

---

## 2.6 Видалення пакета

```bash
sudo apt remove vlc
```

[🔎 Переглянути скріншот](https://ibb.co/MDkZyMMK)  
<img src="https://i.ibb.co/273W0ggR/image.png" width="700">

---

## 2.7 Видалення зайвих залежностей

```bash
sudo apt autoremove
```

[🔎 Переглянути скріншот](https://ibb.co/B5XQGKSW)  
<img src="https://i.ibb.co/tT7vzPWj/image.png" width="700">

---

## 2.8 Оновлення системи

```bash
sudo apt upgrade
```

[🔎 Переглянути скріншот](https://ibb.co/84mSR2Z9)  
<img src="https://i.ibb.co/Pzrfb4Hg/image.png" width="700">

---

# 3. Встановлення середовища програмування

## Python

```bash
sudo apt install python3
sudo apt install idle3
```

[🔎 Переглянути скріншот](https://ibb.co/6cRPgLGw)  
<img src="https://i.ibb.co/4wZTP3Ct/image.png" width="700">

---

## C/C++

```bash
sudo apt install build-essential
```

[🔎 Переглянути скріншот](https://ibb.co/vvZsNyvw)  
<img src="https://i.ibb.co/1J8sCyJv/image.png" width="700">

---

# 4. Встановлення програм через графічне середовище

## 4.1 Через App Center

1. Відкрити програму **App Center**  
2. Ввести назву програми у пошуку  
3. Натиснути **Install**  
4. Ввести пароль користувача
[🔎 Переглянути скріншот](https://ibb.co/G4s1WHx6)  
<img src="https://i.ibb.co/1tsprzvg/image.png" width="700">

[🔎 Переглянути скріншот](https://ibb.co/WW14Xx2p)  
<img src="https://i.ibb.co/svrd4mVJ/image.png" width="700">

[🔎 Переглянути скріншот](https://ibb.co/5XzCJdMn)  
<img src="https://i.ibb.co/qL4h2zyW/image.png" width="700">

---

## 4.2 Через Snap

```bash
sudo snap install vlc
```
[🔎 Переглянути скріншот](https://ibb.co/pjp4gZ2k)  
<img src="https://i.ibb.co/m57hmtJP/image.png" width="700">

---

## 4.3 Через Flatpak

```bash
flatpak install flathub org.videolan.VLC
```
[🔎 Переглянути скріншот](https://ibb.co/tTSHXsbT)  
<img src="https://i.ibb.co/ycDNSy8c/image.png" width="700">

[🔎 Переглянути скріншот](https://ibb.co/7xqg13fg)  
<img src="https://i.ibb.co/xKNm7nkm/image.png" width="700">

[🔎 Переглянути скріншот](https://ibb.co/Tx6j8JjW)  
<img src="https://i.ibb.co/tTgjsnjL/image.png" width="700">

# Висновок

Менеджер пакетів **APT** дозволяє:
- встановлювати програми;
- оновлювати систему;
- видаляти пакети;
- працювати з репозиторіями.

Робота може виконуватися як через термінал, так і через графічний магазин App Center.
