<h1>Различия прошивок Flipper Zero</h1>
<h3 align="center">
  <a href="Firmwares.md">English</a> | 
  <a href="Firmwares.zh-CN.md">中文</a> | 
  <a href="Firmwares.ja-JP.md">日本語</a> | 
  <a href="Firmwares.ru_RU.md" style="color: #ffffff;">Русский</a>
</h3>
<h3>
    <code>::</code> Последнее обновление 11 марта 2024 года. <code>::</code>
</h3>
<p>
    Этот документ поддерживает список различий между различными <a href="#official">прошивками Flipper Zero</a>.
</p>
<table>
    <tr>
        <td>
            <strong>Перейти к:</strong>
        </td>
        <td><a href="#official">Официальная</a></td>
        <td><a href="#unleashed">Unleashed</a></td>
        <td><a href="#plugins">RogueMaster</a></td>
        <td><a href="#Xtreme">Xtreme</a></td>
        <td><a href="#Dexv">Xvirus</a></td>
        <td><a href="#SquachWare">SquachWare</a></td>
        <td><a href="#v1nc">v1nc</a></td>
        <td><a href="#wetox">Wetox</a></td>
        <td><a href="#muddledbox">MuddledBox</a></td>
        <td><a href="#summary">Резюме (TL;DR)</a></td>
    </tr>
</table>
<h2 id="official">
    ✅ Официальная
    <kbd>
        <a href="https://github.com/flipperdevices/flipperzero-firmware">flipperdevices/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>Региональная блокировка передачи Sub-GHz из-за юридических ограничений.</li>
    <li>Невозможно сохранить и отправить скользящие коды (динамическое шифрование) в Sub-GHz, можно только отображать в списке захвата.</li>
    <li>Имя устройства по умолчанию отображается везде (Bluetooth-новости, USB-соединение и т.д.), изменить его невозможно.</li>
    <ul>
        <li><em>Команда Flipper имеет список имен устройств и соответствующую информацию о производстве <a
                    href="https://discord.com/channels/740930220399525928/765282833744265246/971881286543224852">(без
                    адреса доставки)</a>, чтобы упростить помощь при RMA.</em></li>
    </ul>
</ul>
<h2 id="unleashed">
    🔓 Unleashed
    <kbd>
        <a href="https://github.com/DarkFlippers/unleashed-firmware">DarkFlippers/unleashed-firmware</a>
    </kbd>
</h2>
<ul>
    <li><em>Стабильная пользовательская прошивка, сосредоточенная на новых функциях и улучшении оригинальных компонентов прошивки, почти без изменений UI</em></li>
    <li>Активная разработка, сообщество Discord очень активно.</li>
    <li>По умолчанию сняты ограничения на передачу в регионе Sub-GHz.</li>
    <li>Разрешение расширенного диапазона частот Sub-GHz через файл <em>dangerous_settings</em> (например, вызовы в ресторане).</li>
    <li>Разрешение изменения имени Flipper через настройки -> рабочий стол</li>
    <li>Добавление дополнительных частот Sub-GHz по умолчанию, без использования файла <em>setting_user</em>, файл <em>setting_user</em> остается неизменным для пользовательских настроек.</li>
    <li>Добавление дополнительных ключей Mifare classic в включенный файл словаря, пользовательский файл остается неизменным.</li>
    <li>Можно использовать для захвата, отправки или создания новых динамических протоколов шифрования/скользящих кодов, которые заблокированы в официальной прошивке (без кодов инкодера).<em>(например, современные гаражные двери)</em></li>
    <li>Можно вручную добавлять динамические сигналы и коды Sub-GHz, чтобы спарить Flipper с новыми пультами.</li>
    <li>Текущий список измененных и новых протоколов Sub-GHz <a
            href="https://github.com/DarkFlippers/unleashed-firmware#current-modified-and-new-subghz-protocols-list">можно
            найти здесь</a>.</li>
    <li>Дополнительно приложения и плагины, предоставленные через загрузчик приложений SD (файлы FAP).</li>
    <ul>
        <li>Больше деталей и полный список изменений можно найти в их <a
                href="https://github.com/DarkFlippers/unleashed-firmware#readme">README</a>.</li>
    </ul>
</ul>
<h2 id="plugins">
    💫 RogueMaster
    <kbd>
        <a
            href="https://github.com/RogueMaster/flipperzero-firmware-wPlugins">RogueMaster/flipperzero-firmware-wPlugins</a>
    </kbd>
</h2>
<ul>
    <li>Основан на <a href="#unleashed">Unleashed</a> как базовая прошивка (это ветвь <a href="#official">официальной</a> прошивки).</li>
    <li>Содержит копию приложения настроек Xtreme, большая часть кода была удалена и переименована в CFW настройки</li>
    <li>Предоставляет закрытую сборку от Patreon (код получен из открытого проекта)</li>
    <li>Сняты ограничения на передачу в регионе Sub-GHz путем изменения файла <em>extend_range.txt</em>.</li>
    <li>Разрешено расширение диапазона частот Sub-GHz через файл <em>extend_range.txt</em> (например, вызовы в ресторане).</li>
    <li>Имеет протоколы Sub-GHz и большинство других изменений, полученных из Unleashed FW (см. <a href="#unleashed">изменения</a>).</li>
    <li>Добавлены дополнительные пользовательские ресурсы <em>(словарь Mifare classic, примеры файлов и т.д.)</em>.</li>
    <li>Включает несколько PR из официальной прошивки, которые еще не были объединены (незавершенные, WIP) <em>(на переднем крае)</em></li>
    <li>Включает экспериментальный режим «только игра» (также известный как режим дурака).</li>
    <li>Включает улучшенную, но экспериментальную систему «уровней дельфинов».</li>
    <li>Дополнительно приложения и плагины, предоставленные через загрузчик приложений SD (файлы FAP).</li>
    <li>Также включает много других мелких настроек, изменений и множества дополнительных анимаций.</li>
    <ul>
        <li>Больше деталей и полный список можно найти в их <a
                href="https://github.com/RogueMaster/flipperzero-firmware-wPlugins#readme">README</a>.</li>
    </ul>
</ul>
<h2 id="Xtreme">
    💋 Xtreme
    <kbd>
        <a href="https://github.com/Flipper-XFW/Xtreme-Firmware">Flipper-XFW/Xtreme-Firmware</a>
    </kbd>
</h2>
<ul>
    <li>Изначально построен на RogueMaster, затем преобразован в ветвь Unleashed + <a href="#official">официальной</a> прошивки для будущей разработки.</li>
    <li>Добавлен пользовательский UI и темы главного меню, а также пакеты ресурсов (иконки, анимации)</li>
    <li>По умолчанию сняты ограничения на передачу в регионе Sub-GHz.</li>
    <li>Разрешение расширенного диапазона частот Sub-GHz через приложение настроек Xtreme (например, вызовы в ресторане).</li>
    <li>Разрешение изменения имени Flipper через приложение настроек Xtreme</li>
    <li>Имеет протоколы Sub-GHz и большинство других изменений, полученных из Unleashed FW (см. <a href="#unleashed">изменения</a>).</li>
    <li>Добавлены дополнительные пользовательские ресурсы <em>(словарь Mifare classic, больше анимаций (отдельная установка), примеры файлов и т.д.)</em>.</li>
    <li>Включает улучшенную/усовершенствованную систему «уровней дельфинов», аналогичную RogueMaster.</li>
    <li>Дополнительно приложения и плагины, предоставленные через загрузчик приложений SD (файлы FAP).</li>
    <li>Также включает много других мелких настроек, изменений и исправлений стабильности.</li>
</ul>
<h2 id="Dexv">
    ❌ Xvirus
    <kbd>
        <a href="https://github.com/Xvirus-Team/xvirus-firmware">Xvirus-Team/xvirus-firmware</a>
    </kbd>
</h2>
<ul>
    <li>Происходит из ветви <a href="#unleashed">Unleashed FW</a></li>
    <li>Добавлены пользовательские графические темы, не включенные в официальную прошивку.</li>
    <li>Сняты ограничения на передачу в регионе Sub-GHz путём изменения файла <em>extend_range.txt</em>.</li>
    <li>Разрешено расширение диапазона частот Sub-GHz через файл <em>extend_range.txt</em> (например, вызовы в ресторане).</li>
    <li>Имеет протоколы Sub-GHz и большинство других изменений, полученных из Unleashed FW (см. <a href="#unleashed">изменения</a>).</li>
    <li>Добавлены дополнительные пользовательские ресурсы <em>(словарь Mifare classic, примеры файлов и т.д.)</em>.</li>
    <li>Дополнительно приложения и плагины, предоставленные через загрузчик приложений SD (файлы FAP).</li>
</ul>
<h2 id="SquachWare">
    🌲 SquachWare
    <kbd>
        <a href="https://github.com/skizzophrenic/SquachWare-CFW">skizzophrenic/SquachWare-CFW</a>
    </kbd>
</h2>
<ul>
    <li><em>(OEM+)</em></li>
    <li><em>SquachWare на данный момент является устаревшим программным обеспечением! Хотя все ещё есть некоторые хорошие файлы, базовая прошивка очень устарела!! Надеюсь, в будущем восстановлю этот проект, но сейчас мы приостановили его!</em></li>
    <li>Добавлены пользовательские анимации/смайлы.</li>
    <li>Встроенный изменитель имени! (без необходимости перекомпиляции для изменения имени устройства).</li>
    <li>Дополнительно приложения и плагины, предоставленные через загрузчик приложений SD (файлы FAP).</li>
    <li>Включает скрипты Bad USB, разработанные сообществом.</li>
    <li>Включает файлы Sub-GHz, разработанные сообществом.</li>
    <ul>
        <li>Больше деталей можно найти в их <a
                href="https://github.com/skizzophrenic/SquachWare-CFW">README</a>.</li>
    </ul>
</ul>
<h2 id="v1nc">
    ⌨ v1nc
    <kbd>
        <a href="https://github.com/v1nc/flipperzero-firmware">v1nc/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>Поддержка использования различных раскладок клавиатуры для Duckyscripts с помощью ключевого слова <code>DUCKY_LANG</code>.</li>
    <li>Не синхронизируется с upstream Unleashed FW, похоже, не поддерживается больше.</li>
    <li>Включает некоторые интегрированные плагины и игры от сообщества, но не обновляет загрузчик FAP.</li>
</ul>
<h2 id="wetox">
    🎩 Wetox
    <kbd>
        <a href="https://github.com/wetox-team/flipperzero-firmware">wetox-team/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>Разработанная ветка для публичного использования, в то время как другие ветки предназначены для тестирования или архивирования хакатонов.</li>
    <li>Не синхронизируется с upstream официальной прошивкой, похоже, не поддерживается больше.</li>
    <li>Взлом T5577 RFID паролей с помощью атак словарей.</li>
    <li>Бренд на заголовке рабочего стола [WTX].</li>
    <li>Некоторые интересные экспериментальные материалы часто обновляются в разных <a
            href="https://github.com/wetox-team/flipperzero-firmware/branches">ветках</a>.</li>
</ul>
<h2 id="muddledbox">
    📦 MuddledBox
    <kbd>
        <a href="https://github.com/MuddledBox/flipperzero-firmware">MuddledBox/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>Первая «пользовательская прошивка», теперь устарела.</li>
    <li>Сняты ограничения на передачу в регионе Sub-GHz.</li>
    <li>Добавление саморекламных изображений на странице «О приложении» в настройках.</li>
    <li>Добавлены некоторые дополнительные общие частоты Sub-GHz.</li>
</ul>
<h2 id="summary">
    📝 Резюме
    <kbd>(TL;DR)</kbd>
</h2>
<ul>
    <li>Важно поддерживать синхронизацию с upstream (официальной) прошивкой.</li>
    <li>Снятие ограничений TX в большинстве случаев незаконно, риск на ваш страх и риск.</li>
    <li>MuddledBox является первой популярной веткой прошивки, но не развилась.</li>
    <li>Unleashed более сосредоточен на основных функциях, стабильности и протоколах Sub-GHz.</li>
    <li>Xtreme более сосредоточен на новых визуальных настроек, пользовательских интерфейсах и других аспектах.</li>
    <li>RogueMaster основан на Unleashed, но в некоторых случаях может быть менее стабильным, чем Unleashed.</li>
    <li>SquachWare происходит из ветки официальной прошивки, добавляя множество пользовательских элементов, сохраняя при этом безопасность и удобство официальной прошивки.</li>
</ul>


