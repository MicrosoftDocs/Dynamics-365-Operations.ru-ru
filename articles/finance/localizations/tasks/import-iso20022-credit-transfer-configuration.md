---
title: Импорт конфигурации кредитового перевода ISO20022
description: Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175016"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Импорт конфигурации кредитового перевода ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам. Немецкий формат кредитного перевода ISO 20022 используется в качестве примера. Эта процедура может использоваться для других доступных форматов электронной отчетности. 

Эта задача была создана с использованием демонстрационных данных компании DEMF, но можно использовать любую компанию с демонстрационными данными для выполнения этой задачи.

Это первая из пяти задач, которые совместно иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности. Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.

1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. В списке доступных поставщиков конфигурации выберите Microsoft.
3. Щелкните "Установить как активное".
4. Щелкните "Репозитории".
5. Щелкните Открыть.
6. Щелкните "Показать фильтры".
7. Примените следующие фильтры: введите значение фильтра "Перенос кредита ISO20022 (DE)" в поле "Имя конфигурации", используя оператор фильтра "начинается с".
    * Либо найдите конфигурацию в списке, выберите и переместите ее в задачу импорта.  
8. Нажмите кнопку Импорт.
    * Если кнопка "Импорт" недоступна, это означает, что данная конфигурация уже была импортирована.  
9. Щелкните Да.
