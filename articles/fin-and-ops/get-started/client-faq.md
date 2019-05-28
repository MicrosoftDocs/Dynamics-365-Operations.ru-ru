---
title: Часто задаваемые вопросы по клиенту Finance and Operations
description: Эта статья дает ответы на часто задаваемые вопросы о клиенте Microsoft Dynamics 365 for Finance and Operations.
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74f85f7a1c390d1f21d0423a794ff16c7250d9fa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546855"
---
# <a name="finance-and-operations-client-faq"></a>Часто задаваемые вопросы по клиенту Finance and Operations

[!include [banner](../includes/banner.md)]

Эта статья дает ответы на часто задаваемые вопросы о клиенте Microsoft Dynamics 365 for Finance and Operations.

## <a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Почему не загружаются символы при использовании Finance and Operations?

Параметры безопасности в вашем браузере могут стать причиной неправильной загрузки символов. Чтобы решить эту проблему, выполните следующие шаги.

- При возникновении этой проблемы в обозревателе Internet Explorer щелкните **Сервис**, затем щелкните **Свойства браузера**. В диалоговом окне свойств обозревателя на вкладке **Безопасность** щелкните **Другой** и убедитесь, что выбран параметр **Скачивание шрифта**.
- В противном случае может потребоваться добавить сайт Finance and Operations в список доверенных сайтов.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Мне не хватает ленты из Dynamics AX 2012. Можно ли сделать так, чтобы вкладки панели действий всегда были открыты?

Мы планируем реализовать эту функцию в скором времени. После этого пользователи смогут оставлять вкладки области действий открытыми все время. В противном случае вкладки будут сворачиваться, когда не используются, чтобы предоставить больше пространства экрана для страницы.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Почему иногда отображаются различные меню при щелчке правой кнопкой мыши?

При щелчке редактируемого поля правой кнопкой мыши (или при выборе текста) отображается контекстное меню браузера. Это меню предоставляет доступ к командам **Вырезать**, **Копировать** и **Вставить**. Мы не можем встроить эти команды в контекстные меню Finance and Operations, поскольку из соображений безопасности браузеры не позволяют получать доступ к буферу обмена системы программным способом.

Если щелкнуть правой кнопкой мыши ярлык поля или значение доступного только для чтения элемента управления, отобразится контекстное меню Finance and Operations.

Чтобы упростить доступ с клавиатуры, мы планируем реализовать сочетание клавиш в будущем, при нажатии которого будет открываться контекстное меню Finance and Operations.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Где находится функция "Просмотр сведений" в Finance and Operations?

Параметр **Просмотр сведений** доступен в нескольких местах:

- Если элемент управления имеет возможности **Просмотр сведений** и если элемент управление имеет значение, то это значение отображается как гиперссылка. Можно перейти по гиперссылке, чтобы открыть страницу, которая содержит дополнительные сведения.
- **Просмотр сведений** также является параметром в контекстных меню Finance and Operations. Дополнительные сведения о том, когда отображаются контекстные меню Finance and Operations при щелчке правой кнопкой мыши, см. в предыдущем разделе.
