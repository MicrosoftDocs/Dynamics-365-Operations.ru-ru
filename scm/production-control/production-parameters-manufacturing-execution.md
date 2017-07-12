---
title: "Параметры производства в модуле \"Управление производством\""
description: "В этой теме содержится информация о настройке параметров производства в модуле \"Управление производством\"."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c8868c1b09b28f8098dfd7a4983c8bf0cce51a0c
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="production-parameters-in-manufacturing-execution"></a>Параметры производства в модуле "Управление производством"

[!include[banner](../includes/banner.md)]

В этой теме содержится информация о настройке параметров производства в модуле "Управление производством".

Модуль **Управление производством** предназначен главным образом для использования производственными компаниями. Он может использоваться для регистрации времени и потребления номенклатуры для производственных заданий или проектов. Прежде чем начинать использовать модуль "Управление производством" для регистрации заданий, необходимо настроить различные производственные параметры, определяющие порядок и время разноски регистрационной информации в процессе производства. Настройка параметров производства влияет на управление запасами, управление производством и расчет затрат.

Прежде чем работники начнут делать регистрации в производственных заданиях, следует тщательно продумать все настройки на странице **Параметры производства**. Щелкните **Управление производством** &gt; **Настройка** &gt; **Управление производством** &gt; **Значения по умолчанию для производственного заказа**. Если в вашей компании используется функция работы с несколькими сайтами, возможно, имеет смысл настроить разные параметры производства для каждого сайта. Параметры для интеграции с модулем **Производство** настраиваются на следующих вкладках страницы **Параметры производства**:

- **Общие** — общие значения параметров для производственных заданий в модуле "Управление производством".
- **Запуск** — параметры, используемые при запуске производственных операций.
- **Операции** — параметры, применяемые к производственным операциям и обратной связи по операциям в процессе производства.
- **Приемка** — параметры, используемые на последней операции производственного заказа, когда номенклатуры учитываются как принятые.
- **Проверка количества** — параметры, используемые для проверки начального количества и количества по обратной связи для производственных заказов.

## <a name="types-of-production-jobs"></a>Типы производственных заданий
На вкладке **Операции** необходимо выбрать типы производственных заданий, которые требуют регистрации на странице **Регистрация задания**.

Как правило, работники выполняют регистрацию заданий настройки и процессов. Однако если применяется планирование заданий, можно выбрать другие типы заданий, которые должны регистрироваться работниками при обработке производственного заказа. Например, можно потребовать регистрации в заданиях на транспортировку.

> [!IMPORTANT]
> Убедитесь, что выбраны все необходимые типы заданий. В противном случае задания могут быть недоступны для регистрации на странице **Регистрация задания**. Выбранные типы должны соответствовать вариантам, выбранным в столбце **Управление заданиями** на вкладке **Настройка** страницы **Маршрутные группы** (**Управление производством** &gt; **Настройка** &gt; **Маршруты** &gt; **Маршрутные группы**).

Если в маршрутной группе выбрано **Управление заданиями**, этот тип задания учитывается как принятый в производственном заказе, когда задание учитывается как принятое в модуле "Управление производством". Когда все типы заданий, для которых выбрано **Управление заданиями**, учтены как принятые в операции, модуль "Управление задания" учитывает эту операцию как принятую.

> [!NOTE]
> Некоторые типы заданий можно учитывать вручную посредством журналов производства. В этом случае выберите **Управление заданиями** для типа задания, но не выбирайте тип задания для регистрации на вкладке **Операции** на странице **Параметры производства** в модуле "Управление производством".

## <a name="bom-consumption-and-picking-list-journals"></a>Потребление спецификации и журналы отгрузочных накладных
Правильная настройка потребления по спецификации имеет большую важность, потому что она позволяет гарантировать эффективное управление запасами. Например, если параметры потребления по спецификации не заданы правильно в модуле "Управление производством", это может привести к тому, что материалы будут списываться из запасов по дважды или не будут списываться вовсе.

На странице **Параметры производства** автоматическое потребление по спецификации настраивается в три этапа:

- В начале производства. Этот этап настраивается на вкладке **Запуск**.
- Во время производственного процесса, когда операция завершена. Этот этап настраивается на вкладке **Операции**.
- Когда производственный заказ указывается как завершенный. Этот этап настраивается на вкладке **Приемка**.

Для каждого этапа поле **Автопотребление по спецификации** позволяет выбрать один из трех методов комплектации номенклатур для производственного заказа:

- **Принцип пополнения по спецификации** — этот вариант используется в сочетании с параметром, указанным для спецификации в модуле **Производство**. Щелкните **Управление производством** &gt; **Общее** &gt; **Производственные заказы** &gt; **Все производственные заказы**. На странице **Все производственные заказы** выберите производственный заказ в списке, а затем на панели операций щелкните **Спецификация**. На странице **Спецификация** на вкладке **Настройка** в поле **Принцип пополнения по спецификации** выберите один из следующих вариантов:

    - **Запуск**
    - **Готово**
    - **Вручную**
    - Пусто (ни один из вариантов не выбран).
    - **Доступно в ячейке**

    В модуле "Управление производством", если в поле **Автопотребление по спецификации** на вкладке **Запуск** выбран вариант **Принцип пополнения по спецификации**, все материалы, для которых в спецификации установлен вариант **Запуск**, вычитаются из запасов при запуске операции. Вариант **Доступно в ячейке** используется для продуктов, для которых включены расширенные складские процессы. Если выбрать этот принцип пополнения по спецификации, материал списывается при завершении работы склада по комплектации сырья. Материал также списывается, когда строка спецификации, в которой используется этот принцип пополнения, выпускается на склад, и материал доступен в ячейке поступления на производство.
    
    > [!NOTE]
    > Если **Принцип пополнения по спецификации** задан на вкладке **Запуск** в модуле "Управление производством", необходимо выбрать этот же принцип на вкладке **Операции** или на вкладке **Приемка**. Это требование позволяет гарантировать, что материалы будут вычитаться из запасов по спецификациям, у которых в качестве принципа пополнения по спецификации в производственном заказе используется **Готово**. Если на вкладке **Операции** или на вкладке **Приемка** не выбран этот же принцип пополнения по спецификации, материалы могут вычитаться из запасов дважды.
 
- **Всегда** — если выбрать этот вариант для этапа, материалы всегда вычитаются из запасов на этом этапе. Например, материалы для производства будут вычитаться при запуске производственного заказа. Этот вариант требует, чтобы на вкладках **Операции** и **Приемка** был выбран вариант **Никогда**. Это требование позволяет предотвратить двукратное вычитание номенклатур из запасов.
- **Никогда** — при выборе этого варианта для этапа потребление по спецификации на этом этапе не происходит. Например, если выбрать **Никогда** на всех трех вкладках (**Запуск**, **Операции** и **Приемка**), материалы нужно будет вычитать из запасов вручную.

> [!IMPORTANT]
> Внимательно изучите свою настройку параметров производства и убедитесь, что параметры, выбранные на различных вкладках страницы **Параметры производства**, не противоречат друг другу.

Следующие примеры иллюстрируют параметры, соответствующие различным принципам потребления по спецификации. Эти параметры настраиваются на странице **Параметры производства** страницы в модуле "Управление производством".

### <a name="example-1-backflushing-on-operations"></a>Пример 1. Обратный учет по операциям

Используйте следующие параметры, если необходимо генерировать журналы отгрузочных накладных и потребление номенклатур по спецификации при регистрации номенклатур как завершенных для данной операции.

| Вкладка                | Поле                          | Настройка                             |
|--------------------|--------------------------------|-------------------------------------|
| Запустить              | Обновить запуск           | **Статус** или **Статус + количество** |
| Запустить              | Автопотребление по спецификации      | **Никогда**                           |
| Operations         | Автопотребление по спецификации      | **Всегда**                          |
| Приемка | Автопотребление по спецификации      | **Никогда**                           |
| Приемка | Обновить конечный отчет | **Статус + количество**               |

### <a name="example-2-backflushing-on-production"></a>Пример 2. Обратный учет по производству

Используйте следующие параметры, если необходимо генерировать журналы отгрузочных накладных и потребление номенклатур по спецификации при регистрации номенклатур как завершенных для данного производственного заказа.

| Вкладка                | Поле                          | Настройка                             |
|--------------------|--------------------------------|-------------------------------------|
| Запустить              | Обновить запуск           | **Статус** или **Статус + количество** |
| Запустить              | Автопотребление по спецификации      | **Никогда**                           |
| Operations         | Автопотребление по спецификации      | **Никогда**                           |
| Приемка | Автопотребление по спецификации      | **Всегда**                          |
| Приемка | Обновить конечный отчет | **Статус + количество**               |

### <a name="example-3-flushing-principle"></a>Пример 3. Принцип пополнения по спецификации

Используйте следующие настройки, если генерировать журналы отгрузочных накладных и потребление номенклатур по спецификации следует в соответствии с принципом пополнения по спецификации, заданным для номенклатур спецификации.

| Вкладка                | Поле                          | Настройка                |
|--------------------|--------------------------------|------------------------|
| Запустить              | Обновить запуск           | **Статус + количество**  |
| Запустить              | Автопотребление по спецификации      | **Принцип пополнения по спецификации** |
| Operations         | Автопотребление по спецификации      | **Принцип пополнения по спецификации** |
| Приемка | Автопотребление по спецификации      | **Никогда**              |
| Приемка | Обновить конечный отчет | **Статус + количество**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Пример 4. Вычитание материалов во время запуска производственного заказа

Используйте следующие параметры, если журналы отгрузочных накладных и потребление номенклатур по спецификации должны создаваться при запуске производства.

| Вкладка                | Поле                          | Настройка                             |
|--------------------|--------------------------------|-------------------------------------|
| Запустить              | Обновить запуск           | **Статус + количество**               |
| Запустить              | Автопотребление по спецификации      | **Всегда**                          |
| Operations         | Автопотребление по спецификации      | **Никогда**                           |
| Приемка | Автопотребление по спецификации      | **Никогда**                           |
| Приемка | Обновить конечный отчет | **Статус** или **Статус + количество** |

В зависимости от настроек, описанных выше в этом разделе, журналы отгрузочных накладных разносятся на различных этапах процесса производственного заказа:

- При запуске операции
- При получении для операции обратной связи по количеству
- При учете номенклатур в производственном заказе как принятых

### <a name="example-5-manual-bom-consumption"></a>Пример 5. Ручное потребление по спецификации

Можно использовать следующие настройки, если материалы должны всегда вычитаться из запасов вручную. В этом случае журналы отгрузочных накладных не разносятся.

| Вкладка                | Поле                          | Настройка    |
|--------------------|--------------------------------|------------|
| Запустить              | Обновить запуск           | **Статус** |
| Запустить              | Автопотребление по спецификации      | **Никогда**  |
| Operations         | Автопотребление по спецификации      | **Никогда**  |
| Приемка | Автопотребление по спецификации      | **Никогда**  |
| Приемка | Обновить конечный отчет | **Статус** |
