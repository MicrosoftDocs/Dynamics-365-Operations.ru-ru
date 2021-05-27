---
title: Настройка принципа пополнения по спецификации для строк спецификации не учитывается
description: Настройка принципа пополнения по спецификации для строк спецификации не учитывается.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026849"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="755de-103">Настройка принципа пополнения по спецификации для строк спецификации не учитывается</span><span class="sxs-lookup"><span data-stu-id="755de-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="755de-104">Номер статьи базы знаний: 4612725</span><span class="sxs-lookup"><span data-stu-id="755de-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="755de-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="755de-105">Symptoms</span></span>

<span data-ttu-id="755de-106">Эта проблема возникает в том случае, когда поле **Автопотребление по спецификации** на вкладке **Автоматическое обновление** на странице **Параметры управления производством** имеет значение *Принцип пополнения по спецификации*.</span><span class="sxs-lookup"><span data-stu-id="755de-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="755de-107">Этот параметр указывает, что все строки спецификации должны автоматически потребляться при получении заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="755de-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="755de-108">Если значение поля **Принцип пополнения по спецификации** в строках спецификации явно задан *Вручную*, можно предположить, что строки спецификации не потребляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="755de-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="755de-109">Однако в этом случае строки спецификации, для которых в поле **Принцип пополнения по спецификации** используется значение *Вручную*, все равно потребляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="755de-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="755de-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="755de-110">Resolution</span></span>

<span data-ttu-id="755de-111">Если вы столкнулись с этой проблемой, параметры управления производством могут быть настроены для переопределения настройки **Принцип пополнения по спецификации** для строк спецификации.</span><span class="sxs-lookup"><span data-stu-id="755de-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="755de-112">На странице **Параметры управления производством** на вкладке **Автоматическое обновление** проверьте значение поля **Автопотребление по спецификации**.</span><span class="sxs-lookup"><span data-stu-id="755de-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="755de-113">Если значение параметра равно *Всегда*, система будет игнорировать настройку **Принцип пополнения по спецификации** для всех строк спецификации и всегда будет пополнять строки по спецификации.</span><span class="sxs-lookup"><span data-stu-id="755de-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="755de-114">Чтобы система соблюдала настройку **Принцип пополнения по спецификации** для строк спецификации, измените значение в поле **Автопотребление по спецификации** на *Принцип пополнения по спецификации*.</span><span class="sxs-lookup"><span data-stu-id="755de-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
