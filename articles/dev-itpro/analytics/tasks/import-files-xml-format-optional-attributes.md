---
title: (RCS) Импорт файлов в формате XML с дополнительными атрибутами
description: В этой теме содержится информация о том, как пользователь может проектировать конфигурацию формата ER для импорта файлов в формате XML, содержащих дополнительные атрибуты.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727083"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Импорт файлов в формате XML с дополнительными атрибутами

[!include [task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может разработать конфигурацию формата ER для импорта файлов в формате XML, содержащих необязательные атрибуты. Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного". Перед началом загрузите и локально сохраните файл IncomingDocumentToLearnHowToHandleOptionalAttributes.xml из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).

1.  Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.
2.  Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](er-configuration-provider-mark-it-active-2016-11.md).
3.  Щелкните **Конфигурации отчетности**.

## <a name="create-a-new-data-model-configuration"></a>Создать новой конфигурации модели данных
1.  Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.
2.  В поле **Имя** введите "Модель для импорта XML-файла".
3.  Нажмите **Создать конфигурацию**.
4.  Выберите **Конструктор**.
5.  Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.
6.  В поле **Имя** введите "Root".
7.  Нажмите кнопку **Добавить**.
8.  Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.
9.  В поле **Имя** введите "List".
10. В поле **Тип элемента** выберите **Список записей**.
11. Нажмите кнопку **Добавить**.
12. Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.
13. В поле **Имя** введите "Code".
14. В поле **Тип элемента** выберите **Строка**.
15. Нажмите кнопку **Добавить**.
16. Нажмите кнопку **Сохранить**.
17. Закройте страницу.
18. Щелкните **Изменить статус**.
19. Щелкните **Завершить**.
20. Щелкните **OK**.

## <a name="create-a-format-for-data-import"></a>Создание формата для импорта данных
1.  Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.
2.  В поле **Создать** введите "Формат, основанный на модели данных «Модель для импорта XML-файла»".
3.  В поле **Имя** введите "Формат для импорта XML-файла".
4.  Выберите **Да** в поле **Поддерживает импорт данных**.
5.  Нажмите **Создать конфигурацию**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Создание формата для разбора входящего файла в формате XML
1.  Выберите **Конструктор**.
2.  Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.
3.  В дереве выберите **XML\Элемент**.
4.  В поле **Имя** введите "root".
5.  Щелкните **OK**.
6.  Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.
7.  В дереве выберите **XML\Элемент**.
8.  В поле **Имя** введите "document".
9.  В поле **Кратность** выберите **Один — много**.
10. Щелкните **OK**.
11. В дереве выберите **root\document**.
12. Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.
13. В дереве выберите **XML\Атрибут**.
14. В поле **Имя** введите "ID".
15. Щелкните **OK**.
16. Нажмите кнопку **Сохранить**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Создание сопоставления форматов для сохранения проанализированных данных в модели данных
1. Щелкните **Сопоставить формат модели**.
2. Нажмите кнопку **Создать**.
3. В поле **Определение** введите или выберите значение.
4. В списке перейдите по ссылке в выбранной строке.
5. В поле **Имя** введите "Сопоставление".
6. Нажмите кнопку **Сохранить**.
7. Выберите **Конструктор**.
8. В дереве разверните **format**.
9. В дереве разверните узел **format\root: XML Element(root)**.
10. В дереве выберите **format\root: XML Element(root)\document: XML Element 1..* (документ)**.
11. Щелкните **Связать**.
12. В дереве разверните **format\root: XML Element(root)\document: XML Element 1..* (документ)**.
13. В дереве выберите **format\root: XML Element(root)\document: XML Element 1..* (документ)\id**.
14. В дереве разверните **List = format.root.document**.
15. В дереве выберите **List = format.root.document\Code**.
16. Щелкните **Связать**.
17. Нажмите кнопку **Сохранить**.
18. Закройте страницу.
 
## <a name="run-format-mapping"></a>Запуск сопоставления формата
1. Щелкните **Выполнить**.
2. Нажмите кнопку **Обзор** и выберите **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Щелкните **OK**.

> [!NOTE]
> Выбранный файл не был импортирован, поскольку структура формата предполагает существование атрибута "id" для элемента "document", но импортированный файл не содержит такого атрибута.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Изменение структуры формата, чтобы обрабатывать атрибут XML как необязательный
1. Закройте страницу.
2. В дереве разверните **root\document**.
3. В дереве выберите **root\document\id**.
4. Выберите **Да** в поле **Пустая строка для отсутствующего атрибута**.
5. Нажмите кнопку **Сохранить**.
 
## <a name="run-format-mapping-to-test-changes"></a>Запуск сопоставления форматов для проверки изменений
1. Щелкните **Сопоставить формат модели**.
2. Щелкните **Выполнить**.
3. Нажмите кнопку **Обзор** и выберите файл **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Щелкните **OK**.
5. Просмотрите сформированный файл. 

> [!NOTE]
> Этот же файл, который был импортирован в качестве структуры формата, теперь считает атрибут "id" для элемента "document" необязательным.