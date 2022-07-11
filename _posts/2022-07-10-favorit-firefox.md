--- 
title: Установка Firefox из билдов Mozilla ( Linux )
categories:
  -linux
  -firefox
  -mozilla
#date: 2022-07-03 20:02:13
excerpt: '**Firefox** — это предустановленное приложение в Ubuntu/Debian/Fedora. К сожалению, он немного медленнее оригинального Firefox. Он также не полностью интегрирован в среду рабочего стола. Итак, если вы используете Firefox в качестве браузера, я рекомендую установить бинарную версию с веб-сайта Mozilla. Он будет работать немного быстрее и будет полностью интегрирован в ваш рабочий стол.'
permalink: / favorit-firafox/
---


Источники:
 * [https://support.mozilla.org](https://support.mozilla.org/ru/kb/ustanovka-firefox-na-linux#w_ustanovka-firefox-iz-bildov-mozilla-dlia-opytnykh-polzovatelei)

* [Get the original Firefox
](https://averagelinuxuser.com/ubuntu-22-04-after_install/#3-get-the-original-firefox)

**Firefox** — это предустановленное приложение в Ubuntu/Debian/Fedora. К сожалению, он немного медленнее оригинального Firefox. Он также не полностью интегрирован в среду рабочего стола. Итак, если вы используете Firefox в качестве браузера, я рекомендую установить бинарную версию с веб-сайта Mozilla. Он будет работать немного быстрее и будет полностью интегрирован в ваш рабочий стол.

Эта установка будет иметь приоритет над версией Firefox, установленной посредством вашего менеджера пакетов. Чтобы запустить версию, установленную с помощью вашего менеджера пакетов, вам придётся запускать бинарник из терминала. Чтобы сделать это в большинстве дистрибутивов, откройте терминал и введите: **/usr/bin/firefox**

Чтобы установить Firefox, следуйте инструкциям Mozilla :

1. Перейдите на [страницу загрузки Firefox](https://www.mozilla.org/ru/firefox/linux/?utm_medium=referral&utm_source=support.mozilla.org) или  [страница загрузки Firefox ESR](https://www.mozilla.org/ru/firefox/all/#product-desktop-esr) и щёлкните по кнопке **Загрузить сейчас**

2. Откройте терминал и перейдите к папке, в которой сохраняются ваши загрузки. Например:

`cd ~/Downloads `

Распакуйте архив:

`tar xjf firefox-*.tar.bz2 `

Переместите файлы Firefox в /opt:

`mv firefox /opt `

Создайте символическую ссылку на бинарный файл Firefox:

`ln -s /opt/firefox/firefox /usr/local/bin/firefox `

Загрузите файл рабочего стола:

`wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications `

### Удалите снап-версию Firefox:

`sudo snap remove firefox `

Запустите новый Firefox, выполнив эту команду в терминале:

`/usr/local/bin/firefox `

Перейдите в Dock -> щелкните правой кнопкой мыши Firefox -> Добавить в избранное -> Переместите его наверх

>Также, если на вашем компьютере не установлен wget, перейдите на URL, упомянутый выше, щёлкните правой кнопкой мыши на странице, чтобы открыть контекстное меню и выберите Сохранить как. После загрузки файла переместите его в **/usr/local/share/applications**

>Чтобы проверить, что установка прошла успешна, вы можете открыть страницу Информация для решения проблем. В разделе Сведения о приложении значение Бинарный файл приложения должно быть **/opt/firefox/firefox-bin**

<style type="text/css" media="all">
   body{
       width: 90%;
       max-width: 960px;
       margin: 0 auto;
       font-size:1.2em;
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
