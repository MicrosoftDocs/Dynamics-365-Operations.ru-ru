---
title: Обновление номеров сертификатов и дат для проводок TDS
description: В этой статье объясняется, как обновлять номера и даты подлежащих возмещению сертификатов, записанные для поставщика, клиента и счетов книги учета для налога, удерживаемого у источника (TDS).
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
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904451"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Обновление номеров сертификатов и дат для проводок TDS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как обновлять номера и даты подлежащих возмещению сертификатов, записанные для поставщика, клиента и счетов книги учета для налога, удерживаемого у источника (TDS). Сертификаты для проводок TDS можно просмотреть на странице **Подлежащие возмещению сертификаты**. Для обновления сертификатов можно воспользоваться страницей **Обновление сертификатов**.

Чтобы обновить номера и даты сертификатов для проводок TDS, выполните следующие действия.

1. Перейдите **Налог \> Декларации \> Подоходный налог \> Обновление сертификата**.

    [![Страница «Обновление сертификата».](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. На странице **Обновление сертификата** в разделе **Выбор** в поле **Тип налога** выберите **TDS**.
3. В поле **Номер сертификата** выберите номер сертификата TDS клиента или поставщика.

    > [!NOTE]
    > В поле **Номер сертификата** перечислены только те номера сертификатов TDS, для которых флажок **Закрыто** на странице **Подлежащие возмещению сертификаты** снят.

    В поле **Дата сертификата** показана дата сертификата. В поле **Тип счета** отображается тип счета, для которого получен номер сертификата TDS, а в поле **Имя** отображается имя счета.

5. В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода, для которого отображаются проводки TDS.
6. Выберите **Показать данные**, чтобы просмотреть проводки TDS, которые были разнесены в течение выбранного периода.

    На вкладке **Обзор** сетка в верхней области содержит следующие сведения о каждой проводке TDS, которая была разнесена для поставщика или клиента в течение выбранного периода:

    - **Ваучер** — код ваучера проводки TDS.
    - **Дата** — дата проводки TDS.
    - **Сумма** — сумма накладной, для которой рассчитан TDS.
    - **Сумма налога** — сумма налога TDS, рассчитанная для проводки.

7. Чтобы переместить отдельные проводки TDS из верхней сетки в нижнюю сетку, выберите проводки, а затем выберите **Включить**. Можно также выбрать **Включить все**, чтобы переместить все проводки TDS из верхней сетки в нижнюю сетку.

    Чтобы переместить отдельные проводки TDS или все проводки TDS из нижней сетки в верхнюю, используйте кнопку **Исключить** или **Исключить все**.

8. Выберите **Обновить**, чтобы обновить поля **Номер сертификата** и **Дата сертификата** для проводок TDS в нижней сетке.
10. Перейдите **Налог \> Косвенные налоги \> Подоходный налог \> Подлежащий возмещению сертификат** и выберите **Запрос** для просмотра обновленных строк проводок с новыми номерами сертификатов на странице **Проводки сертификата**.

    [![Страница "Проводки сертификата".](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
