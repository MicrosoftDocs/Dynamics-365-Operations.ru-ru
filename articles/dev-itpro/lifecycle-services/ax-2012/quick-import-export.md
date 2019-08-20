---
title: Быстрый импорт и экспорт
description: С помощью быстрого импорта/экспорта можно импортировать и экспортировать, выполняя меньшее число шагов.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 7655de1399c49328bae1736c796325e546796bd5
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850521"
---
# <a name="quick-import-export"></a><span data-ttu-id="c8d92-103">Быстрый импорт и экспорт</span><span class="sxs-lookup"><span data-stu-id="c8d92-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8d92-104">С помощью быстрого импорта/экспорта можно импортировать и экспортировать, выполняя меньшее число шагов.</span><span class="sxs-lookup"><span data-stu-id="c8d92-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="c8d92-105">Мы добавили функцию быстрого импорта и экспорта, которая позволяет пользователям быстро импортировать или экспортировать простые задания, которые они хотят выполнить.</span><span class="sxs-lookup"><span data-stu-id="c8d92-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="c8d92-106">В идеале эта функция используется в сценариях, в которых файл автоматически сопоставляется с системой и пользователю не нужно выполнять расширенное сопоставление или создавать повторяющиеся задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="c8d92-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="c8d92-107">Эта функция поддерживает работу с готовыми и пользовательскими объектами.</span><span class="sxs-lookup"><span data-stu-id="c8d92-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="c8d92-108">Можно выполнять импорт из файлов, а при использовании источника данных ODBC можно выбрать запрос для определения импорта.</span><span class="sxs-lookup"><span data-stu-id="c8d92-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="c8d92-109">Необходимо предварительно определить форматы источников данных для AX или файла и знать, где они расположены.</span><span class="sxs-lookup"><span data-stu-id="c8d92-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="c8d92-110">Нет необходимости создавать группу обработки для использования быстрого импорта или экспорта, поскольку она создается автоматически системой при выполнении задания импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="c8d92-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="c8d92-111">Кроме того, можно хранить историю данных, импортированных с помощью быстрого импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="c8d92-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="c8d92-112">Обратите внимание, что быстрый импорт/экспорт предполагает, что вы знакомы с понятиями DIXF.</span><span class="sxs-lookup"><span data-stu-id="c8d92-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>



