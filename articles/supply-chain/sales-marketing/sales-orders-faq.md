---
title: Часто задаваемые вопросы о заказах на продажу
description: На этой странице рассматриваются часто задаваемые вопросы при работе с заказами на продажу в Dynamics 365 Supply Chain Management.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477407"
---
# <a name="sales-order-faqs"></a>Вопросы и ответы по заказам на продажу

На этой странице рассматриваются часто задаваемые вопросы при работе с заказами на продажу в Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Можно ли связать заказ на покупку с заказом на продажу для удовлетворения спроса?

Можно создать заказ на покупку из заказа на продажу. Дополнительные сведения см. в разделе [Создание заказа на покупку из заказа на продажу](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Можно ли отменить или удалить заказ на возврат или заказ на продажу?

Можно отменить только заказы на продажу и заказы на возврат, которые находятся в состоянии *Создано*. Дополнительные сведения см. в разделе [Отмена заказов на возврат](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Можно ли восстановить удаленный заказ на продажу, по которому выставлена накладная?

Если заказ на продажу, по которому выставлена накладная, был удален по ошибке, его можно восстановить или просмотреть сведения о нем.

Перейдите **Счета клиента \> Транзакции \> Исходный документ \> Показать подробные сведения**. Найдите накладную, которую вы ищете, и выберите ее для просмотра подробных сведений. Эти сведения включают ссылку на заказ на продажу. Кроме того, с этой страницы должна иметься возможность доступа к сведениям о заказах на продажу.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Как удалить потерянные записи заказов на продажу?

Чтобы удалить потерянные записи заказов на продажу, запустите периодическое задание *Удаление заказа на продажу*, перейдите к одному из следующих мест:

- Продажи и маркетинг \> Периодические задачи \> Очистка \> Удалить заказы на продажу
- Розничная торговля и коммерция \> ИТ розничной торговли и коммерции \> Очистка \> Удалить заказы на продажу

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Существует ли способ расчета комиссий по накладным, которые уже были разнесены?

Supply Chain Management в настоящее время не поддерживает расчет комиссий для разнесенных накладных.
