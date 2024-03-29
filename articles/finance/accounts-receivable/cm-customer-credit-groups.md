---
title: Кредитные группы клиентов
description: В этой статье приводятся сведения о кредитных группах клиента.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 032e92431946f0a41bf2e52c155e422d4ea0b3b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886526"
---
# <a name="customer-credit-groups"></a>Кредитные группы клиентов

[!include [banner](../includes/banner.md)]

Можно определить группы клиентов с общим кредитным лимитом. Также учитывается индивидуальный кредитный лимит, определенный в счете клиента в накладной.

Участники кредитной группы клиентов могут быть выбраны из других юридических лиц. При добавлении клиента в список клиентов в кредитной группе клиентов дата окончания кредитного лимита для каждого клиента изменяется на дату окончания срока действия, назначенную группе.

Группы кредитных клиентов можно настроить на странице **Кредитная группа клиентов** (**Управление кредитом \> Кредитные группы клиентов \> Кредитные группы клиентов**).

1. В полях **номер группы** и **Описание** введите код и описание для группы.
2. В полях **Кредитный лимит** и **Валюта** введите кредитный лимит и валюту, которые должны использоваться, когда система проверяет кредитный лимит для любого участника группы.
3. В поле **Дата окончания срока действия кредитного лимита** введите дату окончания кредитного лимита. Для кредитной группы должна быть указана дата окончания срока действия.

После завершения настройки кредитной группы клиентов можно добавлять в нее клиентов, указывая их юридическое лицо и код счета клиента. При добавлении нового клиента в кредитную группу клиентов система выполняет поиск по одному и тому же счету клиента по всем юридическим лицам и предлагает добавить его в кредитную группу клиента.

Используйте меню **Сальдо по срокам** для просмотра сведений о сальдо по срокам оплаты для всех клиентов накладных в кредитной группе клиентов. Страница **Сальдо периода распределения по срокам** показывает сводку сальдо по накладным для счетов клиентов.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
