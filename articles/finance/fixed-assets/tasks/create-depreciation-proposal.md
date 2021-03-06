---
title: Создание предложения по амортизации
description: В этом разделе описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013c768c8a016f399a27b1488ad0d5b339fdf7cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813587"
---
# <a name="create-a-depreciation-proposal"></a>Создание предложения по амортизации

[!include [banner](../../includes/banner.md)]

В этом разделе описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств. В этой задаче используется демонстрационная компания USMF и роль бухгалтера.


## <a name="create-a-depreciation-proposal"></a>Создание предложения по амортизации
1. В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Создать предложение по амортизации**.
2. В поле **Название журнала** выберите вариант в раскрывающемся меню.
3. В поле **Дата окончания** введите дату.

    - Установите флажок **Суммировать амортизацию**, чтобы объединить ежемесячные амортизации в одну строку журнала.  
    - Например, если значение параметра "До даты" — 31 марта 2015 г., формируется следующее сообщение: "Амортизация с 31 января 2015 г." Значение в поле **Дата** в предлагаемых строках журнала в этом случае устанавливается равным 31 марта 2015 г.  
    - Предложение по амортизации можно отфильтровать по основному средству, группе основных средств или другим критериям с помощью параметра **Фильтр**.  
    - При использовании формы **Создавать предложения по приобретению или амортизации для основных средств** можно предложить пакетную амортизацию. Этот способ рекомендуется для более крупных предложений, которые используют больше системных ресурсов. При выборе параметра партии можно по-прежнему выполнять другие задачи в это время. Если амортизация предлагается этим способом, она рассчитывается для моделей стоимости основных средств.  

4. Выберите **Создать журнал**.

## <a name="review-depreciation-entries"></a>Проверка записей амортизации
1. В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.
2. В списке найдите и выберите требуемую запись.
3. Выберите **Строки**.
4. Выберите **Разнести**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]