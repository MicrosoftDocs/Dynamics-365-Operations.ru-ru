---
title: Создание налогового платежа
description: Процедура задания сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aec00c2fb657f0b4074063ef7acad5f4372ebca
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646343"
---
# <a name="create-a-sales-tax-payment"></a>Создание налогового платежа

[!include [banner](../../includes/banner.md)]

Процедура задания сопоставления и разноски налога сопоставит налоговые сальдо в налоговых счетах и корреспондирует их со счетом сопоставления налогов за определенный период.

1. Перейдите в раздел **Налог > Объявления > Налог > Сопоставить и разнести налог**.
2. В поле **Период сопоставления** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
3. В списке перейдите по ссылке в выбранной строке.
4. В поле **Дата начала** введите дату.
    * Если параметр **Включать коррекции** не выбран на странице **Параметры главной книги**, сопоставление может быть обработано для разных версий. Оригинал — это первое сопоставление за интервал периода и может быть обработано только один раз за интервал периода. Последние корректировки сопоставят налоговые проводки, которые были разнесены после создания исходной версии.   
5. В поле **Дата проводки** введите дату.
6. Щелкните **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]