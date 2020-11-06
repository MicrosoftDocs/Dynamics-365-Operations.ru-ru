---
title: Проверка настройки двойной записи в приложениях Finance and Operations и Common Data Service
description: В этой теме объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997238"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="8f590-103">Проверка настройки двойной записи в приложениях Finance and Operations и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8f590-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8f590-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8f590-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="8f590-105">Конкретно, в ней объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8f590-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="8f590-106">Проверка настройки двойной записи в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8f590-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="8f590-107">Чтобы определить, возникают ли ошибки, отображаемые при попытке сохранить записи для обновления, в результате двойной записи, сначала убедитесь, что двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="8f590-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="8f590-108">Если у вас есть права администратора в приложении Finance and Operations, перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="8f590-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="8f590-109">Если отображаются сведения о связанных средах и список выполняемых сопоставлений объектов, двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="8f590-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Проверка подключения приложения Finance and Operations при наличии прав администратора](media/verify_fin_ops_1.png)

+ <span data-ttu-id="8f590-111">Если у вас нет прав администратора, вы получите сообщение об ошибке *Невозможно записать данные в объект \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="8f590-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="8f590-112">В примере на следующем рисунке невозможно создать запись клиента в приложении Finance and Operations, так как настроена двойная запись, но отсутствуют ссылочные данные группы клиентов и условий оплаты в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8f590-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Проверка подключения приложения Finance and Operations при отсутствии прав администратора](media/verify_fin_ops_2.png)

<span data-ttu-id="8f590-114">Сведения об устранении проблем при создании данных в приложениях Finance and Operations см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="8f590-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="8f590-115">Проверка настройки двойной записи в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8f590-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="8f590-116">Если при создании данных вы видите поле **Компания** на страницах в Common Data Service, двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="8f590-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Проверка подключения Common Data Service](media/verify_cds.png)

<span data-ttu-id="8f590-118">Сведения об устранении проблем при создании данных в Common Data Service см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="8f590-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="8f590-119">Сведения о том, как просмотреть подробные сведения об ошибке при возникновении каких-либо ошибок во время создания данных в Common Data Service см. в разделе [Включение и просмотр журнала трассировки подключаемого модуля в Common Data Service для просмотра подробных сведений об ошибке](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="8f590-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
