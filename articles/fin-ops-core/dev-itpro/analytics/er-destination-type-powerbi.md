---
title: Тип места назначения ER Power BI
description: В этой статье содержится информация о том, как настроить тип места назначения ER Power BI для исходящих документов.
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
ms.openlocfilehash: 50675c15ec1273d6955c36aef87f9aaa846d4247
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845609"
---
# <a name="power-bi-destination"></a>Назначение Power BI

[!include [banner](../includes/banner.md)]

Можно настроить место назначения Microsoft Power BI для каждого компонента "папка" или "файл" формата электронной отчетности (ER), настроенного для создания исходящих документов. В зависимости от настройки места назначения созданный документ сохраняется в настроенной ранее папке SharePoint.

Задайте для параметра **Включено** значение **Да**, чтобы использовать конфигурацию электронной отчетности (ER) для организации перемещения данных из вашего экземпляра Dynamics 365 Finance в службы Microsoft Power BI. Перенесенные файлы хранятся на экземпляре сервера Microsoft SharePoint Server, который должен быть настроен для этой цели. Дополнительные сведения см. в разделе [Настройка электронной отчетности (ER) для загрузки данных в Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).

[![Страница параметров места назначения.](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]