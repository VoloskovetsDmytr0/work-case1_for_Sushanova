Виконали Волосковець Дмитро та Перевишко Денис
--------------------------------------------------
1. Встановіть на своїй домашній робочій станції гіпервізор ІІ типу – Virtual Box, VMWare Workstation, Hyper-V (або інший на Ваш вибір).

- Я обрав собі VirtualBox, оскільки працюю з ним давно і він вже в мене встановлений.
  <a href="https://ibb.co/tpmMbLx5"><img src="https://i.ibb.co/zVnhS67w/image.png" alt="image" border="0"></a>
2. Опишіть набір базових дій в встановленому Вами гіпервізорі (VirtualBox):
- Створення нової віртуальної машини в VirtualBox

- 2.1 Запустіть Oracle VM VirtualBox.

- 2.2 Натисніть кнопку «Створити» (New).
<a href="https://ibb.co/BVwQKRqD"><img src="https://i.ibb.co/Fbnyqtgv/image.png" alt="image" border="0"></a>



- У вікні, що з’явиться:

- 2.3 Ім’я — введіть назву ВМ (наприклад, Ubuntu_22.04).

- 2.4 Тип ОС — оберіть тип (Linux, Windows тощо).

- 2.5 Версія — відповідну версію ОС.
 <a href="https://ibb.co/wNgJNkLh"><img src="https://i.ibb.co/xSLmSksq/image.png" alt="image" border="0"></a>


- 2.6 Виділіть обсяг оперативної пам’яті (RAM) за допомогою повзунка.
 <a href="https://imgbb.com/"><img src="https://i.ibb.co/3mWy6XSc/image.png" alt="зображення" border="0"></a>
- 2.7 Створіть віртуальний жорсткий диск:

- 2.8 Тип диска: VDI (VirtualBox Disk Image).

- 2.9 Формат: динамічно розподілений або фіксований.

- 2.10 Вкажіть розмір диска (наприклад, 20–50 ГБ).
 <a href="https://imgbb.com/"><img src="https://i.ibb.co/zTR63YfX/image.png" alt="зображення" border="0"></a>
- 2.11 Підтвердьте створення — віртуальна машина з’явиться у списку.

3. Встановіть в вашому гіпервізорі операційну систему GNU/Linux (будь-який зручний Вам дистрибутив) у базовій конфігурації з графічною оболонкою.


 <a href="https://ibb.co/7NCmcPs2"><img src="https://i.ibb.co/Z1XDs5qW/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/RKnPKFm"><img src="https://i.ibb.co/c95t9BH/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/gF9CBxV1"><img src="https://i.ibb.co/yBPJbrST/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/6RhkZ7tf"><img src="https://i.ibb.co/C5dft39T/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/yxrpj0X"><img src="https://i.ibb.co/MJmf0ns/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/yFrLc84r"><img src="https://i.ibb.co/4RHBnj1H/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/NdKgFZ0m"><img src="https://i.ibb.co/Pvgsrw29/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/hx43F11R"><img src="https://i.ibb.co/20CG3YY7/image.png" alt="image" border="0"></a>
 <a href="https://ibb.co/kgZg6qwR"><img src="https://i.ibb.co/rG9Gf5zC/image.png" alt="image" border="0"></a>
4. Створіть другу віртуальну машину та виконайте для неї наступні дії:
- Встановіть у мінімальній конфігурації з термінальним вводом-виводом без графічного інтерфейсу операційну систему GNU/Linux;
  За основу взяв Ubuntu Server, як раз без GUI:
  <a href="https://ibb.co/1Jm2k3d9"><img src="https://i.ibb.co/Z1MT03Yh/image.png" alt="image" border="0"></a>
- Встановіть графічну оболонку GNOME поверх встановленої в попередньому пункті ОС;

  Для початку треба оновити усі пакети:
  <a href="https://ibb.co/jvSvhWCQ"><img src="https://i.ibb.co/tM9MBx0v/image.png" alt="image" border="0"></a>
  <a href="https://ibb.co/M525zW1t"><img src="https://i.ibb.co/vvwvNgdT/image.png" alt="image" border="0"></a>
Тепер встановлю GNOME:
  <a href="https://ibb.co/hJKRsKq2"><img src="https://i.ibb.co/VcvWVvKM/image.png" alt="image" border="0"></a>
  <a href="https://ibb.co/TBfz72W9"><img src="https://i.ibb.co/yn9LZP4H/image.png" alt="image" border="0"></a>
Застосовуємо інтерфейс і перезапускаємось:
  <a href="https://ibb.co/qTZY5xY"><img src="https://i.ibb.co/Xcwx8Vx/image.png" alt="image" border="0"></a>
  <a href="https://ibb.co/gZwP8qXy"><img src="https://i.ibb.co/d46LvC3B/image.png" alt="image" border="0"></a>
  <a href="https://ibb.co/GfDJ9Djc"><img src="https://i.ibb.co/bjV3FVnz/image.png" alt="image" border="0"></a>
- Встановіть додатково ще другу графічну оболонку та порівняйте її можливості з GNOME.
Взяв за другу граф. оболонку XFCE, оскільки це був мій варіант:
 <a href="https://ibb.co/7dbSdDwQ"><img src="https://i.ibb.co/jPH8PYcz/image.png" alt="image" border="0"></a>
