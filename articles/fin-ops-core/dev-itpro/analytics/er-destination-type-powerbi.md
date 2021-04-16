---
title: Тип места назначения ER Power BI
description: В этом разделе приводятся сведения о настройке типа места назначения ER Power BI для исходящих документов.
author: NickSelin
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.openlocfilehash: 964ed05eaba2a4dbba904b4ce0e0be33d0925fb5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753464"
---
# <a name="power-bi-destination"></a>Назначение Power BI

[!include [banner](../includes/banner.md)]

Можно настроить место назначения Microsoft Power BI для каждого компонента "папка" или "файл" формата электронной отчетности (ER), настроенного для создания исходящих документов. В зависимости от настройки места назначения созданный документ сохраняется в настроенной ранее папке SharePoint.

Задайте для параметра **Включено** значение **Да** для использования конфигурации электронной отчетности (ER), чтобы настроить перенос данных из вашего экземпляра Dynamics 365 Finance в службы Microsoft Power BI. Перенесенные файлы хранятся на экземпляре сервера Microsoft SharePoint Server, который должен быть настроен для этой цели. Дополнительные сведения см. в разделе [Настройка электронной отчетности (ER) для загрузки данных в Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).

[![Страница параметров места назначения](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]