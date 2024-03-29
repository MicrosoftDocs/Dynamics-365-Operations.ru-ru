---
title: Запишите номера подлежащих возмещению сертификатов TDS
description: В этой статье объясняется, как использовать страницу "Подлежащие возмещению сертификаты" для записи номеров и дат сертификатов для налога, удерживаемого у источника (TDS), которые получаются для конкретного поставщика, клиента или книги учета.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853266"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Запишите номера подлежащих возмещению сертификатов TDS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как использовать страницу **Подлежащие возмещению сертификаты** для записи номеров и дат сертификатов для налога, удерживаемого у источника (TDS), которые получаются для конкретного поставщика, клиента или книги учета. Чтобы обновить номера и даты сертификатов TDS, записанных для проводок TDS на этой странице, воспользуйтесь страницей **Обновление сертификата** (**Главная книга \> Периодически \> Подоходный налог \> Обновление сертификата**). После завершения обновления номеров сертификатов TDS закройте их.

Чтобы записать номера и даты сертификатов TDS, выполните следующие действия.

1. Перейдите в раздел **Налог \> Косвенный налог \> Подоходный налог \> Подлежащие возмещению сертификаты**.

    [![Страница подлежащих возмещению сертификатов.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. На странице **Подлежащие возмещению сертификаты** в поле **Тип налога** выберите **TDS**.
3. Выберите **Создать**, чтобы создать запись.
4. В поле **Номер сертификата** введите номер сертификата TDS.
5. В поле **Тип счета** выберите тип счета, для которого получается сертификат TDS: **Поставщик**, **Клиент** или **Главная книга**.
6. В поле **Счет** выберите поставщика, клиента или номер счета ГК, в зависимости от выбранного типа счета. В поле **Имя** отображается имя поставщика, клиента или счета ГК.
7. В поле **Сумма сертификата** введите сумму сертификата TDS.
8. В поле **Дата** введите дату сертификата для номера сертификата.
9. Выберите **Запросы**, чтобы открыть страницу **Проводки сертификата**, на которой можно просмотреть проводки TDS, для которых обновляются номер и дата сертификата TDS. Эти сведения могут быть обновлены на странице **Обновление сертификата** (**Налог \> Декларации \> Подоходный налог \> Обновление сертификата**).

    На странице **Обновление сертификата** в каждой проводке TDS отображаются следующие сведения:

    - **Дата** — дата разноски проводки TDS.
    - **Ваучер** — код ваучера проводки TDS.
    - **Источник** — модуль, в котором была создана проводка TDS.
    - **Счет** — номер поставщика, клиента или счета ГК, для которого была создана проводка TDS.
    - **Имя** — имя поставщика, клиента или счета ГК, для которого была создана проводка TDS.
    - **Сумма** — сумма накладной, для которой рассчитан TDS.
    - **Сумма налога** — сумма налога TDS, рассчитанная для проводки.
    - **Дата сертификата** — дата сертификата TDS, которая была обновлена для проводки TDS.
    - **Номер сертификата** — номер сертификата TDS, который был обновлен для проводки TDS.

10. На странице **Подлежащие возмещению сертификаты** установите флажок **Закрыто**, чтобы закрыть номер сертификата TDS после завершения его обновления для проводок TDS на странице **Обновить сертификат**.

    Чтобы установить флажок **Закрыто** для всех записей на странице, выберите **Пометить все**.

    > [!NOTE]
    > Номера сертификатов TDS, для которых установлен флажок **Закрыто** на странице **Обновить сертификат** недоступны.
