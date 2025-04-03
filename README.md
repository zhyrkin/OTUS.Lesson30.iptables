# OTUS.Lesson30.iptables
Домашнее задание:
1) реализовать knocking port
centralRouter может попасть на ssh inetrRouter через knock скрипт.
2) добавить inetRouter2, который виден(маршрутизируется (host-only тип сети для виртуалки)) с хоста или форвардится порт через локалхост.
3) запустить nginx на centralServer.
4) пробросить 80й порт на inetRouter2 8080.
5) дефолт в инет оставить через inetRouter.

Тестовый Стенд: 8 VM (2CPU, 2Gb RAM, 6Gb HDD, OS Ubuntu 24.04s)

После завершения работы плейбука проверим результаты:

1) Попробуем подключиться к inetrouter с centralRouter, соединение не пройдет, и запустив скрипт мы увидим приглашение принять отпечаток и затем ввести пароль  
   ![Скриншот 03-04-2025 100944](https://github.com/user-attachments/assets/989ba5ca-2638-4053-8736-b6e5912b17f4)

   Так же мы можем увидеть как меняются правила iptables на inetrouter  
  ![Скриншот 03-04-2025 101016](https://github.com/user-attachments/assets/95c9728b-c819-445e-85a5-10a07e8efbf6)  
  ![Скриншот 03-04-2025 101048](https://github.com/user-attachments/assets/b2d4764c-a42f-445f-bd47-049f46b8083c)  
  
2) Проверим что служба nginx запущена на centralserver  
     ![Скриншот 03-04-2025 101232](https://github.com/user-attachments/assets/5d3b2805-8984-4132-b034-90003f5a4bc3)  
   и проверим что при обращении к inetrouter2 на порт 8080 нас перенаправит на centralserver 80 порт  
   ![Скриншот 03-04-2025 111840](https://github.com/user-attachments/assets/b1aab8ec-de97-40f9-bb9c-286c008bde57)  






