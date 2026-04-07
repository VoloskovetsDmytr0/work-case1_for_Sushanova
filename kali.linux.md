# Звіт по Kali Linux

## Хід роботи

### 1. Встановлення ОС Kali Linux (2 бали)
Було розгорнуто операційну систему Kali Linux у середовищі віртуалізації. Налаштовано базові мережеві параметри для взаємодії з тестовим середовищем.
<p align="center">
  <a href="https://ibb.co/tpGXNbDC"><img src="https://i.ibb.co/v4FYrJkz/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/twM3hhfs"><img src="https://i.ibb.co/qLMxnnGs/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/ymbdzfqz"><img src="https://i.ibb.co/hxtLG7VG/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/cSRHv4YC"><img src="https://i.ibb.co/nN4v0xPn/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/p6p78mHB"><img src="https://i.ibb.co/JWP14hYw/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/TxsQs9X7"><img src="https://i.ibb.co/VcsFsfyz/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/pjYZQkjH"><img src="https://i.ibb.co/JjD2qSjY/image.png" alt="image" border="0" width="30%"></a>
  <a href="https://ibb.co/WWxnGk1b"><img src="https://i.ibb.co/DDV4z9nx/image.png" alt="image" border="0" width="30%"></a>
</p>

---

### 2. Інструмент для збору інформації (2 бали)
Для виконання етапу Information Gathering було обрано мережевий сканер **Nmap**. 

Було проведено сканування тестової цілі для виявлення відкритих портів, активних сервісів та визначення версії операційної системи за допомогою команди:
`nmap -sV -O [IP_адреса_цілі]`

<a href="https://ibb.co/k24QKqrF"><img src="https://i.ibb.co/7tn2vrTF/image.png" alt="image" border="0"></a>


---

### 3. Інструмент для аналізу вразливостей (2 бали)
На основі зібраних даних було обрано сканер **Nikto** для детального аналізу веб-сервісу цілі.

Було запущено сканування HTTP-сервісу командою:
`nikto -h http://[IP_адреса_цілі]`

<a href="https://ibb.co/twbQyC74"><img src="https://i.ibb.co/zWSQKfyr/image.png" alt="image" border="0"></a>


---

### 4. Інструмент для тестування на проникнення (2 бали)
Для етапу експлуатації було використано **Metasploit Framework**. Базуючись на результатах розвідки, було обрано відповідний експлойт (наприклад, для вразливого FTP-сервісу).

Було налаштовано параметри `RHOSTS` (IP цілі) та `LHOST` (локальний IP), після чого виконано атаку.
<a href="https://ibb.co/RpKpjx1Z"><img src="https://i.ibb.co/VWGWw7dr/image.png" alt="image" border="0"></a>

---

## Conclusion
During this practical work, the core methodology of penetration testing was successfully demonstrated using the Kali Linux environment. Information gathering was conducted using Nmap to map the network and identify running services. Subsequently, Nikto was deployed to scan for web-based vulnerabilities and misconfigurations. Active exploitation was achieved via the Metasploit Framework, bypassing system defenses and gaining unauthorized access. Finally, post-exploitation procedures were executed using Meterpreter, confirming full system compromise, and the gathered intelligence was aggregated and exported using Metasploit's database reporting tools. The results emphasize the critical importance of timely software updates, secure configurations, and proactive network auditing.
