---
title: Использование относительного пути в привязках данных для моделей и форматов электронной отчетности
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a026eec379f98fd32080df50b5e114b423db34ad
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182815"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Использование относительного пути в привязках данных для моделей и форматов электронной отчетности

[!include[banner](../includes/banner.md)]

Средство электронной отчетности (ER) позволяет пользователям определять структуры электронных форматов, а затем описывать способы заполнения этих структур, используя данные и алгоритмы, существующие в приложении. Дополнительные сведения см. в разделе [Создание конфигураций электронной отчетности (ER)](electronic-reporting-configuration.md). Чтобы указать поток данных для извлечения данных Finance and Operations и их использования для создания электронного документа, необходимо выполнить следующие действия:

- Привяжите настроенные источники данных к элементам спроектированной доменной модели данных. Структура модели и выбранные источники данных могут быть частью сложной иерархической структуры. В связи с этим окончательные привязки могут быть довольно большими и содержать множество элементов различных типов (например, отношения, таблицы и методы). Привязки могут быть менее удобочитаемыми и довольно сложными для проверки и понимания, особенно для не владельцев. 
- Свяжите элементы модели данных с компонентами формата, чтобы определить, какие данные будут заполнены из модели данных в сформированных выходных данных формата.

Чтобы повысить удобство использования конструкторов сопоставления ER, выпущена функция относительных путей. По умолчанию параметр представление относительного пути включен для любого нового экземпляра приложения, в котором используется разработка ER (Microsoft Dynamics 365 Finance, служба Microsoft Regulatory Configuration Service). Мы реализовали параметр относительного пути, чтобы пользователи могли продолжать использовать полный путь при работе с этой презентацией привязок электронной отчетности.

[![Параметры пользователя](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Когда параметр использования относительного пути включен, один символ @ заменяет путь к родительскому элементу в привязке текущего элемента модели. Полный путь привязки становится короче, что делает все сопоставление более очевидным и понятным. В большинстве случаев в конструкторе ER не требуется дополнительной прокрутки для просмотра всех привязок модели данных.

[![Конструктор сопоставлений моделей](./media/relative-path-02.png)](./media/relative-path-02.png)
 
После начала разработки нового выражения ER необходимо ввести только один символ, чтобы определить привязку к полю родительского элемента.

[![Конструктор формул](./media/relative-path-03.png)](./media/relative-path-03.png)
 
При изменении источника данных родительского элемента модели с использованием абсолютного пути необходимо вручную выполнить повторную привязку этого элемента модели, а также всех вложенных элементов, к новому источнику данных. Если параметр относительного пути включен и выбран новый источник данных, который должен быть привязан к родительскому элементу, предлагается возможность автоматически повторно выполнить привязку всех вложенных элементов этого родительского элемента одним щелчком мыши.

[![Сообщение о замене существующего пути](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Если вы подтвердите повторную привязку вложенных элементов, новый родительский элемент будет помещен в путь к каждому вложенному элементу, содержащему существующий родительский элемент.
Эта функция не нарушает обратную совместимость среды электронной отчетности. Все ранее созданные конфигурации электронной отчетности будут работать с этой новой функцией, а обновления или преобразования не требуются.

> [!NOTE]
> Все изменения, введенные в результате массового изменения привязок вложенных элементов в сопоставлениях моделей, правильно сохраняются в виде разностной конфигурации (трассировка изменений). Это позволяет пользователям изменять основу производной версии сопоставлений моделей на любую новую базовую версию, которая была изменена с помощью этой новой функции.