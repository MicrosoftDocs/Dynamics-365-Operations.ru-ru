---
title: Настройка банковских счетов (Россия)
description: В этой статье содержится информация о локальных параметрах и необходимых условиях для банковских модулей для России.
author: AdamTrukawka
ms.date: 12/06/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.search.form: BankGroup, BankAccountTable
ms.openlocfilehash: 32c6490ac7f5800b3361822f164d026b829a9b82
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277142"
---
# <a name="set-up-bank-accounts-russia"></a>Настройка банковских счетов (Россия)

[!include [banner](../includes/banner.md)]

Прежде чем работать с рабочей областью **Управление банками**, необходимо выполнить следующие процедуры, чтобы обеспечить соблюдение предварительных условий, необходимых для использования банковских счетов в юридических лицах в России.

## <a name="create-a-bank-manually-or-update-information-for-a-bank"></a>Создание банка вручную или обновления сведений для банка

1. Перейдите в раздел **Управление банком и кассовыми операциями > Настройка > Банковские группы**.
2. Выберите банк или создайте новый. 
2. Введите характерную для России информацию для банка.  
   - **БИК** — банковский идентификационный код. 
   - **Корр. счет банка** — счет в банке-корреспонденте.
   - **Тип банка** — выберите **Основной**, **Зарубежный** или **Филиал**. Если вы выбрали **Зарубежный**, выберите **Счет поставщика** на экспресс-вкладке **Общие**. Если вы выбрали **Филиал**, выберите значение в поле **Основной банк**.
3. (Необязательно) Выберите шаблон в формате DOCX для использования в поле **Валютное платежное поручение** на экспресс-вкладке **Настройка**. Если этот шаблон определен, он будет использоваться по умолчанию для платежного поручения в валюте для всех зарубежных банковских счетов, связанных с этим банком.

> [!NOTE]
> Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись. Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.


## <a name="create-banks-by-importing-a-list-of-banks"></a>Создание банков путем импорта списка банков

### <a name="prerequisites"></a>Необходимые условия

1.  Импортируйте файл конфигурации электронной отчетности "Каталог БИК банков (RU)" из Microsoft Dynamics Lifecycle Services (LCS).
Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2. Перейдите в раздел **Управление банком и кассовыми операциями > Настройка > Параметры управления банком и кассовыми операциями**. На экспресс-вкладке **Общие** в группе полей **Импорт списка банков** в поле **Импорт конфигурации формата** выберите конфигурацию электронной отчетности "Каталог БИК банков (RU)".


### <a name="import-a-list-of-banks"></a>Импорт списка банков

Выберите **Управление банком и кассовыми операциями > Настройка > Банковские группы** и щелкните **Загрузить список банков**. Открывается диалоговое окно **Импорт данных**.

Список банков может быть обновлен для отмеченных регионов или только для выбранных банков.

В верхней области диалогового окна **Импорт данных** отметьте регионы для импорта или обновлении всех банков из помеченных регионов.
В нижней области диалогового окна **Импорт данных** используйте следующие кнопки, чтобы выбрать банки, которые будут включены в обновление:
  - **Выбрать существующий** — выбор и обновление банков, которые существуют в системе.
  - **Выбрать все** — выбор и обновление всех банков, которые выбраны.
  - **Очистить все** — очистить все банки. 

## <a name="create-a-bank-account"></a>Создание банковского счета

1. Создайте новый банковский счет, выбрав **Управление банком и кассовыми операциями > Банковские счета > Банковские счета**.
2. Заполните все обязательные поля. В следующем списке приведены некоторые поля, которые могут быть обязательными. 
    - **Банковский счет** (код)
    - **Номер банковского счета**
    - **Счет ГК** — это счет главной книги, используемый для разноски.
    - **Валюта**
    - **SWIFT-код** 

  Дополнительные сведения см. в разделе [Рабочая область управления банками](../cash-bank-management/bank-management-workspace.md).

3. Введите информацию, характерную для России: 
    - Выберите **Банк** в поле **Банковские группы**. Убедитесь, что поля **БИК** и **Корр. счет банка** заполнены правильно. Также проверьте содержимое полей **Адрес** и **Контактная информация** на соответствующих экспресс-вкладках и откорректируйте его соответствующим образом.
    - Задайте номерную серию для создания платежных поручений в поле **Нумерация П/П**.
    - Для банковских счетов в иностранной валюте можно также определить шаблоны DOCX для создания платежных поручений в бумажном формате в следующих полях: **Валютное платежное поручение**, **Шаблон поручения (продажа валюты)** и **Шаблон поручения (покупка валюты)**. 

> [!NOTE]
> Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись. Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.

![Банковский счет.](media/rus-bank-account.jpg)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
