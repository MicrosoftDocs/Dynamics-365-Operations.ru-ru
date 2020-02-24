---
title: Тип места назначения ER принтера
description: В этой теме приводятся сведения о настройке места назначения принтера для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов в формате PDF или Microsoft Office (Excel, Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
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
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019967"
---
# <a name="PrinterDestinationType"></a>Назначение принтера

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

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)
