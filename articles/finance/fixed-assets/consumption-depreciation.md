---
title: Амортизация потребления
description: Эта статья содержит обзор метода амортизации "Потребление".
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187322"
---
# <a name="consumption-depreciation"></a>Амортизация потребления

[!include [banner](../includes/banner.md)]

Эта статья содержит обзор метода амортизации "Потребление".

При настройке профиля амортизации основных средств и выборе значения **Потребление** в поле **Метод** на странице **Профили амортизации** основные средства назначаются этому профилю амортизации на основе их использования. Вы не должны настроить проценты и интервалы на странице **Профили амортизации**. После создания профиля амортизации, использующего метод "Потребление", этот метод можно настроить различными способами.

## <a name="set-up-and-use-consumption-depreciation"></a>Настройка и использование амортизации потребления
1.  На странице **Профили амортизации** создайте профиль амортизации. Для выполнения расчетов потребления профиль амортизации должен включать код и название, а в поле **Метод** должно быть выбрано значение **Потребление**.
2.  На странице **Коэффициенты выпуска/пробега** настройте факторы потребления. Каждый коэффициент потребления должен иметь код и название и коэффициент потребления, который указан как количество или как процент.
3.  На странице **Единицы измерения потребления** настройте единицы измерения потребления. Каждая единица потребления должна иметь код и название. Единицы измерения амортизации используются для расчета амортизации по потреблению на странице **Амортизация потребления**. Примерами единиц измерения являются кг, км и час.
4.  На странице **Основные фонды** настройте индивидуальные основные фонды. Для каждого основного средства выберите модели стоимости и журналы амортизации, имеющие методы амортизации. Необходимо настроить модели стоимости или журналы амортизации для амортизации потребления, если какие-либо основные средства используют профили амортизации на основе метода амортизации "Потребление". Эта настройка выполняется на вкладке **Амортизация** страницы **Модели стоимости** или на экспресс-вкладке **Общие** страницы **Профиль амортизации**. Одну и ту же модель стоимости можно использовать для нескольких основных средств. Методы амортизации являются частью модели стоимости или журнала амортизации, которые выбираются для каждого основного средства. Невозможно добавлять или изменять методы непосредственно на странице **Основные средства**. Вы можете изменить профили амортизации только на странице **Журналы амортизации**.
5.  На странице **Модели стоимости** или **Журналы амортизации** в группе полей **Амортизация потребления** введите сведения в следующих полях:
    -   Коэффициент выпуска/пробега
    -   Единица измерения
    -   Единица измерения амортизации
    -   Оценка потребления

    В поле **Разнесенное потребление** отображается амортизация потребления в единицах, которые уже были разнесены для комбинации основных средств и модели стоимости или для журнала амортизации. Значение этого поля нельзя изменить вручную.

## <a name="examples"></a>Примеры
### <a name="example-1"></a>Пример 1

Следующий коэффициент выпуска/пробега настроен для 31 января:

-   Количество равно 1 000.
-   Цена за единицу измерения амортизации, указанная для основных средств, равна 1,5.

Предложение амортизации от 31-го января выглядит следующим образом: Количество × Единица измерения амортизации 1 000× 1,5 = 1 500 Если коэффициент, который определен для основных средств, является процентным коэффициентом, количество, оцененное в поле **Оценка потребления** для модели стоимости основных средств, умножается на процент, который настроен для выбранной даты окончания. Получающееся количество затем предлагается как количество амортизации за период.

### <a name="example-2"></a>Пример 2

Следующий коэффициент для амортизации потребления настроен для 31 января:

-   Процентное отношение равно составляет 10 процентов.
-   Цена за единицу измерения амортизации, указанная для основных средств, равна 1,5.
-   Предполагаемое количество основного средства равно 2 000.

Предложение амортизации на 31-е января выглядит следующим образом: Оцененное количество × Процент × Единица измерения амортизации 2 000 × 0,10 × 1,5 = 300


