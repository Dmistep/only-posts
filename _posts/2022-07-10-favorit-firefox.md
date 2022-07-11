--- 
title: Установка Firefox из билдов Mozilla ( Linux )
permalink: / favorit-firafox/
---


Источник: [https://support.mozilla.org](https://support.mozilla.org/ru/kb/ustanovka-firefox-na-linux#w_ustanovka-firefox-iz-bildov-mozilla-dlia-opytnykh-polzovatelei)

<p>Перед установкой Firefox, убедитесь, что на вашем компьютере установлены необходимые библиотеки. Отсутствие библиотек сделает Firefox неработоспособным.</p>
<p>Чтобы установить Firefox с помощью этого метода, вы должны иметь возможность заходить от <b>root</b> или запускать команды <b>sudo</b>.</p>
<p><mark>Эта установка будет иметь приоритет над версией Firefox, установленной посредством вашего менеджера пакетов.</mark> Чтобы запустить версию, установленную с помощью вашего менеджера пакетов, вам придётся запускать бинарник из терминала. Чтобы сделать это в большинстве дистрибутивов, откройте терминал и введите: <b>/usr/bin/firefox</b>.</p>

1. Перейдите на [страницу загрузки Firefox](https://www.mozilla.org/ru/firefox/linux/?utm_medium=referral&utm_source=support.mozilla.org) или  [страница загрузки Firefox ESR](https://www.mozilla.org/ru/firefox/all/#product-desktop-esr) и щёлкните по кнопке **Загрузить сейчас**

2. Откройте терминал и перейдите к папке, в которой сохраняются ваши загрузки. Например:

`cd ~/Downloads`

3. Распакуйте содержимое загруженного файла, введя:

`tar xjf firefox-*.tar.bz2`

4. Перенесите распакованную папку Firefox в /opt:

`mv firefox /opt`

5. Создайте символическую ссылку на исполняемый файл Firefox:

`sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox`

6. Загрузите копию файла рабочего стола:

`sudo wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications`

>Также, если на вашем компьютере не установлен wget, перейдите на URL, упомянутый выше, щёлкните правой кнопкой мыши на странице, чтобы открыть контекстное меню и выберите Сохранить как. После загрузки файла переместите его в /usr/local/share/applications.

>Чтобы проверить, что установка прошла успешна, вы можете открыть страницу Информация для решения проблем. В разделе Сведения о приложении значение Бинарный файл приложения должно быть /opt/firefox/firefox-bin.

<style type="text/css" media="all">
   body{
       width: 90%;
       max-width: 720px;
       margin: 0 auto;
   }
   h1,h2,h3,h4{
       color: #192a3d;
   }
   p{
       color: #3a4f66;
   }
   a{
       color: #2872fa;
       text-decoration: none;
       font-weight: 500;
   }
</style>
