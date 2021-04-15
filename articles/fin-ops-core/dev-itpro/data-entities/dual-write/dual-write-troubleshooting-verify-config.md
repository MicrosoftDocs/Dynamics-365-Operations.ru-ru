---
title: Проверка конфигурации двойной записи в приложениях Finance and Operations и Dataverse
description: В этой теме объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748857"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="0ef53-103">Проверка конфигурации двойной записи в приложениях Finance and Operations и Dataverse</span><span class="sxs-lookup"><span data-stu-id="0ef53-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0ef53-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef53-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0ef53-105">Конкретно, в ней объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef53-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="0ef53-106">Проверка настройки двойной записи в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0ef53-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="0ef53-107">Чтобы определить, возникают ли ошибки, отображаемые при попытке сохранить строки для обновления, в результате двойной записи, сначала убедитесь, что двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="0ef53-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="0ef53-108">Если у вас есть права администратора в приложении Finance and Operations, перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="0ef53-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="0ef53-109">Если отображаются сведения о связанных средах и список выполняемых сопоставлений таблиц, двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="0ef53-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Проверка подключения приложения Finance and Operations при наличии прав администратора](media/verify_fin_ops_1.png)

+ <span data-ttu-id="0ef53-111">Если у вас нет прав администратора, вы получите сообщение об ошибке *Невозможно записать данные в объект \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="0ef53-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="0ef53-112">В примере на следующем рисунке невозможно создать строку клиента в приложении Finance and Operations, так как настроена двойная запись, но отсутствуют ссылочные данные группы клиентов и условий оплаты в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef53-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Проверка подключения приложения Finance and Operations при отсутствии прав администратора](media/verify_fin_ops_2.png)

<span data-ttu-id="0ef53-114">Сведения об устранении проблем при создании данных в приложениях Finance and Operations см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="0ef53-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="0ef53-115">Проверка настройки двойной записи в Dataverse</span><span class="sxs-lookup"><span data-stu-id="0ef53-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="0ef53-116">Если при создании данных вы видите столбец **Компания** на страницах в Dataverse, двойная запись настроена.</span><span class="sxs-lookup"><span data-stu-id="0ef53-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Проверка подключения Dataverse](media/verify_cds.png)

<span data-ttu-id="0ef53-118">Сведения об устранении проблем при создании данных в Dataverse см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="0ef53-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="0ef53-119">Сведения о том, как просмотреть подробные сведения об ошибке при возникновении каких-либо ошибок во время создания данных в Dataverse см. в разделе [Включение и просмотр журнала трассировки подключаемого модуля в Dataverse для просмотра подробных сведений об ошибке](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="0ef53-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]