---
title: Изменение форматов путем повторного применения шаблонов Excel
description: Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML".
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24eb64679b458d14e30dc5b4365c7305d71cfc4c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754898"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Изменение форматов путем повторного применения шаблонов Excel

[!include [banner](../../includes/banner.md)]

Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML".

Эта процедура показывает, как изменить конфигурацию формата электронной отчетности путем применения шаблона Microsoft Excel с внесенными изменениями. В этой процедуре вам предстоит импортировать измененный шаблон Excel в конфигурации формата шаблона электронной отчетности, созданные для демонстрационной компании Litware, Inc., а затем сформировать электронные документы. Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности". Действия можно выполнять с использованием набора данных GBSI. Прежде чем начать, загрузите и сохраните файл SampleVendPaymWsReport2.xlsx, который указан в разделе справки "Изменение формата электронной отчетности путем повторного применения шаблона Excel" (modify-electronic-reporting-format-reapply-excel-template/).

1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
    * Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный. Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".  

## <a name="select-the-er-format"></a>Выбор формата электронной отчетности
1. Щелкните "Конфигурации отчетности".
2. В дереве разверните узел "Модель платежа".
3. В дереве выберите "Модель платежа\Пример отчета о листе".
4. Нажмите кнопку Вложения.
    * Обратите внимание, что файл SampleVendPaymWsReport.xlsx Excel в настоящее время используется в качестве шаблона для обработки журнала платежей.   
5. Щелкните Открыть.
    * Щелкните "Открыть", чтобы просмотреть макет шаблона Excel.  
    * Просмотрите шаблон. Обратите внимание, что в настоящее время он включает следующие сведения для каждой строки платежа: номер счета поставщика, имя поставщика, банк, внутренний номер, номер счета, дебет, кредит и валюту. В данном примере мы хотим расширить их список путем добавления сведений о дате платежа.   
6. Закройте страницу.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Повторное применение нового шаблона Excel к формату электронной отчетности
1. Выберите Конструктор.
    * Откройте черновую версию выбранного формата электронной отчетности для редактирования.  
2. В области действий щелкните "Импорт".
3. Щелкните "Обновление из Excel".
    * Щелкните "Обновить шаблон" и выберите файл SampleVendPaymWsReport2.xlsx.  
    * Щелкните "Обновить шаблон" и выберите ранее загруженный файл SampleVendPaymWsReport2.xlsx.  
4. Нажмите кнопку "OК".
    * Применяется шаблон SampleVendPaymWsReport2.xlsx. Структура формата электронной отчетности синхронизируется с содержимым шаблона, элементы которого добавляются в формат электронной отчетности. Все существующие элементы в формате электронной отчетности, которые не входят в отчет, удаляются из определения формата.  
5. В дереве выберите "Excel".
    * Обратите внимание, что поле "Шаблон" теперь содержит ссылку на новый шаблон.   
6. Нажмите кнопку Вложения.
7. Щелкните Открыть.
    * Щелкните "Открыть", чтобы просмотреть измененный шаблон Excel.  
    * Просмотрите шаблон. Обратите внимание, что в нем теперь содержится строка для даты платежа.   
8. Закройте страницу.
9. В дереве разверните "Excel".
10. В дереве разверните "Excel\PaymLines".
11. В дереве выберите "Excel\PaymLines\PaymDate".
    * Обратите внимание, что формат электронной отчетности теперь содержит более одного элемента. В шаблон Excel была добавлена ячейка PaymDate.  
12. Перейдите на вкладку "Сопоставление".
13. В дереве разверните узел "model".
14. В дереве разверните узел "model\Payments".
15. В дереве выберите "модель\Платежи\Дата проводки(TransactionDate)".
16. Щелкните "Связать".
    * Укажите, какие данные добавляются в новую ячейку во время выполнения.  
17. Нажмите кнопку "Сохранить".
18. Закройте страницу.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Включение измененной черновой версии формата электронной отчетности для использования при обработке журнала платежей
1. В области действий щелкните "Конфигурации".
2. Щелкните "Параметры пользователя".
3. Выберите "Да" в поле "Запустить настройки".
4. Нажмите кнопку "OК".
5. Щелкните "Изменить".
6. Выберите "Да" в поле "Запустить черновик".

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Использование измененной черновой версии формата электронной отчетности для использования при обработке журнала платежей

Просмотрите созданный лист, включая новый элемент сведений строк платежа — дату платежа.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]