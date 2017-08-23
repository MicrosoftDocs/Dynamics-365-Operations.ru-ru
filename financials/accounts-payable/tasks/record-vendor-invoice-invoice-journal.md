--- 
title: "Регистрация накладной поставщика в журнале накладных"
description: "В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Регистрация накладной поставщика в журнале накладных

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку. Примеры этого типа накладной включают расходы на поставки или услуги.  В данной записи используется демонстрационная компания USMF.

1. Перейдите в раздел "Расчеты с поставщиками" > "Рабочие области" > "Запись накладной поставщика".
2. Щелкните "Новый журнал накладных".
3. Щелкните "Создать".
4. В поле "Имя" введите имя журнала или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. В поле "Описание" введите значение.
6. Щелкните "Строки".
    * В поле "Дата" введите дату разноски, в соответствии с которой будет обновлена главная книга.  
7. В поле "Счет" выберите счет поставщика.
8. В поле Накладная введите номер накладной.
9. В поле "Описание" введите значение.
10. В поле "Кредит" введите число.
11. В поле "Корр. счет" введите номер счета или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
    * По умолчанию в качестве значения "Налоговая группа" будет использоваться значение из счета поставщика.  
    * По умолчанию в качестве значения "Налоговая группа номенклатур" будет использоваться значение из счета ГК, указанного в поле "Корр. счет".  
    * Срок выполнения будет рассчитан на основании условий оплаты.  
    * По умолчанию в качестве значения "Скидка по оплате" будет использоваться значение из счета поставщика.  
12. Щелкните "Разнести".
13. Закройте страницу.

