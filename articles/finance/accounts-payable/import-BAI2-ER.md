---
title: Настройка расширенного импорта банковской выверки с помощью электронной отчетности
description: В этой теме объясняется, как использовать электронную отчетность для настройки расширенного процесса импорта банковской выверки.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 30530a9870ba2ff0546237d2698d1675afa78104
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770204"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Настройка расширенного импорта банковской выверки с помощью электронной отчетности

[!include [banner](../includes/banner.md)]

Функция расширенной банковской выверки позволяет импортировать электронные банковские выписки и автоматически выверять их с банковскими проводками в Microsoft Dynamics 365 Finance. В этой теме объясняется, как настроить функцию импорта для банковских выписок. Настройка импорта банковской выписки зависит от формата электронной банковской выписки. Microsoft Dynamics 365 Finance поддерживает три формата банковской выписки: ISO20022, MT940 и BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Настройка конфигурации электронной отчетности

1. Перейдите в раздел **Рабочие области \> Электронная отчетность**.
2. На плитке поставщика конфигурации **Microsoft** выберите **Репозитории**.
3. Выберите **Глобальный**, затем выберите **Открыть**.
4. Если необходимо установить соединение с репозиторием, выберите синюю ссылку в диалоговом окне.
5. В списке конфигураций найдите **Модель банковской выписки \> Модель банковской выписки BAI2**.
6. Выберите формат **BAI2**.
7. На экспресс-вкладке **Версии** выберите последнюю версию, затем выберите **Импорт**.

## <a name="set-up-the-bank-statement-format"></a>Настройка формата банковской выписки

1. Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Настройка расширенной банковской выверки \> Формат банковской выписки**.
2. Выберите **Создать**.
3. Задайте поля **Формат выписки** и **Имя**.
4. Установите флажок **Универсальный электронный формат импорта**.
5. Задайте в поле **Конфигурация формата импорта** формат **BAI2**.

## <a name="set-up-the-bank-account"></a>Настройка банковского счета

1. Перейдите в раздел **Управление банком и кассовыми операциями \> Банковские счета \> Банковские счета**.
2. Откройте банковский счет.
3. На экспресс-вкладке **Выверка** задайте для параметра **Расширенная банковская выверка** значение **Да**.
4. Выберите в поле **Формат выписки**, созданный ранее формат **BAI2**.

## <a name="import-the-bank-statement"></a>Импорт банковской выписки

1. Перейдите к **Управление банком и кассовыми операциями \> Выверка банковской выписки \> Банковские выписки**.
2. В верхней части страницы **Банковские выписки** выберите **Импортировать выписку**.
3. Задайте в поле **Банковский счет** банковский счет из выписки.
4. Выберите в поле **Формат выписки**, созданный ранее формат **BAI2**.
5. Выберите **Обзор** и выберите файл **BAI**.
6. Выберите **Отправить**.
7. Выберите **ОК**, чтобы импортировать выбранный файл.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Примеры форматов банковской выписки и технических макетов
Ниже приводятся примеры определений технических макетов для расширенных файлов импорта банковской выписки и трех связанных примеров файлов банковской выписки: [Примеры файлов импорта](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Определение технического макета                             | Пример файла банковской выписки          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

