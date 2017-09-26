--- 
title: "Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022"
description: "В этой процедуре показано, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16c2af862a73047a2e6ebdc056275392fa8a0d93
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022. 

В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.

Это пятая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности. Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="create-payment-lines"></a>Создание строк платежа
1. Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".
2. Щелкните "Создать".
3. В списке пометьте выбранную строку.
4. В поле "Имя" введите или выберите значение.
5. Щелкните "Строки".
6. Щелкните "Предложение по оплате".
7. Щелкните "Создать предложение по оплате".
8. Разверните раздел "Записи для добавления".
9. Щелкните "Фильтр".
10. В списке выберите строку для таблицы "Поставщики" и поля "Счет поставщика".
11. В поле "Критерии" введите или выберите значение.
    * Можно применить любые критерии для выбора проводок поставщиков для оплаты, для данного примера в качестве счета поставщика используется DE-001.  
12. Нажмите кнопку "OК".
13. Нажмите кнопку "OК".
14. Щелкните "Создать платежи".

## <a name="generate-an-iso20022-payment-file"></a>Создание файла платежа ISO20022

