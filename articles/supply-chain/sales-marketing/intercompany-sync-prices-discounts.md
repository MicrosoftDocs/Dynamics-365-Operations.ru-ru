---
title: Синхронизация внутрихолдинговых цен и скидок
description: В этой теме описывается синхронизация цен и скидок для внутрихолдинговых заказов на продажу и заказов на покупку
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548483"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Синхронизация внутрихолдинговых цен и скидок

[!include [banner](../../includes/banner.md)]

Скидки и цены между внутрихолдинговыми заказами на продажу и на покупку всегда синхронизированы. Можно также синхронизировать цену и скидки с исходным заказом на продажу, чтобы одинаковые цены и скидки использовались во всех заказах. Для этого используется страница **Внутрихолдинговый**, доступная на вкладке **Общие** на странице списка **Все клиенты** — либо из модуля **Продажи и маркетинг**, либо из модуля **Закупки и источники**.

Поле **Цена и скидка** синхронизировано со строкой внутрихолдингового заказа на продажу. Это означает, что выбрав поля **Разрешить изменение цены** и **Разрешить изменение скидок** вы разрешаете изменение между внутрихолдинговыми заказами на продажу и на покупку. Изменение цены за единицу, единицы цены или накладных расходов продажи во внутрихолдинговом заказе на продажу определяет цену для строки внутрихолдингового заказа на покупку.

Если поля **Разрешить изменение цены** и **Разрешить изменение скидок** включены для внутрихолдингового заказа на продажу или внутрихолдингового заказа на покупку, можно изменить цену или скидку вручную для обоих заказов. В противном случае это действие выполнить невозможно.

Если поля **Разрешить изменение цены** и **Разрешить изменение скидок** не включены для внутрихолдингового заказа на продажу, вы не можете вручную изменять цену (или накладные расходы) или скидку для внутрихолдингового заказа на продажу.

Если поля **Разрешить изменение цены** и **Разрешить изменение скидок** не включены для внутрихолдингового заказа на покупку, вы не можете вручную изменять цену (или накладные расходы) или скидку для внутрихолдингового заказа на покупку.

Если поля **Разрешить изменение цены** и **Разрешить изменение скидок** включены как для внутрихолдингового заказа на покупку, так и для внутрихолдингового заказа на продажу, можно вносить изменения вручную для обоих заказов. Однако это может привести к ситуацию в которой обновления, выполняемые одним лицом, переопределяются обновлениями, внесенными другим лицом в другой компании для того же самого заказа.

> [!NOTE]
> Если поле **Цена и скидка** доступно как для внутрихолдингового заказа на покупку, так и для внутрихолдингового заказа на продажу, становится невозможно управлять ценообразованием.

Чтобы избежать подобных конфликтов лучше всего разрешать изменение цен и скидок только для внутрихолдингового заказа на покупку или для внутрихолдингового заказа на продажу. Это достигается путем включения полей **Разрешить изменение цен** и **Разрешить изменение скидок** в любом из этих заказов.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]