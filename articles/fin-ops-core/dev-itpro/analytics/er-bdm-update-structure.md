---
title: Обновление структуры шаблона бизнес-документа
description: В этой теме объясняется, как обновить структуру шаблона бизнес-документа с помощью функции управления бизнес-документами.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750492"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Обновление структуры шаблона бизнес-документа 

[!include[banner](../includes/banner.md)]

В области **Структура шаблона** редактора шаблонов [Управление бизнес-документами](er-business-document-management.md) можно изменить шаблон бизнес-документа, [добавляя новые поля](er-bdm-add-field-to-excel-template.md) в шаблон в Microsoft Excel. Структура шаблона затем автоматически обновляется в Dynamics 365 Finance, так что она отражает изменения, внесенные в области **Структура шаблона**.

Имеется также возможность изменить шаблон с помощью функций Office 365 Online. Например, можно добавить на редактируемый лист новый именованный элемент, например рисунок или фигуру. В этом случае структура шаблона не обновляется автоматически в Finance, и добавленный элемент не отображается в области **Структура шаблона**. Обновите структуру шаблона вручную в Finance, выбрав **Обновить структуру** на странице редактора шаблонов.

Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Пример. Обновление структуры шаблона бизнес-документа

В этом примере показано, как системный администратор может обновить структуру шаблона бизнес-документа в модуле Finance после изменения шаблона в Office Online. В следующих разделах описаны выполняемые шаги.

### <a name="prepare-a-business-document-template-for-editing"></a>Подготовка шаблона бизнес-документа для редактирования

Выполните следующие процедуры в разделе [Обзор управления бизнес-документами](er-business-document-management.md).

1. [Настройка параметров ER](er-business-document-management.md#configure-er-parameters)
2. [Импорт решений электронной отчетности](er-business-document-management.md#import-er-solutions)
3. [Включение управления бизнес-документами](er-business-document-management.md#enable-business-document-management)
4. [Настроить параметры](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Редактирование шаблона бизнес-документа

1. В рабочей области **Управление бизнес-документами** выберите **Создать документ**.
2. На странице **Создание нового шаблона** выберите шаблон **Накладная с произвольным текстом (пример электронной отчетности) (Excel)**.
3. Выберите **Создать документ**.
4. В поле **Заголовок** введите **Образец FTI Litware**
5. Выберите **ОК** для создания нового шаблона.

    > [!NOTE]
    > Если вы еще не выполнили вход в Office Online, вы [переходите на страницу входа Office 365](er-business-document-management.md#frequently-asked-questions). Чтобы вернуться в среду Finance, нажмите кнопку **Назад** в браузере.

    Новый шаблон открывается для редактирования во встроенном элементе управления Excel Online на странице редактора шаблонов.

[![Использование рабочей области управления бизнес-документами для запуска редактирования шаблона бизнес-документа](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Просмотр текущей структуры редактируемого шаблона

1. В Excel Online на ленте на вкладке **Вид** в группе **Показать** выберите пункт **Линии сетки**.
2. В редактируемом шаблоне выберите прямоугольник над заголовком шаблона. Этот прямоугольник представляет собой рисунок с именем **rptHeaderCompLogo**.
3. Если панель **Структура шаблона** скрыта, выберите **Показать структуру**.
4. В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.
5. Обратите внимание, что в структуре шаблонов в Finance элемент **rptHeaderCompLogo** представляется в качестве дочернего элемента **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.

[![Использование рабочей области управления бизнес-документами для просмотра текущей структуры редактируемого шаблона](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Обновление структуры шаблона бизнес-документа путем удаления рисунка

1. В Excel Online в редактируемом шаблоне выберите изображение **rptHeaderCompLogo**.
2. Выполните одно из следующих действий, чтобы удалить выбранный рисунок из редактируемого шаблона:

    - Выберите клавишу **DELETE** на клавиатуре.
    - Выберите и удерживайте (или щелкните правой кнопкой мыши) рисунок, затем выберите **Вырезать**.

    > [!NOTE]
    > Элемент **rptHeaderCompLogo** в настоящее время все еще присутствует в структуре шаблона в Finance, хотя рисунок больше не включен в шаблон Excel.

3. Выберите **Обновить структуру** для синхронизации структуры редактируемого шаблона в Excel и Finance.
4. В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.
5. Обратите внимание, что элемент **rptHeaderCompLogo** больше не включен в структуру шаблонов в модуле Finance.

[![Использование рабочей области управления бизнес-документами для удаления рисунка из шаблона бизнес-документа](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Обновление структуры шаблона бизнес-документа путем добавления рисунка

1. В Excel Online на ленте на вкладке **Вставить** в группе **Иллюстрации** выберите пункт **Рисунок**.
2. Выберите **Выбрать файл**, перейдите к изображению, которое необходимо добавить, выберите его и затем выберите **ОК**.
3. Выберите **Вставить**.
4. Переместите новый рисунок, пока он не будет в нужном месте. По умолчанию Excel задаем имя рисунка. Например, это может быть имя рисунка **Рисунок 2**.
5. Выберите **Обновить структуру** для синхронизации структуры редактируемого шаблона в Excel и Finance.
6. В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.
7. Обратите внимание, что новый рисунок теперь включен как элемент в структуру шаблона в модуле Finance.

[![Использование рабочей области управления бизнес-документами для добавления рисунка в шаблон бизнес-документа](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Связанные ссылки

[Обзор электронной отчетности (ER)](general-electronic-reporting.md)

[Обзор управления бизнес-документами](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]