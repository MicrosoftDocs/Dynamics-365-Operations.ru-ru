---
title: Типы актива
description: В этой статье объясняется, как создавать типы активов в управлении активами. В нем также описаны номенклатуры, связанные с типами активов.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3a51fdb55e9158e88e89549e3d0049e699c233e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887641"
---
# <a name="asset-types"></a>Типы актива

[!include [banner](../../includes/banner.md)]



В этой статье объясняется, как создать типы актива. В нем также описаны номенклатуры, связанные с типами активов. Типы активов используются в качестве общих категорий для активов. Примеры включают CNC машины, измерительное оборудование и двигатели грузовиков. Типы активов используются для управления типами заданий обслуживания (задачи обслуживания), состояниями жизненного цикла активов, счетчиками, атрибутами активов, шаблонами оценки состояния и моделями активов, которые могут быть выбраны для актива. При создании актива необходимо указать тип актива.

Для каждого типа актива могут быть созданы вариации настройки типа актива. Например, если у вас есть тип актива, который называется **Грузовики**, вы можете создать вариации этого типа актива для различных производителей активов и моделей активов. К каждой настройке типа актива можно добавить необходимые запасные части и планы обслуживания.

Во-первых, вы настраиваете необходимые типы активов. Далее вы создаете модели активов, которые должны быть связаны с типами активов. Наконец, на странице **Значения по умолчанию для типа актива** создаются все вариации типов активов, необходимых для вашего оборудования.

## <a name="create-an-asset-type"></a>Создание типа актива

1. Выберите **Управление активами** > **Настройка** > **Типы активов** > **Типы активов**.
2. Выберите **Создать**, чтобы создать тип актива.
3. В поле **Тип актива** введите идентификатор типа актива.
4. В поле **Имя** введите имя.
5. В поле **Модель жизненного цикла актива** выберите модель жизненного цикла актива. Для получения дополнительной информации о состояниях жизненного цикла актива и моделях жизненного цикла актива см. раздел [Состояния жизненного цикла актива](object-stages.md).
6. Установите параметр **Итог** на **Да**, если следует рассчитать сводные значения ключевого показателя производительности (КПЭ) для активов, которые имеют этот тип активов.
7. Нажмите **Сохранить**.
8. На экспресс-вкладке **Типы заданий обслуживания** выберите типы заданий обслуживания, которые должны быть связаны с типом актива:

    - Чтобы выбрать тип задания обслуживания, выберите его в поле **Остальные типы заданий обслуживания**, а затем выберите кнопку со стрелкой вправо ![Кнопка со стрелкой вправо.](media/29-setup-for-objects.png) чтобы переместить его в выбранный раздел **Выбранные типы заданий обслуживания**.
    - Чтобы выбрать все доступные типы заданий, выберите кнопку со стрелкой ![Все вперед.](media/30-setup-for-objects.png) кнопка. Все типы задания обслуживания перемещаются из поля **Остальные типы заданий обслуживания** в поле **Выбранные типа заданий обслуживания**.
    - Чтобы отменить выбор типа задания обслуживания, выберите его в поле **Выбранные типы заданий обслуживания**, а затем выберите кнопку со стрелкой влево ![Кнопка со стрелкой влево.](media/31-setup-for-objects.png) чтобы переместить его в выбранный поле **Остальные типы заданий обслуживания**.

9. Также можно выбрать счетчики, которые должны быть связаны с типом актива. На экспресс-вкладке **Счетчики** сделайте свой выбор, используя методы, которые описаны для типов задания обслуживания в шаге 8. Дополнительные сведения о настройке счетчиков см. в разделе [Счетчики](counters.md).
10. Также можно выбрать типы атрибута, которые должны быть связаны с типом актива. На экспресс-вкладке **Типы атрибута** сделайте свой выбор, используя методы, которые описаны для типов задания обслуживания в шаге 8. Затем, чтобы создать предпочтительную последовательность типов атрибутов, выберите тип атрибута в поле **Выбранные типы атрибута** и используйте кнопки со стрелками вверх и вниз для перемещения. Последовательность типов атрибута будет отображаться на активах, использующих этот тип актива. Для получения дополнительной информации об атрибутах актива см. раздел [Типы атрибута обслуживания](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > При добавлении новых типов атрибута на экспресс-вкладке **Типы атрибута** существующие активы автоматически обновляются с этой информацией.

11. Также можно выбрать шаблоны оценки состояния, которые должны быть связаны с типом актива. На экспресс-вкладке **Оценки состояния** сделайте свой выбор, используя методы, которые описаны для типов задания обслуживания в шаге 8. Для получения дополнительной информации о шаблонах оценки состояния и регистрациях см. раздел [Оценки состояния](../setup-for-objects/condition-assessment.md).
12. Экспресс-вкладка **Модель актива** показывает все комбинации производителей и моделей активов, настроенных на выбранный тип актива. Чтобы увидеть, как разделены комбинации в зависимости от производителя, выберите **Модель актива**, чтобы открыть страницу **Модель актива**.

    На странице **Модель актива** можно добавить отношения модели актива и типа актива. Кроме того, на странице **Типы актива** можно добавить отношения производителя актива и модели актива непосредственно к типу актива. Наконец, на странице **Модель актива** (**Управление активами** \> **Настройка** \> **Активы** \> **Модель актива**) вы можете создать новые отношения производитель актива – модель актива – тип актива. Таким образом, существует три способа настройки и редактирования отношений производитель актива – модель актива – тип актива. Все доступные комбинации отображаются с разных перспектив, и вы можете выбрать предпочтительную точку входа, когда вы работаете с настройкой.

> [!NOTE]
> - Если выбрать счетчики для типа актива, выбранные параметры автоматически обновляются на странице **счетчики** (**Управление активами** > **настройка** > **Активы** > **Типы активов** > **Счетчики**).
> - Поля в разделе **Подробно** на экспресс-вкладке **Общее** показывают количество типов задания обслуживания, счетчиков, атрибутов и т.д., которые настроены на выбранный тип актива.

Как правило, заказы на работу, созданные вручную, связаны с корректирующим обслуживанием, в то время как автоматически создаваемые заказы на работу связаны с профилактическим обслуживанием. При создании заказов на работу вручную можно использовать только типы заданий обслуживания, выбранные на экспресс-вкладке **Типы заданий обслуживания** страницы **Типы актива**. Тем не менее, автоматически созданные заказы на работу могут использовать все типы заданий обслуживания, которые вы создаете на странице **Типы заданий обслуживания** (**Управление активами** \> **Настройка** \> **Задания** \> **Типы заданий обслуживания**).

## <a name="create-asset-type-setup-lines"></a>Создание строк настройки типа актива

1. Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Типы активов** \> **Настройка типа актива**. Или, выберите **Управление активами** \> **Настройка** \> **Активы** \> **Типы актива** \> **Типы актива**, выберите тип актива и затем выберите **Настройка типа актива**.
2. При первом использовании страницы **Настройка типа актива** можно найти полезной кнопку **Создание комбинаций**. Эту кнопку можно использовать для быстрого создания любых комбинаций модели актива на типе актива. Выберите **Создание комбинаций**, выберите тип актива для создания комбинаций, а затем выберите **OK**.

    > [!NOTE]
    > Если вы не будете использовать все автоматически созданные комбинации настройки типа актива, вы можете удалить настройку, выбрав ее, а затем выбрав **Удалить**.

3. Выберите **Создать**, чтобы вручную создать настройку типа актива.
4. В зависимости от того, насколько конкретной должна быть настройка типа актива, сделайте выбор в полях **Тип актива**, **Производитель** и **Модель**.
5. Если гарантийное договор связан с типом актива, выберите соглашение в полях **Гарантия Поставщика** и **Гарантия Клиента**. 
6. На экспресс-вкладке **Запасные части** выберите **Добавить**, чтобы добавить запасные части в выбранную настройку типа актива.
7. Чтобы утвердить запасную часть, выберите строку запасных частей, а затем выберите **Утвердить**. Можно выбрать несколько строк для утверждения.
8. Чтобы узнать, используется ли запасная часть где-то еще в управлении активами (например, в отношении активов и заказов на работу), выберите строку запасных частей, а затем выберите **Применимость номенклатуры** для открытия страницы **Применимость номенклатуры**. Чтобы увидеть все активные запасные части в списке, выберите флажок **Активный**. Чтобы увидеть только утвержденные запасные части, выберите флажок **Утвержденный**.
9. На экспресс-вкладке **Планы обслуживания** выберите **Добавить**, чтобы добавить планы обслуживания в выбранную настройку типа актива.
10. Чтобы скопировать настройку типа актива в другую настройку, можно использовать функцию «Копировать». Выберите настройку типа актива, в которую нужно скопировать настройку, выберите **Скопировать настройку**, и выберите настройку типа актива, из которой нужно скопировать настройку. Параметры различных параметров определяют, сколько информации включено. После завершения, выберите **OK**, чтобы скопировать настройки.

> [!NOTE]
> При наличии большого числа строк запасных и строк плана обслуживания, которые вы будете повторно использовать, функция «Копировать» позволяет быстро и легко настроить данные для многих комбинаций настройки типа актива.

## <a name="spare-parts-on-the-asset-type-setup"></a>Запасные части в настройке типа актива

Как было описано в разделе «Создание строк настройки типа актива», запасные части настраиваются в моделях актива на странице **Настройка типа актива**. Поэтому при открытии страницы **Настройка типа актива** можно увидеть только запасные части, связанные с выбранной комбинацией типа актива, производителя актива и модели актива. Чтобы увидеть список всех записей запасных частей, откройте страницу **Запасные части** (**Управление активами** \> **Запросы** \> **Запасные части**).

На странице **Запасные части** можно также создавать новые запасные части для существующих комбинаций типа актива, производителя актива и модели актива. Вы можете решить, предпочитаете ли вы создавать записи запасных частей на странице **Настройка типа актива** или на странице **Запасные части**. Страница **Настройка типа актива** содержит обзор данных о выбранной комбинации типа актива, производителя актива и модели актива, в то время как страница **Запасные части** предоставляет полный обзор всех строк настройки типа актива. Если страница **Запасные части** содержит много записей, страница **Настройка типа актива** может дать вам лучший обзор.

Чтобы узнать, используется ли запасная часть выбранной строки где-то еще в управлении активами (например, в отношении активов и заказов на работу), выберите **Применимость номенклатуры** для открытия страницы **Применимость номенклатуры**. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]