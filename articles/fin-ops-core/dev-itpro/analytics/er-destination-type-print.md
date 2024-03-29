---
title: Тип места назначения ER принтера
description: В этой статье объясняется, как можно настроить место назначения "принтер" для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER).
author: kfend
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7e01476b85c6c35d7c36c90db4d64ab2a2930fec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271745"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Назначение принтера

[!include [banner](../includes/banner.md)]

Созданный документ можно отправить непосредственно на сетевой принтер для непосредственной печати.

## <a name="prerequisites"></a>Необходимые условия

Перед началом необходимо установить и настроить агент маршрутизации документов, а затем зарегистрировать сетевые принтеры. Дополнительные сведения см. в [Установка агента маршрутизации документов для включения сетевой печати](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Убедитесь, что место назначения принтера доступно

Чтобы сделать место назначения **Принтер** доступным в текущем экземпляре Microsoft Dynamics 365 Finance, перейдите в рабочую область **Управление функциями** и включите следующие функции в следующем порядке:

1. Преобразовать исходящие документы электронной отчетности из форматов Microsoft Office в PDF
2. Агент маршрутизации документов как назначение электронной отчетности для исходящих документов

[![Включение функции места назначения ER принтера в управлении функциями.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Применимость

#### <a name="pdf-printing"></a>Печать PDF

В версиях Finance до версии 10.0.18 место назначения **Принтер** может быть настроено только для тех компонентов файлов, которые используются для создания выходных данных в формате PDF для печати (элементы формата **Слияние PDF** или **Файл PDF**) или формат Microsoft Office Excel и Word (элемент формата **Файл Excel**). При создании выходных данных в формате PDF они отправляются на принтер. Когда выходные данные создаются в формате Office с помощью элемента формата **Файл Excel**, они автоматически преобразуются в формат PDF и затем отправляются на принтер.

Однако в версии 10.0.18 можно настроить пункт назначения **Принтер** для элемента формата **Обычный файл**. Этот элемент форматирования в основном используется для создания выходных данных в формате TXT или XML. Можно настроить формат электронной отчетности, содержащий элемент формата **Обычный файл** в качестве корневого элемента формата и элемент формата **Двоичное содержимое** в качестве единственного вложенного элемента под ним. В этом случае элемент формата **Обычный файл** будет создавать выходные данные в формате, указанном в привязке, которая настраивается для элемента формата **Двоичное содержимое**. Например, можно настроить эту привязку для [заполнения](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) этого элемента содержимым вложения [Управление документами](../../fin-ops/organization-administration/configure-document-management.md) в формате PDF или Office (Excel или Word). Выходные данные можно распечатать с помощью настроенного пункта назначения **Принтер**. 

> [!NOTE]
> При выборе элемента формата **Общее\\Файл** для настройки пункта назначения **Принтер** нет возможности гарантировать во время разработки, что выбранный элемент будет создавать выходные данные в формате PDF или выводные данные, которые могут быть преобразованы в формат PDF. Поэтому появится следующее предупреждающее сообщение: "Убедитесь, что выходные данные, созданный выбранным компонентом формата, могут быть преобразованы в PDF. В противном случае снимите флажок «Преобразовать в PDF»." Необходимо предпринять шаги, чтобы помочь предотвратить возникновение ошибок во время выполнения, когда для печати во время выполнения предоставляются выходные данные в формате, отличном от PDF, или в формате, который не может быть преобразован в PDF. Если ожидается получение выходных данных в формате Office (Excel или Word), необходимо выбрать параметр **Преобразовать в PDF**.
>
> В версии 10.0.26 и более поздних для использования параметра **Преобразовать в PDF** необходимо выбрать **PDF** для параметра **Тип маршрутизации документа** для настроенного пункта назначения **Принтер**.

#### <a name="zpl-printing"></a>Печать ZPL

В версии 10.0.26 или более поздней можно настроить пункт назначения **Принтер** для элемента формата **Общее\\Файл**, выбрав **ZPL** для параметра **Тип маршрутизации документов**. В этом случае параметр **Преобразовать в PDF** игнорируется во время выполнения, а выходные данные TXT или XML отправляются непосредственно на выбранный принтер с помощью контракта Zebra Programming Language (ZPL) [агента маршрутизации документов (DRA)](install-document-routing-agent.md). Эта функция используется для формата электронной отчетности, который представляет макет этикетки ZPL II для печати различных этикеток.

[![Задание параметра типа маршрутизации документов в диалоговом окне параметров места назначения.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Дополнительные сведения об этой функции см. в разделе [Разработка нового решения электронной отчетности для печати этикеток ZPL II](er-design-zpl-labels.md).

### <a name="limitations"></a>Ограничения

Место назначения **Принтер** реализовано только для развертываний в облаке.

### <a name="use-the-printer-destination"></a>Использование места назначения принтера

1. Установите для параметра **Включен** задано значение **Да**, чтобы отправить созданный документ на принтер.
2. В поле **Имя принтера** выберите нужный сетевой принтер.
3. Задайте для **Сохранить в архиве печати?** значение **Да** для сохранения созданных выходных данных в архиве печати, чтобы они были доступны для дальнейшей печати. Чтобы получить доступ к архивированным выходным данным позже, перейдите **Управление организацией** \> **Запросы и отчеты** \> **Архив отчетов**.

[![Использование места назначения принтера.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Параметр **Преобразовать в PDF** не должен быть включен при настройке места назначения **Принтер**. Преобразование PDF для печати выполняется даже в том случае, если этот параметр отключен.

Чтобы использовать определенную [ориентацию страницы](electronic-reporting-destinations.md#SelectPdfPageOrientation) при печати исходящего документа в формате Excel, необходимо включить параметр **Преобразовать в PDF**. При установке для параметра **Преобразовать в PDF** значения **Да**, поле **Ориентации страницы** становится доступным. В поле **Ориентация страницы** можно выбрать ориентацию страницы.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
