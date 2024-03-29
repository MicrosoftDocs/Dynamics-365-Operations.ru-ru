---
title: Разработка новых конфигураций электронной отчетности для создания отчетов в формате Word
description: В этой статье объясняется, как пользователи могут настроить новый формат электронной отчетности (ER) для создания отчетов в виде документов Microsoft Word.
author: kfend
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.search.form:
- ERWorkspace, ERSolutionTable, EROperationDesigner
- LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: b56b328aa2a2b53dc177a02a4d453e5dbcb8340c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273349"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Разработка новых конфигураций электронной отчетности для создания отчетов в формате Word

[!include [banner](../includes/banner.md)]

Для создания отчетов в виде документов Microsoft Word необходимо разработать шаблон для отчетов, используя, например, классическое приложение Word. На следующем рисунке показан образец шаблона для контрольного отчета, который может быть создан для отображения сведений об обработанных платежах поставщикам.

![Образец шаблона для контрольного отчета в классическом приложении Word.](./media/er-design-configuration-word-image1.png)

Чтобы использовать документ Word в качестве шаблона для отчетов в формате Word, можно настроить новое [решение](er-quick-start1-new-solution.md) [электронной отчетности (ER)](general-electronic-reporting.md). Это решение должно включать [конфигурацию](general-electronic-reporting.md#Configuration) электронной отчетности, которая содержит компонент формата электронной отчетности.

> [!NOTE]
> При создании новой конфигурации формата электронной отчености для создания отчетов в формате Word необходимо либо выбрать **Word** в качестве типа формата в раскрывающемся диалоговом окне **Создать конфигурацию**, либо оставить поле **Тип формата** пустым.

![Создание конфигурации формата на странице конфигураций.](./media/er-design-configuration-word-image2.gif)

Компонент формата электронной отчетности решения должен содержать элемент формата **Excel\\File**, и этот элемент формата должен быть связан с документом Word, который будет использоваться в качестве шаблона для созданных отчетов во время выполнения. Чтобы настроить компонент формата электронной отчетности, необходимо открыть черновую версию созданной конфигурации электронной отчетности в конструкторе форматов электронной отчетности. Затем добавьте элемент **Excel\\File**, вложите шаблон Word в редактируемый формат электронной отчетности и свяжите этот шаблон с добавленным элементом **Excel\\File**.

> [!NOTE]
> При присоединении шаблона необходимо использовать [тип документа](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), который был ранее [настроен](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) в параметрах электронной отчетности для хранения шаблонов в форматах электронной отчетности.

![Присоединение шаблона к странице конструктора форматов.](./media/er-design-configuration-word-image3.gif)

Можно добавлять вложенные элементы **Excel\\Range** и **Excel\\Cell** для элемента **Excel\\File**, чтобы указать структуру данных, которые будут введены в создаваемые отчеты во время выполнения. После этого эти элементы необходимо связать с источниками данных редактируемого формата электронной отчетности, чтобы указать фактические данные, которые будут введены в создаваемые отчеты во время выполнения.

![Добавление вложенных элементов на странице конструктора форматов.](./media/er-design-configuration-word-image4.gif)

При сохранении изменений в формате электронной отчетности во время разработки иерархическая структура формата хранится в прикрепленном шаблоне Word в виде [пользовательской XML-части](/visualstudio/vsto/custom-xml-parts-overview) с именем **Отчет**. Необходимо получить доступ к измененному шаблону, загрузить его из Finance, сохранить локально и открыть в классическом приложении Word. На следующем рисунке показан образец шаблона, сохраненного локально для контрольного отчета, который содержит пользовательскую XML-часть **Отчет**.

![Предварительный просмотр примера шаблона отчета в классическом приложении Word.](./media/er-design-configuration-word-image5.gif)

Когда привязки элементов формата **Excel\\Range** и **Excel\\Cell** выполняются во время выполнения, данные, обеспечиваемые каждой привязкой, поступают в созданный документ Word как отдельное поле пользовательской XML-части **Отчет**. Для ввода значений из полей пользовательской XML-части в созданный документ необходимо добавить соответствующие [элементы управления содержимым](/office/client-developer/word/content-controls-in-word) Word в ваше шаблон Word, чтобы служить местозаполнителями для данных, которые будут заполнены во время выполнения. Чтобы указать, как заполняются элементы управления содержимым, сопоставьте каждый элемент управления содержимым соответствующему полю пользовательской XML-части **Отчет**.

![Добавление и сопоставление элементов управления содержимым в классическом приложении Word.](./media/er-design-configuration-word-image6.gif)

Затем необходимо заменить исходный шаблон Word редактируемого формата электронной отчетности на измененный шаблон, который теперь содержит элементы управления содержимым Word, сопоставленные полям пользовательской XML-части **Отчет**.

![Замена шаблона на странице конструктора форматов.](./media/er-design-configuration-word-image7.gif)

При выполнении настроенного формата электронной отчетности для создания нового отчета используется прикрепленный шаблон Word. Фактические данные хранятся в отчете Word как пользовательская XML-часть с именем **Отчет**. При открытии созданного отчета элементы управления содержимым Word заполняются данными из пользовательской XML-части **Отчет**.

## <a name="frequently-asked-questions"></a>Вопросы и ответы

**Вопрос:** я настроил формат электронной отчетности для печати документа Word, содержащего адрес компании. В шаблоне Word для этого формата электронной отчетности я вставил элемент управления содержимым в формате RTF, чтобы представить адрес компании. В Finance я ввел адрес компании в виде многострочного текста и выбрал **Ввод** для добавления возврата каретки для каждой введенной строки. Поэтому я ожидал, что адрес компании появится в виде многострочного текста в созданных документах. Однако адрес отображается в виде одной строки текста, которая содержит специальные символы вместо возврата каретки. Что неправильно с моими настройками?

**Ответ.** Вместо использования элемента управления содержимым в формате RTF необходимо использовать элемент управления содержимым в формате обычного текста и установить флажок **Разрешить возвраты каретки (несколько абзацев)** в свойствах данного элемента управления.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word](./tasks/er-design-configuration-word-2016-11.md)
- [Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
