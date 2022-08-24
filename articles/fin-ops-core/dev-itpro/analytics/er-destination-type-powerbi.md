---
title: Тип места назначения ER Power BI
description: В этой статье содержится информация о том, как настроить тип места назначения ER Power BI для исходящих документов.
author: kfend
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 8d167d6749e2f05f1e263839260dfdb563d2bbea
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285376"
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
