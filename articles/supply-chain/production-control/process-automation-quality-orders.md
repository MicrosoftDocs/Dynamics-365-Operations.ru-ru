---
title: Вызов потоков автоматизации процессов для создания заказов контроля качества
description: В этой теме приводятся ресурсы для использования Power Automate для автоматизации бизнес-процессов с использованием примера заказов контроля качества.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115213"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="15e7e-103">Вызов потоков автоматизации процессов для создания заказов контроля качества</span><span class="sxs-lookup"><span data-stu-id="15e7e-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="15e7e-104">Организации имеют увеличивающую потребность в автоматизации стандартных бизнес-процессов, обеспечивают более удобное взаимодействие с персоналом и используют различные сигналы данных и системы для автоматического ведения бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="15e7e-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="15e7e-105">Используя роботизированную автоматизацию процессов (RPA) и Microsoft Power Automate, компании могут использовать интерфейс без написания кода для автоматизации повторяющихся процессов, тем самым получая эффективность и точность работы.</span><span class="sxs-lookup"><span data-stu-id="15e7e-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="15e7e-106">Загружаемый шаблон решения по автоматизации для Supply Chain Management — это демонстрация того, как Power Automate можно использовать для автоматизации бизнес-процессов, использующая в качестве примера заказы контроля качества.</span><span class="sxs-lookup"><span data-stu-id="15e7e-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="15e7e-107">Шаблон решения по автоматизации можно загрузить [здесь](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="15e7e-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="15e7e-108">Обзор этой функции и ее возможностей см. в следующем видеоролике: [Использование RPA для создания заказов контроля качества в Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="15e7e-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="15e7e-109">![Параметры автоматизации с RPA](media/rpa-automation-options.png "Параметры автоматизации с RPA")</span><span class="sxs-lookup"><span data-stu-id="15e7e-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="15e7e-110">Шаблон решения Power Automate включает поток автоматизации в облаке и поток локальной автоматизации, который автоматизирует создание заказов контроля качества в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="15e7e-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="15e7e-111">Автоматизация может быть запущена в ответ на множество событий и сигналов, в том числе на ввод пользователем или сигналов с оборудования (в том числе Интернет вещей).</span><span class="sxs-lookup"><span data-stu-id="15e7e-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="15e7e-112">Пример приложения Power *Q-Ordering* включен в шаблон решения.</span><span class="sxs-lookup"><span data-stu-id="15e7e-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="15e7e-113">Он позволяет пользователю сканировать QR-код номенклатуры, вводить количество и прикладывать изображения с помощью камеры.</span><span class="sxs-lookup"><span data-stu-id="15e7e-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="15e7e-114">Параметры решения включаются для настройки автоматизации для конкретного варианта использования в производственном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="15e7e-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="15e7e-115">![Создать заказ для контроля качества](media/rpa-create-quality-roder.png "Создать заказ для контроля качества")</span><span class="sxs-lookup"><span data-stu-id="15e7e-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="15e7e-116">Чтобы получить подробные пошаговые инструкции по загрузке, установке и использованию образца решения для автоматизации создания заказа контроля качества, см. раздел [Автоматизация создания заказа контроля качества в Dynamics 365 Supply Chain Management с помощью роботизированной автоматизации процессов с использованием Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="15e7e-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

