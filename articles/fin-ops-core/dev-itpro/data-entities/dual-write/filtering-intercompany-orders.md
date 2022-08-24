---
title: Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов
description: В этой статье объясняется, как фильтровать внутрихолдинговые заказы, чтобы сущности Orders ("Заказы") и OrderLines ("Строки заказов") не синхронизировались.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f5b7831e103aaa219394099b79537bf0842d9be8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289291"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Фильтрация внутрихолдинговых заказов, чтобы исключить синхронизацию заказов и строк заказов

[!include [banner](../../includes/banner.md)]

Вы можете фильтровать внутрихолдинговые заказы, чтобы таблицы **Заказы** и **OrderLines** не синхронизировались. В некоторых сценариях сведения о внутрихолдинговых заказах не требуются в приложении взаимодействия с клиентами.

Каждая из стандартных таблиц Dataverse расширяется через ссылки на столбец **IntercompanyOrder**, а карты двойной записи изменяются, чтобы они ссылались на дополнительные столбцы в фильтрах. Таким образом, внутрихолдинговые заказы больше не синхронизируются. Этот процесс помогает избежать ненужных данных в приложении взаимодействия с клиентами.

1. Расширьте таблицу **Заголовки заказов на продажу CDS**, добавив ссылку на столбец **IntercompanyOrder**. Этот столбец заполняется только во внутрихолдинговых заказах. Столбец **IntercompanyOrder** доступен в таблице **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовков заказов на продажу CDS.":::

2. После развертывания пункта **Заголовки заказов на продажу CDS** столбец **IntercompanyOrder** доступен в сопоставлении. Примените фильтр, имеющий `INTERCOMPANYORDER == ""` в качестве строки запроса.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Диалоговое окно изменения запроса для заголовков заказов на продажу CDS.":::

3. Расширьте таблицу **Строки заказов на продажу CDS**, добавив ссылку на столбец **IntercompanyInventTransId**. Этот столбец заполняется только во внутрихолдинговых заказах. Столбец **InterCompanyInventTransId** доступен в таблице **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для строк заказов на продажу CDS.":::

4. После развертывания пункта **Строки заказов на продажу CDS** столбец **IntercompanyInventTransId** доступен в сопоставлении. Примените фильтр, имеющий `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Диалоговое окно изменения запроса для строк заказов на продажу CDS.":::

5. Повторите шаги 1 и 2, чтобы расширить таблицу **Заголовок счета на продажу V2** и добавить запрос фильтра. В этом случае используйте `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` в качестве строки запроса для фильтра.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовка счета на продажу V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Диалоговое окно изменения запроса для заголовка счета на продажу V2.":::

6. Повторите шаги 3 и 4, чтобы расширить таблицу **Строки счета на продажу V2** и добавить запрос фильтра. В этом случае используйте `INTERCOMPANYINVENTTRANSID == ""` в качестве строки запроса для фильтра.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Диалоговое окно изменения запроса для строк счета на продажу V2.":::

7. Таблица **Предложения с расценками** не имеет внутрихолдинговой связи. Если кто-то создает предложение с расценками для одного из внутрихолдинговых клиентов, можно использовать столбец **CustGroup**, чтобы поместить всех этих клиентов в одну группу клиентов. Можно расширить заголовок и строки, добавив столбец **CustGroup**, а затем отфильтровать, чтобы группа не включалась.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Страница сопоставления исходных данных с целевыми для заголовка предложения с расценками на продажу CDS.":::

8. После того как сущность **Предложения с расценками** расширена, примените фильтр, имеющий `CUSTGROUP != "<company>"` в качестве строки запроса.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Диалоговое окно изменения запроса для заголовка предложения с расценками на продажу CDS.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
