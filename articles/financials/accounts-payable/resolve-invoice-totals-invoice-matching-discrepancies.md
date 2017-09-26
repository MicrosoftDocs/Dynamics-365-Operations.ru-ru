---
title: "Устранение несоответствий во время сопоставления итогов по накладным"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 8ccc1af0e1bd7909b7810d359a916849ecc1a709
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Устранение несоответствий во время сопоставления итогов по накладным

[!include[banner](../includes/banner.md)]




Один из типов валидации сопоставления накладных — это сопоставление итогов по накладным. Чтобы указать, что система должна выполнять сопоставление итогов по накладным, на странице **Параметры модуля расчетов с поставщиками** на вкладке **Проверка накладной** установите параметр **Сопоставлять итоги по накладным** в значение **Да**. 

Сопоставление итогов накладных можно использовать, чтобы гарантировать, чтобы итоги накладных не отличаются от ожидаемых сумм более чем на допустимое отклонение. На странице **Сведения о сопоставлении итогов по накладнымs** сравнивается шесть итогов. Если какой-либо из итогов отличается от ожидаемого соответствующего итога по заказа ну покупку, несоответствие помечается флагом. 

Чтобы просмотреть накладную, в которой обнаружены несоответствия при сопоставлении итогов, в рабочей области **Запись накладной поставщика** щелкните плитку **Накладные, ожидающие обработки**. Затем на панели операций на вкладке **Просмотр** щелкните **Сведения о сопоставлении**. Если при сопоставлении обнаружены несоответствия, рядом с суммой накладной отображаются значки-предупреждения. Просмотреть дополнительные сведения об итогах можно, просмотрев сведения о сопоставлении итогов по накладной. 

После выявления расхождения может возникнуть необходимость обратиться к поставщику, если вы считаете, что данные в накладной ошибочны. В зависимости от результата переговоров с поставщиком вы можете выполнить одно из следующих действий:

-   Принять расхождение в цене и разнести накладную с расхождениями сопоставления. Ваша система может быть настроена так, что разноска при наличии расхождений сопоставления будет требовать утверждения. В этом случае вы должны утвердить расхождение сопоставления; при желании можно ввести комментарий к утверждению. После этого накладную можно будет разнести.
-   Изменить сумму накладной на ожидаемую и разнести накладную.
-   Запросить у поставщика полный зачет и новую, исправленную накладную.

Дополнительные сведения см. в разделе [Рассмотрение и разрешение исключений](tasks/research-resolve-exceptions.md).


