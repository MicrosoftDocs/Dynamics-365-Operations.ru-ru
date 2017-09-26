---
title: "Создание документации или обучения с помощью записей задач"
description: "В этом разделе объясняется, что такое Регистратор задач и руководства по задачам, как создать записи задач и как настроить руководства по задачам Microsoft и включить их в вашу Справку."
author: josaw1
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 529751c09b8f99f986cad23a633bea661929d558
ms.openlocfilehash: d5e4857081134808b194d3248dd8739f83b57d6e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2017

---

# <a name="create-documentation-or-training-using-task-recordings"></a>Создание документации или обучения с помощью записей задач

[!include[banner](../includes/banner.md)]

В этом разделе объясняется, что такое Регистратор задач и руководства по задачам, как создать записи задач и как настроить руководства по задачам Microsoft и включить их в вашу Справку.

> [!IMPORTANT]
> Для Dynamics 365 for Talent возможность создания пользовательских проводников по задачам не предусмотрена. Справочная система Talent автоматически подключается к проводникам по задачам для этого продукта. 

<a name="learn-about-task-recorder"></a>Сведения о регистраторе задач
-------------------------

Регистратор задач — это средство, которое можно использовать для записи действий, выполняемых в пользовательском интерфейсе продукта. При использовании регистратора задач записываются все события, выполняемые в пользовательском интерфейсе с участием сервера, включая добавление значений, изменение параметров и удаление данных. Записываемые шаги вместе называются *записью задачи*. Записи задач можно использовать различными способами.

-   **Записи задач можно воспроизводить как руководства по задачам.** Руководства по задачам являются неотъемлемой частью справочной системы. Руководство по задаче — это контролируемая, управляемая и интерактивная пошаговая процедура выполнения бизнес-процесса. Пользователь получает инструкции по завершению каждого шага с помощью всплывающей подсказки (или "пузыря"), которая анимирована в пользовательском интерфейсе и указывает на элемент пользовательского интерфейса, с которым должен взаимодействовать пользователь. В "пузыре" также предоставляется информация о том, как взаимодействовать с элементом, например "Нажмите здесь" или "Введите значение в этом поле". Руководство по задаче выполняется согласно текущему набору данных пользователя и данным, введенным в среде потребителя.
-   **Записи задачи можно отображать как шаги процедур в области Справка.** Область Справка можно использовать для поиска и отображения записей задач. Область "Справка" можно открыть, щелкнув значок **?** на верхней панели навигации или используя сочетание клавиш **Ctrl+Shift+?**. Можно просмотреть шаги записи задачи в области "Справка" или воспроизвести запись как руководство по задаче, чтобы пройти через все этапы в пользовательском интерфейсе.
-   **Записи задач можно сохранить в BPM.** Можно сохранить запись задачи в строке иерархии в библиотеке средства моделирования бизнес-процессов (BPM) в Lifecycle Services (LCS). Список шагов и диаграмма бизнес-процесса будут созданы из записи. Записи задач, сохраненные в библиотеке BPM, можно отображать как справку.
-   **Записи задач можно сохранить как документы Word.** Это позволяет легко создавать печатные обучающие руководства.

Можно создать собственные записи задач, воспроизвести записи задач, предоставленные Майкрософт, или изменить записи задач, предоставленные Майкрософт, в соответствии с собственной конфигурацией. Дополнительные сведения о регистраторе задач см. в разделе [Регистратор задач](task-recorder.md).

## <a name="plan-your-task-recording"></a>Планирование записи задачи
Если вы создаете новую запись задачи или основываетесь на записи в записи задачи Майкрософт, учитывайте следующее.

-   Планируйте запись так же, как видео. Принимайте решения заблаговременно.
-   Выполните все шаги бизнес-процесса несколько раз без записи, чтобы понять шаги.
-   При этом обратите внимание, где вы используете сочетания клавиш или клавишу **ВВОД**, чтобы избежать их использования во время фактической записи.
-   Определите следующее:
    -   Требуется ли сгруппировать шаги в подзадачи? Подзадачи визуально разделяют разделы процесса. Например, при создании записи для процесса "Создание и выпуск продукта" может потребоваться сгруппировать шаги, необходимые для создания продукта, а затем сгруппировать шаги, необходимые для выпуска продукта. Подзадачи также упрощают чтение более длинных процессов.
    -   Требуется ли добавить заметки, и если да, то где? Дополнительные сведения см. в разделе "Изучите различные типы заметок" ниже.
    -   Какие значения будут добавлены в различные поля по мере выполнения шагов бизнес-процесса? Рекомендуется знать, что будет выбираться или вводиться по мере выполнения бизнес-процесса, чтобы не возвращаться и не исправлять ошибки во время записи.

**Напишите описания и заметки заранее**

-   В начале каждой записи задачи отображается поле описания, которое позволяет ввести введение в запись. Рекомендуется написать и сохранить описание заранее в отдельном документе, чтобы скопировать и вставить его в запись задачи во время записи. Таким образом можно уточнить текст заранее, а не во время записи. Вставка текста позволяет сделать процесс записи более быстрым и плавным.
-   Для каждого шага в записи задачи можно создать заметки. Во время воспроизведения руководства по задаче заметки отображаются в "пузыре" как примечания над или под текстом для шага. Если заметки просматривать как текст в области "Справка", они отображаются как текст, встроенный в шаг. Как и в случае описания, рекомендуется написать и сохранить заметки в отдельном документе. Во время воспроизведения записи задачи вставьте заметки из этого документа.

**Изучите различные типы заметок** Все заметки являются необязательными. Добавляйте их, только когда в них содержится полезная для пользователя информация.

-   **Заголовок.** Примечание заголовка отображается до текста шага, который автоматически создает регистратор задачи. В руководстве по задаче примечание заголовка отображается над автоматически созданным текстом. Используйте этот тип заметки, чтобы объяснить, почему пользователь выполняет этот шаг, или предоставить дополнительный контекст.

Это область редактирования, которая отображается при добавлении заметки при создании записи. Введите заметку заголовка в поле **Заголовок**. 

[![экран1](./media/screen1.png)](./media/screen1.png) 

Так выглядит заметка заголовка в "пузыре" в руководстве по задаче. 

[![экран2](./media/screen2.png)](./media/screen2.png)

-   **Примечания.** Заметка примечаний отображается после текста шага, который автоматически создает регистратор задачи. В руководстве по задаче она отображается, только если пользователь переходит по ссылке **Показать больше** в "пузыре" руководства по задаче. Используйте этот тип заметки для описания того, что необходимо знать пользователю для выполнения этого шага.

Это область редактирования, которая отображается при добавлении заметки при создании записи. Введите заметку примечаний в поле **Примечания**. 

[![экран3](./media/screen3.png)](./media/screen3.png) 

Так выглядит заметка примечания в "пузыре" в руководстве по задаче.

[![экран4](./media/screen4.png)](./media/screen4.png)

-   **Информационный шаг**: эти примечания создаются при щелчке правой кнопкой мыши на элементе управления или в любой части формы &lt; **Регистратор задач** &lt; **Добавить информационный шаг. **Информационные шаги отображаются как пронумерованные шаги в любом месте вставки, даже если действие не было записано в пользовательском интерфейсе. Можно добавить информационный шаг на уровне формы или информационный шаг, связанный с элементом управления. Если информационный шаг связан с формой, в каком-либо месте формы отобразится "пузырь" руководства по задаче без указателя при воспроизведении руководства по задаче. Если информационный шаг связан с элементом управления, "пузырь" руководства по задаче будет указывать на этот элемент управления при воспроизведении руководства по задаче. В области "Справка" заметка информационного шага отобразится как пронумерованный шаг с любым введенным текстом. Используйте информационные шаги, чтобы подготовить пользователя к следующим шагам, чтобы описать шаги, которые необходимо выполнить вне Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, или чтобы сослаться на другие записи (хотя создавать гиперссылки в заметках невозможно).

**Определите продолжительность записи**

-   Обычно пользователь читает или воспроизводит запись от начала до конца, поэтому не объединяйте шаги или задачи, которые лучше выполнять по-отдельности.
-   Старайтесь не записывать длинный сценарий, который включает несколько подпроцессов. Например, процесс "Использование секции обслуживания клиентов в магазине" слишком обширен. Разделите его на более короткие задачи, такие как "Принятие возвратов" и "Добавление к подарочному сертификату".
-   Если задачу можно выполнить в рамках нескольких различных бизнес-процессов, создайте для ее отдельную запись, чтобы ссылаться на эту задачу в других записях.
-   Если процесс включает несколько задач, которые пользователь, скорее всего, будет выполнять сразу, задачи можно включить в одну запись, например "Настройка и назначение функциональных профилей".
-   Если задача будет выполнять лишь один раз (например, конфигурация) и после этого будет сразу же выполняться другая задача, которая может быть повторяющейся или отдельной задачей, разделите эти задачи на две записи.

**Решите, где в пользовательском интерфейсе будет начинаться запись** Страница, на которой вы находитесь, когда начинается запись задачи, определяет то, для какой страницы воспроизводится руководство по задаче. Например, если вы хотите, чтобы запись по задаче отображалась в области "Справка", когда пользователь щелкает справку на странице "Параметры главной книги", необходимо начать запись на странице "Параметры главной книги". **Сохраните записи как AXTR-файлы** После завершения создания или изменения записи задачи вы можете загрузить или сохранить запись несколькими способами. Можно загрузить файл как пакет записи задачи (.axtr), загрузить файл как сырой файл записи (.xml), загрузить файл как документ Word или сохранить файл в библиотеке LCS. Рекомендуется всегда сохранять запись задачи как файл пакета записи задачи (.axtr). Это облегчит обслуживание файла, если потребуется изменить процедуры или заметки позже. Если требуется загрузить файл как документ Word, также сохраните его как файл пакета записи задачи.

## <a name="create-your-task-recording"></a>Создание записи задачи
Подробное пошаговое руководство см. в разделе [Создание записи задачи](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Копирование и настройка записей задач Майкрософт
Можно загрузить и изменить записи задач Майкрософта, чтобы использовать их для собственной справочной документации или учебных материалов. Чтобы загрузить запись задачи Майкрософт, выполните следующие шаги:

1.  Откройте регистратор задач. Регистратор задач расположен в меню **Настройки**.
2.  В области ресторатора задач щелкните **Ведение записи.**
3.  В разделе **Где находится запись** щелкните **В библиотеке LCS**.
4.  Щелкните **Выбор библиотеки LCS**.
5.  Выберите глобальную библиотеку Microsoft.
6.  В дереве выберите узел библиотеки бизнес-процессов, с которым связана запись задачи.
7.  Нажмите кнопку **OК**.
8.  Щелкните **Начать**.
9.  Теперь просмотрите запись, изменяя любые шаги, которые будут перезаписаны. **Примечание**. Если требуется изменить только текст записи, можно открыть запись в режиме **Изменение заметок к записи** и затем сохранить ее.
10. После воспроизведения записи до конца щелкните **Остановить** на панели регистратора задач вверху экран.
11. Выберите способ сохранения записи задачи.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Включение записей задач в область "Справка"
Чтобы отобразить собственные пользовательские записи задач в области "Справка", чтобы их можно было воспроизвести как руководства по задачам или просмотреть как текст, необходимо сохранить записи задач в собственной библиотеке BPM, а затем обновить параметры системы справки, чтобы она указывала на вашу библиотеку BPM. Дополнительные сведения см. в разделе [Подключение системы справки.](../get-started/help-connect.md)

<a name="see-also"></a>См. также
--------

[Обзор справки](..\get-started\help-overview.md)

[Подключение справки](..\get-started\help-connect.md)

[Регистратор задач](task-recorder.md)

[Создание расширенных разделов справки с помощью регистратора задач (внешняя ссылка)](https://mbspartner.microsoft.com/AX/Videos/970)
