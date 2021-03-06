---
title: Обработка журнала распределения ГК
description: В этой теме объясняется, как обрабатывать запросы распределения в Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834432"
---
# <a name="process-ledger-allocation-journal"></a>Обработка журнала распределения ГК

[!include [banner](../../includes/banner.md)]

В этой теме объясняется, как обрабатывать запросы распределения. Страница "Обработать запрос на распределение" используется для создания журнала распределения, который можно просмотреть и утвердить перед разноской в главную книгу или можно сразу же разнести в главную книгу. Прежде чем создавать журнал распределений, должно быть как минимум одно активное правило распределения книги учета. В этой задаче используется демонстрационная компания USMF.

1. В области переходов выберите **Модули > Главная книга > Распределения > Обработать запрос на распределение**.
2. В поле **Правило** выберите требуемую запись в раскрывающемся меню.
3. В поле **Состояние на дату** введите дату.

    - **Состояние на дату** очень важно, когда книга учета является источником данных для правила. Эта дата определяет, какие сальдо главной книги необходимо включить для распределения.  
    - В поле **Нулевое исходное значение** выберите **Стоп**. При этом будет остановлен процесс распределения и отобразится сообщение, указывающее на выбор нулевой исходной суммы.  

4. В поле **Параметры предложения** выберите **Только предложение**. Выберите **Только предложение** для просмотра и при необходимости утвердите результат в журналах распределения до разноски распределения в главной книге.  
5. В поле "Дата разноски ГК" введите дату.
6. Нажмите **ОК**.
7. В области переходов выберите **Модули > Главная книга > Распределения > Журналы распределения**.
8. Выберите **Строки**.
9. Выберите **Разнести**.
10. Выберите **Разнести**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]