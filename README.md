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

![Screenshot_2025_01_15_15_23_44_67_c8c413cbdde2659431e41a03d647cf5f](https://github.com/user-attachments/assets/40f1c16f-2fbe-4c4e-b20c-2bd746b9ab73)

2. Находите пункт "Режим VPN для приложений"

![Screenshot_2025_01_15_15_23_49_51_c8c413cbdde2659431e41a03d647cf5f](https://github.com/user-attachments/assets/bca1cd5c-1878-4a05-a89f-db4b3b42d7ce)

3. Включаете режим "Прокси" (или оставляете "Обход") и выбираете приложения, которые нужно проксировать (или игнорировать)
Пример: 

![Screenshot_2025_01_15_15_24_04_34_c8c413cbdde2659431e41a03d647cf5f](https://github.com/user-attachments/assets/bb6a6cbf-354c-4fea-bd7a-2b6ee77cf805)

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
2. Качаете конфигурацию с [Releases](https://github.com/sucrosexd/vpnforlumiere/releases/tag/config), ~~так как файл иначе не закинуть.~~ (кликабельно)
3. Заходите в приложение, листаете ниже и находите пункт "Файл с настройками подключения"

![Screenshot_2025_01_15_15_17_18_34_c070da9001a1faa552ad1af3a9c1a6ed](https://github.com/user-attachments/assets/f16a8013-85ec-4d40-8fa7-e567d736b180)

4. На всякий, проверьте название файла и подтверждаете.

![-212690_temp](https://github.com/user-attachments/assets/19e15153-70c5-4a4a-833a-b55c36ca27b5)

5. Ура, всё работает!

![Screenshot_2025_01_15_15_27_46_60_c070da9001a1faa552ad1af3a9c1a6ed](https://github.com/user-attachments/assets/a58fa400-0411-4dba-9602-3374297314e3)

Если вам лень каждый раз выключать VPN, то можно настроить его на работу (или игнорирование) для отдельных приложений.
Для этого надо:
1. Открываете пункт настроек и находите пункт "Соединение"

![Screenshot_2025_01_15_15_21_02_01_c070da9001a1faa552ad1af3a9c1a6ed](https://github.com/user-attachments/assets/bc4d11f6-2d9b-45dd-9df9-e9fba8c9a261)

2. Открываете пункт "Раздельное туннелирование приложений"

![Screenshot_2025_01_15_15_21_04_96_c070da9001a1faa552ad1af3a9c1a6ed](https://github.com/user-attachments/assets/a9bec8cf-e8d3-4ab7-985d-f82e86892d24)

3. Выбираете нужный режим работы и нужные приложения.
Пример:

![Screenshot_2025_01_15_15_22_44_46_c070da9001a1faa552ad1af3a9c1a6ed](https://github.com/user-attachments/assets/7bd56101-816a-4e97-a385-5e2566c1d820)


### <a id="amnwindows">Windows</a>
1. Скачиваете [AmneziaVPN](https://github.com/amnezia-vpn/amnezia-client/releases/tag/4.8.2.3) для Windows (кликабельно)

![image_2025-01-15_18-36-20](https://github.com/user-attachments/assets/7bc3f867-2b4d-482e-a6e4-1d4975865203)

2. Тыкаете на "Далее" и всё установится.
3. Качаете конфигурацию с [Releases](https://github.com/sucrosexd/vpnforlumiere/releases/tag/config), ~~так как файл иначе не закинуть.~~ (кликабельно)
4. После установки и открытия приложения находите пункт "Файл с настройками подключения"

![image_2025-01-15_18-41-5911](https://github.com/user-attachments/assets/194123ce-f5a9-4f7b-a27b-07a6e9a4002b)

5. Добавляете конфигурацию, сверяете название файла (на всякий случай), подтверждаете.

![image_2025-01-15_18-41-591](https://github.com/user-attachments/assets/b95a686c-1f82-4b71-86ba-bd96c445c526)

6. Ура, всё работает!

![image_2025-01-15_18-41-592](https://github.com/user-attachments/assets/8081329a-4469-4b81-a69a-6d400e9d61bb)

</details>
<details>
  <summary>Бонус</summary>
  Жесть, так как этот сервак держится на моей стипендии и если вам не жалко пару деняк, можете закинуть мне немного на оплату сервака
  <details>
    <summary>реквизит (он один)</summary>
    СБП, Тинькофф: +79510917872
    подпись "на сервак" :ноготочки:
  </details>
</details>
