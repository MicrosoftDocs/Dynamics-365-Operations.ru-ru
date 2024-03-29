---
title: Документы обоснования бюджетного плана
description: Документы обоснования предоставляют описания для этих запросов бюджета, чтобы объяснить причину, по которой необходим конкретный бюджет.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711781"
---
# <a name="budget-planning-justification-documents"></a>Документы обоснования бюджетного плана

[!include [banner](../includes/banner.md)]

Документы обоснования предоставляют описания для этих запросов бюджета, чтобы объяснить причину, по которой необходим конкретный бюджет. 

Шаблон бюджетного плана создается менеджером бюджета в Microsoft Word и назначается текущему процессу планирования бюджета. Владельцы бюджета могут затем открыть шаблон, и данные будут автоматически заполнены в Word на основе их запроса бюджета. Затем они могут добавить дополнительный текст или данные перед сохранением и присоединить свои персональные документы обоснования к бюджетному плану.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Настройка надстройки Microsoft Dynamics Office Add-in для Microsoft Word

1.  Откройте новый документ Microsoft Word.
2.  Щелкните **Вставить** на ленте, затем щелкните **Магазин**.
3.  Найдите надстройку Microsoft Dynamics Office Add-in и щелкните **Добавить**.
4.  В Word в области справа щелкните **Добавить сведения о сервере**.
5.  Введите или вставьте URL-адрес сервера и нажмите кнопку **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Определение шаблона обоснования в Microsoft Word

1.  После входа щелкните **Дизайн** в надстройке Microsoft Dynamics Office Add-in.
2.  Для сведений заголовка используйте кнопку **Добавить поля**.
3.  Выберите источник данных объекта BudgetPlanJustification и нажмите кнопку **Далее**. **Примечание:** Этот объект является обязательным для любого документа обоснования. Другие объекты могут использоваться, но отправка обратно в Microsoft Dynamics 365 Finance не будет выполняться, если этот объект не будет включен.
4.  Добавьте метки BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter и DocumentNumber в документ Word. **Примечание:** При необходимости вместо стандартных меток можно использовать свои собственные пользовательские метки.
5.  Щелкните **Готово** для завершения раздела заголовка.
6.  Для сведений уровня строки по суммам бюджетного плана щелкните **Добавить таблицу**.
7.  Снова выберите источник данных объекта BudgetPlanJustification и нажмите кнопку **Далее**.
8.  Добавьте поля для EffectiveDate, ScenarioName, AccountDisplayValue и AccountingCurrencyExpenseAmount. **Примечание:** Если комментарии могут добавляться в отдельные строки бюджетного плана, их можно добавить в таблицу здесь.
9.  Добавьте любые дополнительные инструкции конечному пользователю и задайте все необходимое форматирование или стили в документе.
10. Сохраните документ на локальном компьютере и закройте файл перед продолжением.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Настройка процесса бюджетного планирования для использования в шаблоне обоснования

1.  Откройте **Бюджетирование** &gt; **Настройка** &gt; **Бюджетное планирование** &gt; **Шаблоны документов обоснования**.
2.  Щелкните **Создать** и перейдите в только что созданный документ Microsoft Word.
3.  Введите отображаемое имя и описание шаблона. Нажмите кнопку **ОК**.
4.  Перейдите в раздел **Бюджетирование** &gt; **Настройка** &gt; **Бюджетное** **планирование** &gt; **Конфигурация бюджетного планирования**.
5.  Выберите процесс, в котором следует использовать шаблон обоснования, и нажмите **Изменить**.
6.  В поле **Шаблон документа обоснования** выберите соответствующий шаблон и сохраните.

##### <a name="edit-and-save-personalized-justification-documents"></a>Изменение и сохранение персональных документов обоснования

1.  Создайте новый бюджетный план или откройте существующий бюджетный план.
2.  В раскрывающемся меню **Обоснование** выберите **Создать новое обоснование**.
3.  После заполнения сведений выберите отправку персонализированного документа из раскрывающегося меню **Обоснование**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
