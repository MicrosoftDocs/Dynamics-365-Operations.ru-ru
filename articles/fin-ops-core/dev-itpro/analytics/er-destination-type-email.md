---
title: Тип места назначения ER электронной почты
description: В этой теме приводятся сведения о настройке места назначения электронной почты для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019966"
---
# <a name="EmailDestinationType">Место назначения электронной почты</a>

[!include [banner](../includes/banner.md)]

Можно настроить место назначения электронной почты для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов. На основании настройки места назначения созданный документ передается в виде вложения электронной почты.

Задайте для параметра **Включено** значение **Да**, чтобы отправить выходной файл по электронной почте. После включения этого параметра вы можете указать получателей сообщения электронной почты, и также изменить тему и текст сообщения электронной почты. Можно настроить постоянные тексты для темы и текста сообщения электронной почты или можно использовать [формулы](er-formula-language.md) электронной отчетности для динамического создания текстов сообщений электронной почты. 

Адреса электронной почты для электронной отчетности можно настроить двумя способами. Настройка может быть выполнена так же, как она выполняется средством управления печатью, или можно разрешить адрес электронной почты, используя прямую ссылку на конфигурацию ER через формулу.

[![Включить место назначения электронной почты](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Типы адреса электронной почты

При выборе **Изменить** для поля **Кому** или **Cc** открывается диалоговое окно **Кому**. Затем можно выбрать тип адреса электронной почты для использования. Типы электронной почты **Конфигурационное сообщение эл. почты** и **Управление печатью** в настоящее время поддерживаются.

[![Выбор типа электронной почты](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Управление печатью

При выборе типа электронной почты **Управление печатью** можно ввести фиксированные адреса электронной почты в поле **Кому**. 

[![Настройка фиксированных адресов электронной почты](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Чтобы использовать нефиксированные адреса электронной почты, необходимо выбрать тип источника электронной почты для места назначения файла. Поддерживаются следующие значения: **Клиент**, **Поставщик**, **Перспективный клиент**, **Контакт**, **Конкурент**, **Работник**, **Кандидат**, **Потенциальный поставщик** и **Неодобренный поставщик**. После выбора типа источника электронной почты нажмите кнопку рядом с полем **Исходная учетная запись эл. почты**, чтобы открыть форму **Конструктор формул**. Можно использовать эту форму, чтобы приложить формулу, возвращающую во время выполнения **счет субъекта** выбранного типа источника из обработанного документа в место назначения электронной почты.

[![Настройка учетной записи источника электронной почты](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Формулы зависят от конфигурации электронной отчетности. В поле **Формула** введите характерную для конкретного документа ссылку на тип субъекта клиента или поставщика. Вместо печати можно найти узел источника данных, который представляет счет клиента или поставщика, и выбрать **Добавить источник данных**, чтобы обновить формулу. Пример, при использовании конфигурации **перемещения кредита ISO 20022** узел, представляющий счет поставщика, — `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Если ввести строковое значение, например `"DE-001"`, и сохранить формулу, контактному лицу поставщика будет направлено сообщение электронной почты, **DE-001**.


[![Страница конструктора формул ER](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Настройка учетной записи источника электронной почты](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Конфигурационное сообщение эл. почты

Используйте этот тип электронной почты, если конфигурация, которую вы используете, имеет узел в источниках данных, который возвращает **адрес электронной почты**. Можно использовать источники данных и функции в конструкторе формул, чтобы получить адрес электронной почты в правильном формате. Пример, при использовании конфигурации **перемещения кредита ISO 20022** узел, представляющий адрес электронной почты контактного лица поставщика, — `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Настройка источника адреса электронной почты](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)
- [Конструктор формул в электронной отчетности (ER)](general-electronic-reporting-formula-designer.md)