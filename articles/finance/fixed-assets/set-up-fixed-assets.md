---
title: Настройка основных средств
description: В этом разделе приводится обзор настройки модуля "Основные средства".
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8196ddc879df1f398aabef0c1c4064bf0d4fff2c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771928"
---
# <a name="set-up-fixed-assets"></a>Настройка основных средств

[!include [banner](../includes/banner.md)]

В этом разделе приводится обзор настройки модуля **Основные средства**.

## <a name="overview"></a>Обзор

Параметры управляют общим поведением в модуле "Основные средства".

Группы ОС позволяют группировать активы и задавать атрибуты по умолчанию для каждого актива, назначенного группе. Книги назначаются группам ОС. Книги отслеживают финансовую стоимость основного средства с течением времени с помощью конфигурации амортизации, определенной в профиле амортизации.

Фиксированные средства при создании назначаются группе. По умолчанию книги, назначенные для группы ОС, затем назначаются основному средству. Книги, которые настроены для разнесения в главную книгу, связаны с профилем разноски. Счета ГК определяются для каждой книги в профиле разноски и используются при разноске проводок основных средств.

![Компоненты основных средств](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Профили амортизации

Сначала требуется настроить профили амортизации. В профиле амортизации настраивается, как стоимость актива амортизируется с течением времени. Необходимо указать метод амортизации, год амортизации (календарный год или финансовый год) и частоту амортизации. Дополнительные сведения см. в разделе [Настройка и создание профилей амортизации](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Книги

После настройки профилей амортизации необходимо создать требуемые книги для своих основных средств. Каждая книга отслеживает независимый финансовый жизненный цикл средства. Книги можно настроить для разноски связанных проводок в главную книгу. Эта конфигурация используется по умолчанию, поскольку она обычно используется для корпоративной финансовой отчетности. Книги, которые не будут разноситься в ГК, разносятся только в субкнигу основных средств и обычно используются для целей налоговой отчетности.

Основной профиль амортизации назначен каждой книге. Книги также имеют альтернативный или резервный профиль амортизации, если такой тип профиля применим. Для автоматического включения журнала основных средств в выполнения амортизации необходимо включить параметр **Расчет амортизации**. Если этот параметр не включен для актива, предложение по амортизации пропускает этот актив.

Можно также настроить производные книги. Определенные производные проводки разносятся относительно производных книг как точная копия основной проводки. Поэтому производные проводки обычно настраиваются для приобретения и списания, а не для проводок амортизации. Дополнительные сведения см. в разделе [Настройка моделей стоимости](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Профили разноски по ОС

После настройки книги можно создать профиль разноски. Профиль разноски должен быть определен по книге, но его можно также указать на более детальном уровне. Например, можно определить профиль разноски для сочетания книги и группы основных средств или даже для отдельной книги основного средства. По умолчанию счета ГК, которые определены, используются для проводок с основными средствами.

Необходимо определить счета ГК, которые используются во время процессов выбытия, как для выбытия путем продажи, так и для выбытия при списании. Во время выбытия проводки по основным средствам, которые были ранее разнесены, реверсируются из исходных счетов. Чистые суммы затем переносятся на соответствующий счет прибылей и убытков для выбытия ОС. Чтобы помочь гарантировать правильное реверсирование проводок, необходимо настроить счета для каждого типа проводки, используемого в бизнесе. Счетом ГК должен быть исходный счет, заданный для данного типа проводки в профиле разноски, а корр. счетом должен быть ваш счет прибылей и убытков для выбытия. Исключением является остаточная стоимость. В этом случае и счет ГК, и корр. счет должны быть установлены на счет прибылей и убытков для выбытия. Дополнительные сведения см. в разделе [Настройка профилей разноски основных средства](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Группы ОС

Поле **Группа ОС** — единственное обязательное поле при создании основного средства. Значение этого поля определяет значение по умолчанию нескольких информационных полей для актива. Книги настроены так, что книга по умолчанию назначается каждому активу в группе. Таким образом атрибуты, которые заданы для книг учета, могут относиться к конкретным группам ОС. Эти атрибуты включают строк службы и соглашение по амортизации.

Можно также определить амортизационные премии или амортизационную премию для конкретного сочетания из группы ОС и книги. Необходимо назначить приоритет для амортизационной премии, чтобы указать порядок вычисления премий, если книге назначены несколько премий. Дополнительные сведения см. в разделе [Настройка групп основных средств](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Наименования журналов

На странице **Наименования журналов** необходимо создать наименования журналов, которые должны использоваться с журналом основных средств. Необходимо задать в поле **Тип журнала** значение **Разнести основные средства**. Задайте поле **Серии ваучеров** таким образом, чтобы наименования журналов использовались для журнала основных средств. Журналы основных средств не должны использовать настройку **Только один код ваучера**, так как уникальный код ваучера необходим для нескольких автоматизированных процессов, таких как перемещения и разделения.

## <a name="fixed-asset-parameters"></a>Параметры основных средств

Последний шаг — обновить параметры основных средств.

Поле **Порог капитализации** определяет средства, которые амортизируются. Если строка покупки выбрана в качестве основного средства, но она не достигает указанного порога капитализации, основное средство создается или обновляется, но для параметра **Расчет амортизации** устанавливается значение **Нет**. Поэтому средство не будет автоматически амортизироваться как часть предложений по амортизации.

Один из важных параметров называется **Автоматически создать суммы переоценки амортизации со списанием**. При выборе варианта **Да** амортизация средства автоматически корректируется на основе настроек амортизации в момент выбытия средства. Другой вариант позволяет вычитать скидки по оплате от суммы приобретения при приобретении основных средств с помощью накладной поставщика.

На экспресс-вкладке **Заказы на покупку** вы можете настроить, как создавать активы как часть процесса покупки. Первый параметр называется **Разрешить приобретение активов из модуля "Покупки"**. Если задать для этого параметра значение **Да**, приобретение актива происходите при разноске накладной. Если задать для этого параметра значение **Нет**, по-прежнему можно поместить ОС в заказ на покупку (PO) и накладную, но приобретение не будет разноситься. Разноска должна выполняться как отдельный шаг из журнала основных средств. Параметр **Создавать актив при разноске поступления продуктов или накладной** позволяет создавать новые активы "на лету" во время разноски. Таким образом, актив не должен быть настроен как основное средство перед выполнением транзакции. Последний параметр, **Проверка создания основных средств при вводе строки**, применяется только для заявок на покупку.

Можно настроить коды причин, чтобы они требовались для изменений основных средств или для специфических проводок основных средств.

Наконец, на вкладке **Номерные серии** задаются номерные серии для основных средств. Номерная серия **Основные средства** может быть переопределена номерной серией **Группа основных средств**, если она была определена.

Дополнительные сведения см. в разделе [Создание основного средства](tasks/create-fixed-asset.md).