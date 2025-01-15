# vpnforlumiere
Инструкция для настройки VPN (VLESS или Amnezia) для участников проекта Lumiere. 

### Выбор протокола:
- <a href="#vless">VLESS</a> - лёгкий и быстрый протокол, который всегда остаётся незамеченным даже в Китае из-за маскировки под HTTPS-трафик.
- <a href="#amnezia">AmneziaWG</a> - протокол на основе WireGuard, был изменён для исключения обнаружения протокола. 

<details>
<summary><a id="vless">VLESS (NekoBox/V2Box/NekoRay)</a></summary>
Выбор платформы:
1. <a href="#vlandroid">Android</a>
2. <a href="#vlios">iOS</a>
3. <a href="#vlwindows">Windows</a>
  
### <a id="vlandroid">Android</a>
1. Качаем  [NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid/releases/) (кликабельно). Рекомендуется первый файл, если не устанавливается - качаем второй файл (в крайних случаях).

![android1](https://github.com/user-attachments/assets/fb708a8b-06c9-4a4a-aed8-8c470db38134)

2. Копируете конфигурацию, заходите в приложение и разрешаете уведомления.
> ```vless://bf41ea56-e8fc-4ddc-abb8-7c5af381c26f@147.45.69.83:443?security=reality&type=tcp&headerType=&path=&host=&sni=wikiportal.su&fp=chrome&pbk=hC-5z-MOBkbDKyOmn0HHGZydlbzb_UmnfLQPNFwk7DY&sid=d78758a007ae678a#lumiere```
3. Нажимаете "Добавить профиль" (рядом с поиском) и там же "Импорт из буфера обмена"

![photo_2024-11-10_01-26-16](https://github.com/user-attachments/assets/bac44295-8cf1-4407-94e7-01e8b3b44cc7)

4. Нажимаем на кнопку внизу и разрешаем подключение по VPN.

Если вам лень каждый раз выключать VPN, то можно настроить его на работу (или игнорирование) для отдельных приложений.
Для этого надо:
1. Открываете боковое меню и открываете настройки



2. Находите пункт "Режим VPN для приложений"



3. Включаете режим "Прокси" (или оставляете "Обход") и выбираете приложения, которые нужно проксировать (или игнорировать)
Пример: 


### <a id="vlios">iOS</a>
~~Честно, у меня нет яблока под рукой, но в принципе всё схоже.~~
1. Качаете [V2BOX](https://apps.apple.com/us/app/v2box-v2ray-client/id6446814690) из App Store
2. Копируете конфигурацию, заходите и сразу переходите в вкладку "Configs"
> ```vless://bf41ea56-e8fc-4ddc-abb8-7c5af381c26f@147.45.69.83:443?security=reality&type=tcp&headerType=&path=&host=&sni=wikiportal.su&fp=chrome&pbk=hC-5z-MOBkbDKyOmn0HHGZydlbzb_UmnfLQPNFwk7DY&sid=d78758a007ae678a#lumiere```
3. Нажимаете на плюсик и выбираете "Импортировать v2ray из буфера" (или же первый пункт в ссылке)
4. Подключаетесь и проверяете работу.

### <a id="vlwindows">Windows</a>
~~Готовьтесь, много букв и много действий~~
1. Качаете [NekoRay](https://github.com/Matsuridayo/nekoray/releases) (кликабельно). Нам нужна версия для Windows, поэтому качаем четвертый по списку файл.

![screenshot_10112024_013805](https://github.com/user-attachments/assets/68eb533d-84cb-4295-b974-ec06c4f45d21)

2. Распаковываем архив любым удобным способом, открываем папку "nekoray" и открываем "nekobox.exe" *(для удобства дальнейшего использования можно создать ярлык - перетащить этот файл с **зажатым Alt**, тогда система сама создаст ярлык)*

![screenshot_10112024_013621](https://github.com/user-attachments/assets/d8a527ab-27f9-4517-939e-282768678597)

3. Копируем конфигурацию, нажимаем на Сервер => Добавить профиль из буфера обмена
> ```vless://bf41ea56-e8fc-4ddc-abb8-7c5af381c26f@147.45.69.83:443?security=reality&type=tcp&headerType=&path=&host=&sni=wikiportal.su&fp=chrome&pbk=hC-5z-MOBkbDKyOmn0HHGZydlbzb_UmnfLQPNFwk7DY&sid=d78758a007ae678a#lumiere```

![screenshot_10112024_014347](https://github.com/user-attachments/assets/1ded404e-cecd-43aa-801f-54d92afa36ba)

4. После того, как профиль был добавлен, нажимаем на галочку "Режим TUN" и соглашаемся на открытие с правами администратора

![screenshot_10112024_014756](https://github.com/user-attachments/assets/21a6de96-c824-4866-8257-39962275a698)

5. После перезапуска с правами администратора нажимаем правой кнопкой мыши по нашему профилю и запускаем его.

![screenshot_10112024_014902](https://github.com/user-attachments/assets/b1950a9d-25a9-46d6-b6ad-8fc4ea3d6867)

</details>
<details>
<summary><a id="amnezia">AmneziaWG (собственный клиент)</a></summary>
Выбор платформы:
1. <a href="#amnandroios">Android/iOS</a>
2. <a href="#amnwindows">Windows</a>

### <a id="amnandroios">Android/iOS</a>
#### Все дальнейшие действия будут производиться на Android, на iOS действия одинаковые. ~~(ну. почти. надеюсь.)~~
1. Качаете AmneziaVPN для [Android](https://play.google.com/store/apps/details?id=org.amnezia.vpn) или [iOS](https://apps.apple.com/us/app/amneziavpn/id1600529900) (кликабельно)
2. Качаете конфигурацию с Relases, ~~так как файл иначе не закинуть.~~
3. Заходите в приложение, листаете ниже и находите пункт "Файл с настройками подключения"



4. На всякий, проверьте название файла и подтверждаете продолжение.



5. Ура, всё работает!



### <a id="amnwindows">Windows</a>
1. вхыазахывза
</details>
