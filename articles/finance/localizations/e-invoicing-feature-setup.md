---
title: Работа с настройками функцией
description: В этой статье объясняется, как настроить функции электронного выставления накладных.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 0d64757871c12ae914f7ace4cc0121a08a32a9d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272267"
---
# <a name="work-with-feature-setups"></a>Работа с настройками функцией

[!include [banner](../includes/banner.md)]

Чтобы настроить создание электронных файлов и других шагов обработки (например, добавление цифровых подписей файлов, их отправка в веб-службу правительственных органов и получение ответов или их хранение), настройте процесс обработки, правила применимости и переменные для функций электронных накладных.

Сведения о настройке комбинируются в концепцию *настройки функции*, и они могут быть созданы, удалены или скорректированы. Для завершенных версий функций электронного выставления накладных эти сведения также можно просмотреть.

Можно создать столько элементов настройки функций, сколько необходимо для определения различных сценариев создания, обработки и получения электронных файлов. Несмотря на то, что эти пункты настройки функций имеют независимые действия обработки и условия для выполнения, они создаются как часть единой функции электронного выставления накладных и наследуют ее жизненный цикл и процесс развертывания.

## <a name="add-a-feature-setup"></a>Добавление настройки функции

1. Выполните вход в учетную запись Regulatory Configuration Services (RCS).
2. В рабочей области **Функция глобализации** в разделе **Функции** выберите плитку **Электронное выставление накладных**.
3. На странице **Функции электронного выставления накладных** выберите версию функции электронного выставления накладных, которая находится в состоянии **Черновик**.
4. На вкладке **Настройки** выберите **Добавить**.
5. В раскрывающемся диалоговом окне **Создать настройку функции** в группе полей **Создать** выберите один из следующих вариантов:
 
    - **Пользовательская настройка** — создайте новую настройку функций с пустыми каналами, пустым списком конвейера обработки, пустым разделом для правил применимости и набором переменных по умолчанию, в зависимости от типа настройки.
    - **Из настройки функций** — создание копии другой настройки функции в области текущей функции электронного выставления накладных.

6. Если на последнем шаге был выбран параметр **Пользовательская настройка**, введите имя и описание пункта настройки функции, затем в группе полей **Тип настройки** выберите один из следующих вариантов:

    - **Конвейер обработки** — выберите этот параметр для создания и обработки исходящих электронных документов. Для этого типа настройки система создает пустой список конвейера обработки, пустой раздел для правил применимости и набор переменных по умолчанию. Вы не сможете работать с каналами для входящих электронных документов.
    - **Канал данных** — выберите этот параметр, чтобы настроить процесс получения входящих электронных документов из одного из определенных каналов и передачи их непосредственно в Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management без дополнительных действий. Для этого типа настройки система создает заранее определенный список параметров для каналов данных, пустой раздел для правил применимости и набор переменных по умолчанию. Вы не сможете добавлять какие-либо действия в конвейер обработки.
    - **Канал данных и конвейер обработки** — этот тип настройки напоминает тип настройки **Канал данных**. Однако перед передачей входящего электронного документа в Finance или Supply Chain Management можно настроить дополнительные действия в конвейере обработки.

7. Если в последнем шаге был выбран **Канал данных** или **Канал данных и конвейер обработки**, в поле **Выбор канала данных** необходимо выбрать канал, с которым будет осуществляться интеграция.
8. Выберите **Создать**.

После создания настройки функций можно выбрать **Правка**, чтобы настроить ее.

## <a name="edit-a-feature-setup"></a>Изменение настройки функции

В зависимости от типа настройки функций можно настроить процесс создания исходящих электронных файлов и их отправки во внешние каналы, а также для получения входящих документов и передачи их в приложение Finance или Supply Chain Management.

### <a name="data-channel"></a>Канал данных

*Канал данных* принимает электронный файл и либо обрабатывает его, либо передает его непосредственно в Finance или Supply Chain Management. Этот параметр недоступен для настройки функций типа **Конвейер обработки**.

Для настройки канала данных введите имя канала. Затем определите параметры на основе выбранного типа канала. Идентификатор канала данных должен ссылаться на переменную, созданную специально для идентификации канала данных. Он будет использоваться в качестве ссылки в Finance или Supply Chain Management.

На вкладке **Фильтр вложений** необходимо определить набор фильтров для извлечения определенных файлов из канала. Можно создать несколько строк, если предполагается, что файлы будут иметь различные расширения имен файлов, или файлы должны обрабатываться по-разному в зависимости от имени файла. Вот основные параметры:

- **Имя** — введите имя файла, на который будет ссылаться система во время обработки. В приложениях Finance и Supply Chain Management можно будет просмотреть файлы в журнале отправки.
- **Фильтр** — определите фильтр для выбора файлов.
- **Необязательный** — если этот флажок снят, файл является обязательным. В этом случае система выводит сообщение об ошибке, если каналы не содержат файлов, соответствующих фильтру. Этот параметр применяется для сообщений электронной почты.

Если канал является почтовым ящиком, а входящее сообщение электронной почты содержит несколько вложений, можно настроить правила для определения того, как служба должна обрабатывать вложения. Служба может рассматривать каждое вложение как отдельную электронную накладную или рассматривать одно вложение как основную накладную, а все остальные вложения — как дополнения.

### <a name="processing-pipeline"></a>Обработка конвейера

*Конвейер обработки* представляет собой набор *действий*, которые выполняются последовательно до тех пор, пока они не будут успешно завершены. Конвейер обработки можно использовать для настройки процесса создания электронных файлов и выполнения других шагов (например, для цифровых подписей файлов, отправки их во внешние веб-службы и анализа отклика, а также получения и обработки входящих документов).

Список действий определен заранее. Можно использовать кнопки **Создать** и **Удалить**, чтобы указать комбинацию действий, которые логически определяют необходимый процесс для отправки или получения документов.

Порядок действий важен. Можно настроить порядок с помощью кнопок **Вверх** и **Вниз**.

У каждого действия есть набор параметров, которые можно настраивать или корректировать. Особый набор параметров зависит от типа действия.

- **Действие** — выберите тип действия.
- **Имя действия** — введите имя действия. Это имя будет отображаться в журналах отправки, а также в сообщениях в приложениях Finance и Supply Chain Management.
- **Описание** — укажите дополнительные сведения о назначении действия в процессе.
- **Включить повторную попытку** — если этот флажок установлен, можно выбрать действие в поле **Повторить попытку действия** и настроить дополнительные параметры на вкладке **Параметры повторных попыток**.

    Функция повторных попыток позволяет настроить поведение службы, если выполнение определенного действия невозможно. Например, если внешняя веб-служба, к которой вы пытаетесь подключиться, не отвечает, можно указать, сколько раз система должна повторить попытку подключения, с каким интервалом и от какого действия в конвейере обработки.

- **Экспорт результатов** — можно установить этот флажок для *одного* действия в конвейере обработки. Электронный файл, который действие создает в приложении Finance или Supply Chain Management, может быть экспортировано со страницы **Журнал отправки электронных документов**.

### <a name="applicability-rules"></a>Правила применимости

*Правила применимости* — это настраиваемые операторы, которые предоставляют контекст для выполнения функций электронного выставления накладных с помощью набора возможностей электронного выставления накладных.
Бизнес-документы, отправляемые из Finance или Supply Chain Management в электронное выставление накладных, не содержат явной ссылки, которая позволяет набору возможностей электронного выставления накладных вызывать определенную версию функции электронного выставления накладных и определенный элемент настройки функции для обработки отправки. Однако когда бизнес-документ правильно настроен, он содержит необходимые элементы, которые позволяют электронному выставлению накладных решить, какая версия функции электронного выставления накладных и конвейера обработки должна быть выбрана и выполнена.

Правила применимости позволяют службе электронного выставления накладных найти конкретные функции электронного выставления накладных, которые должны использоваться для обработки отправки. Для поиска правильных функций поля **Контекст** из отправленного бизнес-документа сопоставляются с предложениями из правил применимости.

С правилами применимости можно работать следующими способами:

- Выберите **Создать**, чтобы добавить новое предложение в набор правил применимости.
- Выберите **Удалить**, чтобы удалить предложение.
- Выберите несколько записей, а затем воспользуйтесь кнопкой **Группировать** или **Разгруппировать**, чтобы создать сочетание элементов или логических утверждений. Например, выберите строки, которые необходимо сгруппировать, затем выберите **Сгруппировать предложение**. При группировке предложений в сетку добавляется новый столбец. В этом столбце указывается логический оператор для сгруппированного предложения. Поддерживаются следующие типы операторов:

    - Equal
    - Not equal
    - Больше/Меньше
    - Больше или равно/Меньше или равно
    - Contains
    - Начинается с

    > [!NOTE]
    > При разгруппировании предложения всегда начинайте с самого вложенного уровня группировки.

### <a name="variables"></a>Переменные

*Переменные* обеспечивают большую гибкость при настройке конвейера обработки и потока данных между действиями. Можно ссылаться на переменную в некоторых параметрах действий для временного хранения данных или электронных файлов. Некоторые переменные используются для передачи данных между приложениями Finance или Supply Chain Management и службой электронного выставления накладных.

Система создает некоторые переменные по умолчанию. Например, переменная **BusinessDocumentDataModel** содержит деловые данные в структуре нотации объектов JavaScript Object Notation (JSON), которая передается в вызов из подключенного приложения во время процесса отправки.

Доступны следующие типы переменных:

- **Постоянная** — контейнер для хранения временных данных, которые используются в действиях конвейера обработки.
- **От клиента** — содержимое переменной извлекается из клиента Dynamics 365 во время выполнения процесса отправки.
- **В клиент** — содержимое переменной становится доступным для импорта клиентом Dynamics 365 во время выполнения процесса отправки.
- **Тип данных** — выберите тип данных сведений, которые хранятся в переменной.

### <a name="parameters"></a>Параметры

Параметр **Отключить сокращение бизнес-данных** используется для оптимизации структуры полезной нагрузки бизнес-данных, поступающих из приложения Finance или Supply Chain Management во время отправки электронного документа. Оптимизация позволяет уменьшить объем данных, поступающих в службу электронного выставления накладных для дальнейшего преобразования в требуемый электронный файл. Значение по умолчанию равно **Нет**.

- **Да** — Finance или Supply Chain Management отправит файл JSON структуры **Модель накладной** или **Финансовая модель** (для Бразилии), который определен в модуле **Электронная отчетность**. Все элементы модели заполняются деловыми данными на стороне приложения, независимо от готовой структуры электронного файла. Модели обычно содержат больше бизнес-данных, чем требуется для целевой структуры файлов, и для создания этих данных в приложении может потребоваться больше времени. Значение **Да** для этого параметра требуется в редком случае, когда требуется создавать различные выходные файлы в одной функции электронного выставления накладных и настройке функции. Значение **Да** полезно при устранении неполадок сценариев, в структуре электронных файлов и полноте бизнес-данных.
- **Нет** — Finance или Supply Chain Management произведет первый вызов службы без бизнес-данных. Цель этого вызова — получить сведения о конфигурации электронной отчетности (ER), которая будут использоваться для преобразования электронных файлов в конвейере обработки. Эти сведения возвращаются в приложение, которое использует его для определения подмножества бизнес-данных, которые должны быть включены в файл JSON структуры **Модель накладных** или **Финансовая модель** (для Бразилии). Значение **Нет** для этого параметра помогает уменьшить объем бизнес-данных, отправляемых приложением в службу, так как приложение может отправлять только бизнес-данные, необходимые для успешного создания электронного файла.

### <a name="validate-a-feature-setup"></a>Проверка настройки функции

Вы можете выполнить проверку для проверки согласованности всей конфигурации. Например, если обязательный параметр для действия оставлен пустым, проверка обнаруживает это несоответствие и выдается предупреждающее сообщение.

- На странице **Настройка версии функции** в области действий выберите **Проверить**.

## <a name="delete-a-feature-setup"></a>Удаление настройки функции

1. На странице **Функции электронного выставления накладных** выберите версию функции электронного выставления накладных, которая находится в состоянии **Черновик**.
2. На вкладке **Настройки** выберите **Удалить**.
3. В отобразившемся окне сообщений выберите **Да**, чтобы подтвердить удаление настройки функций.
