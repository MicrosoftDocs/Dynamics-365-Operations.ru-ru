---
title: Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов
description: В этой теме описывается порядок фильтрации внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701041"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов

[!include [banner](../../includes/banner.md)]

Вы можете фильтровать внутрихолдинговые заказы, чтобы исключить синхронизацию сущностей **Заказы** и **OrderLines**. В некоторых сценариях сведения о внутрихолдинговых заказах не являются обязательными в приложении взаимодействия с клиентами.

Каждая из стандартных сущностей Common Data Service расширяется со ссылками на поле **IntercompanyOrder**, а карты двойной записи изменяются для ссылки на дополнительные поля в фильтрах. В результате внутрихолдинговые заказы больше не синхронизируются. Этот процесс позволяет избежать ненужных данных в приложении взаимодействия с клиентами.

1. Добавьте ссылку на **IntercompanyOrder** в **Заголовки заказов на продажу CDS**. Оно заполняется только для внутрихолдинговых заказов. Поле **IntercompanyOrder** доступно в **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, SalesOrderHeader":::
    
2. После развертывания пункта **Заголовки заказов на продажу CDS** поле **IntercompanyOrder** доступно в сопоставлении. Примените фильтр с `INTERCOMPANYORDER == ""` в качестве строки запроса.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Заголовки заказов на продажу, изменение запроса":::

3. Добавьте ссылку на **IntercompanyInventTransId** в **Строки заказа на продажу CDS**.  Оно заполняется только для внутрихолдинговых заказов. Поле **InterCompanyInventTransID** доступно в **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, SalesOrderLine":::

4. После развертывания пункта **Строки заказов на продажу CDS** поле **IntercompanyInventTransId** доступно в сопоставлении. Примените фильтр с `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Строки заказа на продажу, изменить запрос":::

5. Разверните **Заголовок накладной по продаже V2** и **Строки накладной по продаже V2** таким же образом, как разворачивали сущности Common Data Service на шагах 1 и 2. Затем добавьте запросы фильтра. Строка фильтра для сущности **Заголовок накладной по продаже V2** равна `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Строка фильтра для сущности **Строки накладной по продаже V2** равна `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Сопоставить промежуточные данные с целевыми, Заголовки накладной по продаже":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Заголовки накладной по продаже, изменение запроса":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Строки накладной по продаже, изменение запроса":::

6. Сущность **Предложения с расценками** не имеет внутрихолдинговой связи. Если кто-то создает предложение с расценками для одного из внутрихолдинговых клиентов, можно поместить всех этих клиентов в одну группу клиентов, используя поле **CustGroup**.  Заголовок и строки можно развернуть, добавив поле **CustGroup**, а затем выполнить фильтрацию, чтобы не включать эту группу.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Сопоставить промежуточные данные с целевыми, Заголовок предложения с расценками по продаже":::

7. После того как сущность **Предложения с расценками** развернута, примените фильтр со строкой запроса `CUSTGROUP !=  "<company>"`.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Заголовок предложения с расценками по продажам, правка запроса":::
