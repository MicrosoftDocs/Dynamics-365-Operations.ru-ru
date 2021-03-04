---
title: Тип места назначения ER принтера
description: В этой теме приводятся сведения о настройке места назначения принтера для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов в формате PDF или Microsoft Office (Excel, Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679614"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Назначение принтера

[!include [banner](../includes/banner.md)]

Созданный документ можно отправить непосредственно на сетевой принтер для непосредственной печати.

## <a name="prerequisites"></a>Необходимые условия

Перед началом необходимо установить и настроить агент маршрутизации документов, а затем зарегистрировать сетевые принтеры. Дополнительные сведения см. в [Установка агента маршрутизации документов для включения сетевой печати](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Убедитесь, что место назначения принтера доступно

Чтобы сделать место назначения **Принтер** доступным в текущем экземпляре Microsoft Dynamics 365 Finance, перейдите в рабочую область **Управление функциями** и включите следующие функции в следующем порядке:

1. Преобразовать исходящие документы электронной отчетности из форматов Microsoft Office в PDF
2. Агент маршрутизации документов как назначение электронной отчетности для исходящих документов

[![Включение функции места назначения ER принтера в управлении функциями](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Применимость

Место назначения **Принтер** может быть настроено только для тех компонентов файлов, которые используются для создания выходных данных в формате PDF для печати (слияние PDF или формат PDF) или Microsoft Office Excel/Word (файл Excel). При создании выходных данных в формате PDF они отправляются на принтер. Когда выходные данные создаются в формате Microsoft Office, они автоматически преобразуются в формат PDF и затем отправляются на принтер.

### <a name="limitations"></a>Ограничения

Эта функция предназначена для предварительного просмотра и подчиняется условиям использования, которые описаны в [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).

Место назначения **Принтер** реализовано только для развертываний в облаке.

### <a name="use-the-printer-destination"></a>Использование места назначения принтера

1. Установите для параметра **Включен** задано значение **Да**, чтобы отправить созданный документ на принтер.
2. В поле **Имя принтера** выберите нужный сетевой принтер.
3. Задайте для **Сохранить в архиве печати?** значение **Да** для сохранения созданных выходных данных в архиве печати, чтобы они были доступны для дальнейшей печати. Чтобы получить доступ к архивированным выходным данным позже, перейдите **Управление организацией** \> **Запросы и отчеты** \> **Архив отчетов**.

[![Использование места назначения принтера](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Параметр **Преобразовать в PDF** не должен быть включен при настройке места назначения **Принтер**. Преобразование PDF для печати выполняется даже в том случае, если этот параметр отключен.

Чтобы использовать определенную [ориентацию страницы](electronic-reporting-destinations.md#SelectPdfPageOrientation) при печати исходящего документа в формате Excel, необходимо включить параметр **Преобразовать в PDF**. При установке для параметра **Преобразовать в PDF** значения **Да**, поле **Ориентации страницы** становится доступным. В поле **Ориентация страницы** можно выбрать ориентацию страницы.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]