---
title: Устранение неполадок при обновлении и миграции до расширенного управления складом
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907895"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="6bc88-103">Устранение неполадок при обновлении и миграции до расширенного управления складом</span><span class="sxs-lookup"><span data-stu-id="6bc88-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bc88-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.</span><span class="sxs-lookup"><span data-stu-id="6bc88-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="6bc88-105">Я получаю следующее сообщение об ошибке: "java.security.cert.certPathValidatorException: не найдена привязка доверия для пути сертификации."</span><span class="sxs-lookup"><span data-stu-id="6bc88-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6bc88-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6bc88-106">Issue description</span></span>

<span data-ttu-id="6bc88-107">Вы получаете это сообщение об ошибке в мобильном приложении управления складом, поскольку сертификаты с собственной подписью не являются доверенными для Android 8+ в локальных средах.</span><span class="sxs-lookup"><span data-stu-id="6bc88-107">You receive this error message in the Warehouse Management mobile app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6bc88-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6bc88-108">Issue resolution</span></span>

<span data-ttu-id="6bc88-109">Используйте внешний (общий) центр сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="6bc88-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="6bc88-110">Исправление для этой проблемы доступно в версии 1.9.0.0 приложения склада.</span><span class="sxs-lookup"><span data-stu-id="6bc88-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="6bc88-111">Дополнительные сведения об этой проблеме и ее устранении см. в разделе [Устранение неполадок при подключении к мобильному приложению управления складом](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6bc88-111">For more information about this issue and how to fix it, see [Troubleshoot Warehouse Management mobile app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="6bc88-112">Каков утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом?</span><span class="sxs-lookup"><span data-stu-id="6bc88-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="6bc88-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6bc88-113">Issue description</span></span>

<span data-ttu-id="6bc88-114">В настоящее время вы работаете под управлением складом/запасами и с использованием базовой функции запасов, и хотите перейти к расширенной работе со складом, чтобы воспользоваться преимуществами мобильных устройств, волн и работы.</span><span class="sxs-lookup"><span data-stu-id="6bc88-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="6bc88-115">Однако возникают проблемы при попытке выполнить этот переход.</span><span class="sxs-lookup"><span data-stu-id="6bc88-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="6bc88-116">Например, невозможно изменить продукты таким образом, чтобы они использовали аналитики хранения (сайт, склад и местоположение), так как у продуктов имеются проводки по ним.</span><span class="sxs-lookup"><span data-stu-id="6bc88-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="6bc88-117">Поэтому вы должны изучить утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом.</span><span class="sxs-lookup"><span data-stu-id="6bc88-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6bc88-118">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6bc88-118">Issue resolution</span></span>

<span data-ttu-id="6bc88-119">Для получения дополнительных сведений о процессе перехода от базовой работы со складом на расширенную работу со складом, см. следующие записи блога и документацию:</span><span class="sxs-lookup"><span data-stu-id="6bc88-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="6bc88-120">Включение процесса управления складом для существующих номенклатур и складов</span><span class="sxs-lookup"><span data-stu-id="6bc88-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="6bc88-121">Миграция Microsoft Dynamics AX WMS на новые функции склада и транспортировки R3</span><span class="sxs-lookup"><span data-stu-id="6bc88-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="6bc88-122">Миграция элементов WMSI/WMS2</span><span class="sxs-lookup"><span data-stu-id="6bc88-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="6bc88-123">Обновление управления складом с Microsoft Dynamics AX 2012 до Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6bc88-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]