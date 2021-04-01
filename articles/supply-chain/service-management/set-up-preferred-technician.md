---
title: Настройка предпочтительного технического специалиста
description: Можно выбрать любого работника в качестве предпочтительного специалиста для соглашения о сервисном обслуживании или заказа на сервисное обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b2554197c1963cdd7ba0871edb532661d10945
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256071"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="91a08-103">Настройка предпочтительного технического специалиста</span><span class="sxs-lookup"><span data-stu-id="91a08-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="91a08-104">Можно выбрать любого работника в качестве предпочтительного специалиста для соглашения о сервисном обслуживании или заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="91a08-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="91a08-105">Однако имеет смысл добавить работника к соответствующей группе исполнения, чтобы работник был включен в разделе **Панель исполнения**.</span><span class="sxs-lookup"><span data-stu-id="91a08-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="91a08-106">Назначение сотрудника команде подготовки к отправке</span><span class="sxs-lookup"><span data-stu-id="91a08-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="91a08-107">Щелкните **Управление персоналом** \> **Общий** \> **Работники** \> **Работники**.</span><span class="sxs-lookup"><span data-stu-id="91a08-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="91a08-108">Дважды щелкните по имени работника, чтобы открыть страницу подробных сведений о работнике.</span><span class="sxs-lookup"><span data-stu-id="91a08-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="91a08-109">В разделе **Панель операций** щелкните **Настройка** \>**Группа исполнения**, чтобы открыть форму **Подготовка работников к отправке**.</span><span class="sxs-lookup"><span data-stu-id="91a08-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="91a08-110">В поле **Группа исполнения** выберите группу, для которой необходимо назначить работника.</span><span class="sxs-lookup"><span data-stu-id="91a08-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="91a08-111">Назначение предпочтительного специалиста к соглашению на обслуживание</span><span class="sxs-lookup"><span data-stu-id="91a08-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="91a08-112">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="91a08-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="91a08-113">Дважды щелкните соглашение о сервисном обслуживании, чтобы открыть форму подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="91a08-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="91a08-114">На вкладке **Общие** выберите поле **Предпочитаемый техник** и выберите члена подходящей группы исполнения предпочтительного специалиста для соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="91a08-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="91a08-115">Назначение предпочтительного специалиста к соглашению на обслуживание</span><span class="sxs-lookup"><span data-stu-id="91a08-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="91a08-116">Щелкните **Управление сервисным обслуживанием** \> **Периодические операции** \> **Панель исполнения**.</span><span class="sxs-lookup"><span data-stu-id="91a08-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="91a08-117">В форме <STRONG>Панель исполнения</STRONG> укажите диапазон дат для мероприятий по исполнению, которые необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="91a08-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="91a08-118">Кроме того, укажите, необходимо ли отображать закрытые мероприятия и необходимо ли ограничить мероприятие по подготовке к отправке командами, к которым вы относитесь или которые вы уполномочены отслеживать.</span><span class="sxs-lookup"><span data-stu-id="91a08-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="91a08-119">Нажмите <STRONG>OK</STRONG>, чтобы открыть диалоговое окно <STRONG>Панель исполнения</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="91a08-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="91a08-120">Выберите строку действия по сервисному обслуживанию, которое необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="91a08-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="91a08-121">На вкладке **Связанные** используйте список **Работник** для назначения члена подходящей группы исполнения в качестве предпочитаемого специалиста для сервисного вызова.</span><span class="sxs-lookup"><span data-stu-id="91a08-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="91a08-122">См. также</span><span class="sxs-lookup"><span data-stu-id="91a08-122">See also</span></span>

[<span data-ttu-id="91a08-123">Обзор разработки и создания соглашений о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="91a08-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="91a08-124">Создание заказов на сервисное обслуживание вручную</span><span class="sxs-lookup"><span data-stu-id="91a08-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="91a08-125">[Соглашения на обслуживании (форма)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="91a08-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]