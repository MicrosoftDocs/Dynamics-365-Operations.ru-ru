---
title: Создание шаблонов электронной почты в Attract
description: Этот раздел содержит сведения о шаблонах электронной почты, которые можно создать и использовать в Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 55c12010cfd055ee6977f50e566b70f76a2e1682
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462312"
---
# <a name="create-email-templates-in-attract"></a>Создание шаблонов электронной почты в Attract

[!include [banner](includes/banner.md)]

С помощью библиотеки шаблонов электронной почты администраторы могут создать единообразную тему и фирменный стиль для всех сообщений электронной почты, отправляемых через Microsoft Dynamics 365 Talent: Attract и Offer. Администраторы могут также организовать коллекцию шаблонов содержимого электронной почты, которой могут пользоваться другие пользователи. Группа найма на работу может использовать эти шаблоны в своем workflow-процессе для более эффективной отправки сообщений электронной почты. Некоторые сообщения электронной почты настроены для автоматической отправки, и администратор может использовать библиотеку шаблонов электронной почты для настройки содержимого этих сообщений электронной почты.

> [!NOTE]
> Для использования шаблонов электронной почты ваша организация должна иметь надстройку Comprehensive Hiring.

## <a name="global-template-configurations"></a>Глобальные конфигурации шаблонов

Чтобы создать согласованный фирменный стиль для всех сообщений электронной почты, администратор должен сначала создать глобальный верхний и нижний колонтитул для всех шаблонов электронной почты. В центре администрирования на вкладке **Параметры шаблона электронной почты** в разделе **Заголовок** администратор может отправить изображение для использования в качестве заголовка или баннера для всех сообщений электронной почты. Изображение может быть логотипом компании, фирменным бланком или любым другим изображением, представляющим компанию. Рекомендуется, чтобы ширина быть в диапазоне от 25 до 800 пикселов, а высота в диапазоне от 25 до 150 пикселов, поскольку эти размеры лучше всего подходят для большинства клиентов электронной почты, например Microsoft Outlook. Изображение должно быть файлом JPEG, JPG, PNG или SVG, а размер файла должен быть менее 1 мегабайта (МБ). После отправки изображения создается и отображается предварительный просмотр заголовка. Если необходимо удалить или заменить изображение заголовка, администратор может использовать параметр **Удалить** над предварительным просмотром.

В разделе **Нижний колонтитул** администратор может предоставить ссылки на политику конфиденциальности компании для обмена данными, а также положения и условия. Эти ссылки включаются в нижний колонтитул, который создается автоматически. Затем отображается предварительный просмотр нижнего колонтитула. Администратор может также выбрать конкретный язык, на котором будут отправляться колонтитулы электронной почты как часть всех сообщений электронной почты. Эта же конфигурация языка также будет использоваться для сборки таблицы результатов собеседования. 

Не забудьте сохранить изменения перед закрытием центра администрирования.

> [!NOTE] 
> Верхний и нижний колонтитулы — это глобальные настройки для всех сообщений электронной почты. Таким образом, они будут отображаться во всех сообщениях электронной почты, отправляемых через Attract. Если эти параметры не настроены, верхний и нижний колонтитулы будут отсутствовать во всех сообщениях электронной почты.

## <a name="email-template-library"></a>Библиотека шаблонов сообщений электронной почты 

После настройки конфигураций глобального шаблона администратор можно начать создавать и организовывать шаблоны для всех сообщений электронной почты, отправляемых из Attract и Offer. Библиотека шаблонов электронной почты доступна только для администраторов. Чтобы открыть библиотеку, в главном меню переходов выберите вкладку **Шаблоны электронной почты**. Библиотека систематизирована по разным действиям в Attract, для которых требуется отправлять сообщения электронной почты, такие как планирование, оценка, создание должности и предложение. Администратор может выбрать любую категорию для просмотра всех типов сообщений электронной почты, которые связаны с действием. Например, выберите **Планирование** для просмотра различных типов сообщений электронной почты, отправляемых в процессе планирования, и всех шаблонов, доступных для каждого типа электронной почты. Каждый подраздел в категории представляет тип сообщения электронной почты.

Некоторые типы сообщений электронной почты могут иметь несколько получателей. Например, в категории **Планирование** сообщения электронной почты, которые отправляются, когда требуется сводка расписания собеседований, отправляются как кандидатам, так и сотрудникам, проводящим собеседование. В каждом разделе есть два основных столбца: **Название шаблона** и **Получатель**. Каждая строка в разделе представляет один шаблон для типа сообщений электронной почты. Сначала символ замка отображается в строке для каждого шаблона. Этот символ означает, что шаблон — стандартный шаблон, который поставляется с Attract и который не может быть удален. Для любого шаблона администратор может использовать кнопку с многоточием (**...**) для дублирования шаблона, задания его в качестве шаблона по умолчанию или удаления его. Когда шаблон задан как шаблон по умолчанию, возможен один из двух типов поведения. Поведение указывается значком или значками, отображаемыми в строке для шаблона:

- **По умолчанию** — этот значок указывает, что шаблон является шаблоном по умолчанию для сообщения электронной почты, которое отправляется, и что информация должна вводиться, когда пользователь отправляет сообщение электронной почты этого конкретного типа.
- **По умолчанию** + **Отправляются автоматически** — это сочетание значков указывает, что шаблон является активным шаблоном для генерируемых системой сообщений электронной почты, отправляемых автоматически.

Чтобы изменить шаблон, выберите строку и внесите изменения в шаблон.

> [!NOTE]
> У каждого получателя определенного типа сообщений электронной почты имеется шаблон по умолчанию. Все стандартные шаблоны Attract устанавливаются как шаблоны по умолчанию, пока администратор не создаст новый шаблон для определенного типа сообщений электронной почты и установит его в качестве шаблона по умолчанию.

## <a name="create-a-template"></a>Создать шаблон

Чтобы создать шаблон, в правом верхнем углу библиотеки шаблонов электронной почты выберите **+ Создать шаблон**. Чтобы выбрать тип сообщений электронной почты, для которого создается шаблон, выберите получателя, процесс и событие, для которого должно отправляться сообщение электронной почты. Затем выберите **Создать**.

Шаблон открывается в представлении редактирования, и можно задать имя шаблона. Например, если шаблон предназначен для кандидатов из университета США, но его содержимое написано на французском языке, можно ввести **Университет\_США\_французский** в заголовке. Заголовок, строка темы и основное содержимое для любого шаблона может поддерживать языки, отличные от английского.

Поле **Кому** для шаблона изменить невозможно, поскольку вы уже выбрали получателя при первом создании шаблона.

Можно добавлять таких пользователей, как **Специалист по найму** или **Специалист по комплектации штата**, в строку копии (Cc). При отправке сообщения электронной почты эти роли автоматически заменяются соответствующими пользователями, в зависимости от контекста должности.

Строка темы и основное содержимое поддерживают заполнители. Можно вставить заполнители, введя **\#**, затем выбрав соответствующий заполнитель в раскрывающемся списке автозавершения. Список доступных заполнителей отображается в правой части страницы. При отправке сообщения электронной почты эти заполнители автоматически заменяются на основе контекста должности и получателя. Например, шаблон для сообщения электронной почты, которое отправляется кандидатам, содержит заполнитель \#{Candidate\_Name}. При отправке сообщения электронной почты кандидату с именем Кэмерон, заполнитель будут заменен именем Кэмерона.

Редактор основного содержимого — это редактор форматированного текста, позволяющий задавать стиль и формат текста. Он также позволяет вставлять гиперссылки и привязки.

После создания шаблона для конкретного типа сообщений электронной почты выберите кнопку с многоточием (**...**) в строке для шаблона и задайте его в качестве шаблона по умолчанию.

## <a name="consume-templates"></a>Использование шаблонов

Когда группа найма отправляет сообщение электронной почты, она может использовать шаблоны, которые созданы администратором. Если было создано нескольких шаблонов для сообщения электронной почты, отправляемого пользователем, появляется раскрывающийся список в workflow-процессе составления сообщения электронной почты. Шаблон по умолчанию вводится автоматически, но пользователь может выбрать другой шаблон.

> [!NOTE] 
> Для автоматически отправляемых сообщений электронной почты можно создать несколько шаблонов. Однако только один шаблон можно задать в качестве активного шаблона. Поскольку этот процесс запускается событием, только администратор может определить шаблон, который необходимо использовать, на основе сочетания значков **По умолчанию** и **Отправляется автоматически** в библиотеке шаблонов.


[!INCLUDE[footer-include](../includes/footer-banner.md)]