---
title: Импорт конфигурации безакцептного списания ISO20022
description: Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам клиентов.
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
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185758"
---
# <a name="import-iso20022-direct-debit-configuration"></a>Импорт конфигурации безакцептного списания ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам клиентов. Эта процедура использует формат прямого дебетования ISO 20022 в качестве примера. 



Эта процедура была создана с использованием демонстрационных данных компании DEMF, но можно использовать любую компанию с демонстрационными данными для этих целей.



Это первая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.

1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. В списке доступных поставщиков конфигурации выберите Microsoft.
3. Щелкните "Установить как активное".
4. Щелкните "Репозитории".
5. Щелкните Открыть.
6. Щелкните "Показать фильтры".
7. Примените следующие фильтры: введите значение фильтра "Прямое дебетование ISO20022 (DE)" в поле "Имя конфигурации", используя оператор фильтра "начинается с".
    * Если требуется, можно найти конфигурацию в списке, выбрать ее и пропустить этот шаг.  
8. Нажмите кнопку Импорт.
    * Если кнопка "Импорт" недоступна, это означает, что данная конфигурация уже была импортирована.  
9. Щелкните Да.
