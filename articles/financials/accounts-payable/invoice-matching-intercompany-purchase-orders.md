---
title: "Сопоставление накладных и внутрихолдинговые заказы на покупку"
description: "Юридическое лицо — покупатель, участвующее во внутрихолдинговой торговой проводке, может быть настроено для использования сопоставления накладных по расчетам с поставщиками. В этом случае, чтобы внутрихолдинговые накладные поставщиков могли быть разнесены, должны быть удовлетворены требования разноски как для внутрихолдинговой торговли, так и для сопоставления накладных по расчетам с поставщиками."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07c101b886d33fa5fc9e8129230ca270f48c5217
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Сопоставление накладных и внутрихолдинговые заказы на покупку

[!include[banner](../includes/banner.md)]


Юридическое лицо — покупатель, участвующее во внутрихолдинговой торговой проводке, может быть настроено для использования сопоставления накладных по расчетам с поставщиками. В этом случае, чтобы внутрихолдинговые накладные поставщиков могли быть разнесены, должны быть удовлетворены требования разноски как для внутрихолдинговой торговли, так и для сопоставления накладных по расчетам с поставщиками.

В примерах из этого раздела используются следующая схема для внутрихолдинговой торговли:
-   Компания "Fabrikam Закупка" — это юридическое лицо — покупатель.
-   Компания "Fabrikam Продажи" — это юридическое лицо — продавец.
-   Клиент 4020 существует в компании Fabrikam Продажи.
-   Поставщик 3024 существует в компании Fabrikam Закупка.
-   В "Fabrikam Закупка" задана внутрихолдинговая информация для поставщика 3024. "Fabrikam Продажи" указана как компания-клиент, а клиент 4020 определен как счет клиента, соответствующий юридическому лицу "Fabrikam Закупка".
-   В "Fabrikam Продажи" задана внутрихолдинговая информация для клиента 4020. "Fabrikam Закупка" указана как компания-поставщик, а поставщик 3024 определен как счет клиента, соответствующий юридическому лицу "Fabrikam Продажи".

В этих примерах используются следующие настройки для сопоставления накладных по расчетам с поставщиками для компании "Fabrikam Закупка":
-   На странице "Параметры модуля расчетов с поставщиками" выбран параметр "Включить проверку сопоставления накладных".
-   На странице "Параметры модуля расчетов с поставщиками" в поле "Разнести накладную с несоответствиями" выбрано "Требуется утверждение".
-   Допустимое процентное отклонение цены компании для юридического лица составляет 2 процента.

## <a name="example-price-matching-and-intercompany-trade"></a>Пример. Сопоставление цены при внутрихолдинговой торговле
Чистые суммы для внутрихолдинговой накладной поставщика и внутрихолдинговая накладная клиента должны быть равны. Это требование имеет больший приоритет, чем любые применимые утверждения сопоставления накладных или процентные отклонения цены. Предположим для примера, что вы выполняете следующие действия.
1.  В "Fabrikam Закупка" вы создаете заказ на продажу SO888 для клиента 4020. В "Fabrikam Закупка" автоматически создается внутрихолдинговый заказ на покупку ICPO222 для поставщика 3024, а в "Fabrikam Продажи" автоматически создается заказ на продажу ICSO888.
2.  В "Fabrikam Продажи" вы регистрируете факт получения номенклатур и разносите отборочную накладную. Статус заказа на продажу ICSO888 изменяется на "Доставлено". Статус заказа на покупку ICPO222 изменяется на "Получено".
3.  В "Fabrikam Продажи" вы выполняете обновление накладной для ICSO888. Цена за единицу измерения равна 0,45, при этом обновляются 100 номенклатур.
4.  В "Fabrikam Закупка" вы создаете накладную для ICPO222. Вы случайно изменили чистую цену с 45,00 на 54,00. Отображается значок, указывающий, что цена превышает допустимое отклонение цены в 2%.
5.  На странице "Сведения о сопоставлении накладных" выберите параметр для того, чтобы одобрить разноску с соответствующими несоответствиями. На странице "Накладная поставщика" щелкните OK. Если бы накладная поставщика не была внутрихолдинговой накладной поставщика, разноска была бы успешной. Однако, поскольку вы работаете с внутрихолдинговой накладной поставщика, не удается выполнить разноску. При внутрихолдинговой торговле итоговые суммы накладной для внутрихолдингового заказа на продажу должны быть равны итоговым суммам накладной для соответствующего внутрихолдингового заказа на покупку. Чтобы решить эту проблему, вам необходимо изменить чистую цену по накладной, изменив чистую цену в накладной, изменив чистую цену обратно на значение по умолчанию: 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Пример. Сопоставление количества при внутрихолдинговой торговле
Количества внутрихолдингового заказа на покупку и внутрихолдингового заказа на продажу должны быть равны. Это требование имеет больший приоритет, чем любые применимые утверждения сопоставления накладных. В этом примере используется следующие дополнительные условия внутрихолдинговой торговли:
-   В "Fabrikam Закупка" политика действий по заказу на покупку для поставщика 3024 настроена для автоматической разноски как исходной накладной клиента, так и внутрихолдинговой накладной поставщика.

В этом примере используются следующие дополнительные настройки при сопоставлении накладных по расчетам с поставщиками для компании "Fabrikam Закупка":
-   На странице "Группы номенклатурных моделей" для группы моделей, которую использует номенклатура B-R14, выбран параметр "Требовать отборочную накладную".
-   Количество в наличии для номенклатуры B-R14 равно 0 (нуль).

Предположим для примера, что вы выполняете следующие действия.
1.  В "Fabrikam Закупка" вы создаете заказ на продажу SO999 для клиента 4020. Заказ содержит одну номенклатуру строки: 100 батареек (номенклатура B-R14) по цене за единицу 1,00 каждая. В "Fabrikam Закупка" автоматически создается внутрихолдинговый заказ на покупку ICPO333 для поставщика 3024, а в "Fabrikam Продажи" автоматически создается заказ на продажу ICSO999.
2.  В "Fabrikam Продажи" вы выполняете обновление накладной для ICSO999. Разноску не удается выполнить, так как номенклатура отсутствует в запасах и еще не была получена. Таким образом, финансовые сведения не могут быть обновлены.
3.  В "Fabrikam Продажи" зарегистрируйте полученные номенклатуры и разнесите отборочную накладную для ICSO999. Поступление продуктов для ICPO333 автоматически разносится в "Fabrikam Закупка". В "Fabrikam Закупка" полученное количество для номенклатуры B-R14 изменяется на 100.
4.  В "Fabrikam Продажи" вы выполняете обновление накладной для ICSO999. Разноска успешно выполняется в обоих юридических лицах. В "Fabrikam Закупка" количество, приобретенное для номенклатуры B-R14, изменяется на 100.





