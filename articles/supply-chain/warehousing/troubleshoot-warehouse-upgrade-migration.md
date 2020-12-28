---
title: Устранение неполадок при обновлении и миграции до расширенного управления складом
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645825"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="b398a-103">Устранение неполадок при обновлении и миграции до расширенного управления складом</span><span class="sxs-lookup"><span data-stu-id="b398a-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b398a-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.</span><span class="sxs-lookup"><span data-stu-id="b398a-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="b398a-105">Я получаю следующее сообщение об ошибке: "java.security.cert.certPathValidatorException: не найдена привязка доверия для пути сертификации."</span><span class="sxs-lookup"><span data-stu-id="b398a-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b398a-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="b398a-106">Issue description</span></span>

<span data-ttu-id="b398a-107">Вы получаете это сообщение об ошибке в приложении склада, поскольку сертификаты с собственной подписью не являются доверенными для Android 8+ в локальных средах.</span><span class="sxs-lookup"><span data-stu-id="b398a-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b398a-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="b398a-108">Issue resolution</span></span>

<span data-ttu-id="b398a-109">Используйте внешний (общий) центр сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="b398a-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="b398a-110">Исправление для этой проблемы доступно в версии 1.9.0.0 приложения склада.</span><span class="sxs-lookup"><span data-stu-id="b398a-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="b398a-111">Дополнительные сведения об этой проблеме и ее устранении см. в разделе [Устранение неполадок при подключении к приложению склада](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b398a-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="b398a-112">Каков утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом?</span><span class="sxs-lookup"><span data-stu-id="b398a-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="b398a-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="b398a-113">Issue description</span></span>

<span data-ttu-id="b398a-114">В настоящее время вы работаете под управлением складом/запасами и с использованием базовой функции запасов, и хотите перейти к расширенной работе со складом, чтобы воспользоваться преимуществами мобильных устройств, волн и работы.</span><span class="sxs-lookup"><span data-stu-id="b398a-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="b398a-115">Однако возникают проблемы при попытке выполнить этот переход.</span><span class="sxs-lookup"><span data-stu-id="b398a-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="b398a-116">Например, невозможно изменить продукты таким образом, чтобы они использовали аналитики хранения (сайт, склад и местоположение), так как у продуктов имеются проводки по ним.</span><span class="sxs-lookup"><span data-stu-id="b398a-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="b398a-117">Поэтому вы должны изучить утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом.</span><span class="sxs-lookup"><span data-stu-id="b398a-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b398a-118">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="b398a-118">Issue resolution</span></span>

<span data-ttu-id="b398a-119">Для получения дополнительных сведений о процессе перехода от базовой работы со складом на расширенную работу со складом, см. следующие записи блога и документацию:</span><span class="sxs-lookup"><span data-stu-id="b398a-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="b398a-120">Включение процесса управления складом для существующих номенклатур и складов</span><span class="sxs-lookup"><span data-stu-id="b398a-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="b398a-121">Миграция Microsoft Dynamics AX WMS на новые функции склада и транспортировки R3</span><span class="sxs-lookup"><span data-stu-id="b398a-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="b398a-122">Миграция элементов WMSI/WMS2</span><span class="sxs-lookup"><span data-stu-id="b398a-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="b398a-123">Обновление управления складом с Microsoft Dynamics AX 2012 до Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b398a-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
