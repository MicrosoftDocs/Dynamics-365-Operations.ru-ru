---
title: Тип места назначения ER Power BI
description: В этом разделе приводятся сведения о настройке типа места назначения ER Power BI для исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.openlocfilehash: 3355c3bced950f65964b124fee553d8c5b53c6b0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679590"
---
# <a name="power-bi-destination"></a><span data-ttu-id="1bb98-103">Назначение Power BI</span><span class="sxs-lookup"><span data-stu-id="1bb98-103">Power BI destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bb98-104">Можно настроить место назначения Microsoft Power BI для каждого компонента "папка" или "файл" формата электронной отчетности (ER), настроенного для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="1bb98-104">You can configure a Microsoft Power BI destination for each folder or file component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="1bb98-105">В зависимости от настройки места назначения созданный документ сохраняется в настроенной ранее папке SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1bb98-105">Based on the setting of the destination, a generated document is stored in a previously configured SharePoint folder.</span></span>

<span data-ttu-id="1bb98-106">Задайте для параметра **Включено** значение **Да** для использования конфигурации электронной отчетности (ER), чтобы настроить перенос данных из вашего экземпляра Dynamics 365 Finance в службы Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="1bb98-106">Set **Enabled** to **Yes** to use your ER configuration to arrange the transfer of data from your Dynamics 365 Finance instance to Microsoft Power BI services.</span></span> <span data-ttu-id="1bb98-107">Перенесенные файлы хранятся на экземпляре сервера Microsoft SharePoint Server, который должен быть настроен для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1bb98-107">The transferred files are stored on a Microsoft SharePoint Server instance that must be configured for that purpose.</span></span> <span data-ttu-id="1bb98-108">Дополнительные сведения см. в разделе [Настройка электронной отчетности (ER) для загрузки данных в Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="1bb98-108">For more information, see [Configure Electronic reporting (ER) to pull data into Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).</span></span>

<span data-ttu-id="1bb98-109">[![Страница параметров места назначения](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span><span class="sxs-lookup"><span data-stu-id="1bb98-109">[![Destination setting page](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bb98-110">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1bb98-110">Additional resources</span></span>

- [<span data-ttu-id="1bb98-111">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="1bb98-111">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="1bb98-112">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="1bb98-112">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
