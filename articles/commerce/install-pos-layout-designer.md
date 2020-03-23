---
title: Установка конструктора макетов POS
description: Можно использовать конструктор одним щелчком, чтобы создать различные макеты Modern POS (MPOS) и Cloud POS в альбомном или портретном режиме для магазинов, касс, кассиров и менеджеров.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023874"
---
# <a name="install-the-pos-layout-designer"></a>Установка конструктора макетов POS

[!include [banner](includes/banner.md)]

Можно использовать конструктор одним щелчком, чтобы создать различные макеты Modern POS (MPOS) и Cloud POS в альбомном или портретном режиме для магазинов, касс, кассиров и менеджеров.

Графический дизайн интерфейса для MPOS или Cloud POS управляется макетом кассы. Макет определяет расположение разных объектов. Примеры: общий макет, макет сетки элементов, макет клиента и макет платежей, а также макеты разных кнопок меню. Макеты также определяют общий вид интерфейса продаж, с которым работают работники.

## <a name="install-the-one-click-designer"></a>Установка конструктора одним щелчком

1. В Commerce с помощью левого верхнего меню откройте **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.
2. Выберите любой макет с типом приложения **Modern POS для Windows** или **Cloud POS**, затем нажмите **Конструктор макета**.
3. На панели уведомлений, которая отображается внизу окна Internet Explorer, щелкните **Открыть**, чтобы установить конструктор одним щелчком. (Панель уведомлений может отображаться в разных местах разных браузеров.)
4. В открывшемся окне сообщения **Выполнение приложения - предупреждение безопасности** щелкните **Выполнить** для установки хоста розничного конструктора. Индикатор хода выполнения показывает ход установки.
5. После установки на странице **Войти** введите свое имя пользователя и пароль Commerce и щелкните **Войти**, чтобы запустить конструктор.
6. После проверки учетных данных и запуска конструктора можно разработать собственный макет или изменить существующий макет.

    [![Макет в конструкторе одним щелчком](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Устранение неполадок установки конструктора макета

- Когда вы нажимаете **Конструктор**, запрос для загрузки (или выполнения) программы установки не отображаются или текущие параметры безопасности не позволяют загрузить файл. 

    **Решения:**

    - В Internet Explorer убедитесь, что блокатор всплывающих окон отключен для этого сайта. Щелкните **Настройки** &gt; **Свойства браузера** &gt; **Конфиденциальность** &gt; **найдите Блокирование всплывающих окон** и изменяет настройку, если изменение требуется.
    - В Internet Explorer добавьте URL-адрес Commerce в зону надежных сайтов. Щелкните **Настройки** &gt; **Свойства браузера** &gt; **Безопасность** &gt; **Надежные сайты** &gt; **Сайты** &gt; **Добавить**.

- Программа не запускается и отображается инструкция обратиться к поставщику.

    **Решение.** В Internet Explorer добавьте URL-адрес Commerce в зону надежных сайтов. Щелкните **Настройка** &gt; **Свойства браузера** &gt; **Безопасность** &gt; **Надежные сайты** &gt; **Сайты** &gt; **Добавить**.

**Известная проблема:** конструктор не работает правильно в браузерах Google Chrome и Mozilla Firefox. Мы работаем, чтобы устранить эту проблему.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка, установка и активация Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)