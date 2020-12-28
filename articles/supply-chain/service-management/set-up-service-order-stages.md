---
title: Настройка этапов заказа на обслуживания
description: Настройка этапов заказа на обслуживания.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86d60a67b60b1bd3a13666b35f729f88ecfee3d3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435712"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="07714-103">Настройка этапов заказа на обслуживания</span><span class="sxs-lookup"><span data-stu-id="07714-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="07714-104">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Заказы на обслуживание** \> **Этапы сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="07714-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="07714-105">Нажмите клавиши CTRL+N, чтобы создать новую запись.</span><span class="sxs-lookup"><span data-stu-id="07714-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="07714-106">В полях **Этап сервисного обслуживания** и **Описание** укажите код и описание этапа обслуживания.</span><span class="sxs-lookup"><span data-stu-id="07714-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="07714-107">Выберите соответствующие параметры для этапа.</span><span class="sxs-lookup"><span data-stu-id="07714-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="07714-108">Выберите для текущего этапа родительский этап или оставьте поле **Родитель** пустым, если данный этап является начальным в настройке этапов.</span><span class="sxs-lookup"><span data-stu-id="07714-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07714-109">После сохранения этапа поле <STRONG>Родитель</STRONG> изменить невозможно.</span><span class="sxs-lookup"><span data-stu-id="07714-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="07714-110">Вместо этого следует удалить запись и снова создать запись с другим значением в поле <STRONG>Родитель</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="07714-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="07714-111">Кроме того, можно создать только один этап с пустым полем <STRONG>Родитель</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="07714-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="07714-112">Другими словами, разрешено создание только одного начального этапа.</span><span class="sxs-lookup"><span data-stu-id="07714-112">That is, only one initial stage is permitted.</span></span></P>


  


