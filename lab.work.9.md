# 🐧 Лабораторна робота №9: "Захист системи та користувачів у Linux. Створення користувачів та груп"

**👨‍💻 Виконали:** Волосковець Дмитро та Перевишко Денис  

---

## 1 Словник базових англійських термінів (Dictionary)

| Термін | Визначення та призначення |
| :--- | :--- |
| **User account** | Обліковий запис для ідентифікації та автентифікації користувача в системі. |
| **Root user** | Суперкористувач (адміністратор), що має повний доступ до всіх ресурсів ОС. |
| **Privileges** | Права доступу, що визначають перелік дозволених операцій. |
| **Group** | Логічне об'єднання облікових записів для управління колективними правами. |
| **UID (User ID)** | Унікальний числовий ідентифікатор користувача. |
| **GID (Group ID)** | Унікальний числовий ідентифікатор кожної групи в системі. |
| **Authentication** | Процедура перевірки справжності заявленого ідентифікатора (пароль). |
| **Authorization** | Надання прав на доступ до ресурсів після автентифікації. |
| **Primary group** | Основна група користувача (зазвичай однойменна з логіном). |
| **Secondary group** | Додаткова група для отримання розширених прав доступу. |

## 1.2 Теоретичні відомості: Концепція UPG (User Private Group)

**User Private Group (UPG)** — це схема, за якої для кожного нового користувача автоматично створюється однойменна група, де він є єдиним членом.
* **Доцільність:** Це забезпечує безпеку та ізоляцію даних у багатокористувацькому середовищі. Це дозволяє встановлювати права доступу на файли (наприклад, `rw-rw-r--`), не надаючи при цьому доступу стороннім особам, доки вони не будуть явно додані до цієї групи.

---

## 2. Інструментарій та методи виконання

У роботі використано наступні утиліти CLI:
* `id`, `getent` — перегляд ідентифікаторів та записів баз даних.
* `w`, `who`, `last` — моніторинг активності користувачів.
* `useradd`, `usermod`, `userdel` — керування обліковими записами.
* `groupadd`, `groupmod`, `groupdel` — керування групами.
* `passwd`, `chage` — безпека паролів та їх термінів дії.

---

## 3. Хід виконання роботи

### 3.1 Початкова робота в CLI та опис команд
Опрацьовано основні команди адміністрування в терміналі Ubuntu.

| Назва команди | Призначення та функціональність |
| :--- | :--- |
| `sudo` | Виконання операцій із привілеями адміністратора. |
| `su` | Заміна поточного ідентифікатора користувача на інший. |
| `id` | Виведення інформації про UID, GID та групи користувача. |
| `grep` | Фільтрація текстових даних (пошук по файлах /etc/passwd). |
| `last` | Історія останніх успішних та невдалих входів у систему. |
| `who` / `w` | Список активних користувачів та їх поточної діяльності. |
| `groupadd` | Створення нової групи користувачів. |
| `useradd` | Реєстрація нового користувача (параметр `-m` для home-директорії). |
| `usermod` | Зміна параметрів акаунту (параметр `-aG` для додавання в групи). |

### 3.2 Практичні завдання

**1. Інформація про поточного користувача:**
```bash
id
grep $USER /etc/passwd
```
> **[Вивід інформації id та grep]**

<a href="https://imgbb.com/"><img src="https://i.ibb.co/JWG5FZv1/image.png" alt="зображення" border="0"></a>

**2. Моніторинг активності (last, w, who):**
* `who` — показує лише хто увійшов.
* `w` — показує хто увійшов + навантаження та що роблять.
* `last` — показує історію сесій.
```bash
last -n 5
w
who
```
> **[Порівняння виводу last, w, who]**

<a href="https://ibb.co/B5VRBnZY"><img src="https://i.ibb.co/bMgnXbBG/image.png" alt="image" border="0"></a>
<a href="https://ibb.co/zWFdZxyf"><img src="https://i.ibb.co/20SJdhDK/image.png" alt="image" border="0"></a>

<a href="https://imgbb.com/"><img src="https://i.ibb.co/bjPVXr9F/image.png" alt="зображення" border="0"></a>

**3. Керування групами та користувачами:**
Створюємо групи `super_admins`, `noob_users` та `good_students`, а також трьох користувачів.
```bash
# Створення груп
sudo groupadd super_admins
sudo groupadd noob_users
sudo groupadd good_students

# Створення користувачів та паролів
sudo useradd -m user_alpha && sudo passwd user_alpha
sudo useradd -m user_beta && sudo passwd user_beta
sudo useradd -m user_gamma && sudo passwd user_gamma

# Додавання користувачів у групи
sudo usermod -aG super_admins,good_students user_alpha
sudo usermod -aG super_admins,noob_users,good_students user_beta
sudo usermod -aG noob_users,good_students user_gamma
```
> **[СКРІНШОТ: Створення груп та користувачів]**

<a href="https://imgbb.com/"><img src="https://i.ibb.co/0pTCZwCH/image.png" alt="зображення" border="0"></a>
<a href="https://ibb.co/m5XtBkQq"><img src="https://i.ibb.co/RTBPSfL0/image.png" alt="image" border="0"></a>
<a href="https://ibb.co/6RQ1dxJN"><img src="https://i.ibb.co/pvqRm8rn/image.png" alt="image" border="0"></a>

**4. Перевірка складу груп та очищення:**
```bash
grep -E 'super_admins|noob_users|good_students' /etc/group

# Видалення користувачів та груп
sudo userdel -r user_alpha
sudo userdel -r user_beta
sudo userdel -r user_gamma
sudo groupdel super_admins
sudo groupdel noob_users
sudo groupdel good_students
```
> **[СКРІНШОТ: Фінальна перевірка груп та видалення]**

<a href="https://ibb.co/60pdVr6J"><img src="https://i.ibb.co/r2LWTFnf/image.png" alt="image" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/20HywX7f/image.png" alt="зображення" border="0"></a>
---

## 4. Контрольні запитання

1. **Чому паролі не зберігаються в звичайному вигляді?** Через безпеку; у `/etc/shadow` зберігаються хеші, які неможливо прочитати зворотно.
2. **Чому не треба працювати під root?** Будь-яка випадкова помилка (як `rm -rf`) під root може миттєво знищити ОС.
3. **su vs sudo?** `su` потребує пароль root, `sudo` дозволяє виконати дію через пароль поточного юзера (якщо є права).
4. **Чому каталог root (/root) не в /home?** Щоб адміністратор міг зайти в систему для ремонту, якщо розділ `/home` зламався або не змонтувався.
5. **getent?** Дозволяє брати дані з системних баз, незалежно від того, локальні вони чи мережеві (LDAP).
6. **Змінити пароль?** Команда `passwd [username]`.
7. **Видалення груп?** `groupdel`. Назва зникає, файли залишаються з числовим GID.
8. **chage?** Керування терміном дії пароля (наприклад, зміна кожні 30 днів).
9. **usermod?** Найчастіші: `-aG` (групи), `-L` (блокування), `-l` (зміна логіна).

---

## 5. Висновки / Conclusions

Під час виконання лабораторної роботи я вивчив інструменти адміністрування користувачів та груп в Linux. Я навчився створювати облікові записи, керувати правами доступу через групи та використовувати утиліти для моніторингу безпеки системи. Отримані навички є базовими для захисту системи та розмежування прав користувачів.

During this laboratory work, I studied the tools for user and group administration in Linux. I learned how to create accounts, manage access rights through groups, and use utilities to monitor system security. The skills acquired are fundamental for protecting the system and separating user permissions.
