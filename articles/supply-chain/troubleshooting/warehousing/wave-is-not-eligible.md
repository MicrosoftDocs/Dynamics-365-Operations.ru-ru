---
title: Не разрешается очистка волны
description: Не разрешается очистка волны
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924335"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="b4233-103">Не разрешается очистка волны</span><span class="sxs-lookup"><span data-stu-id="b4233-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="b4233-104">Код ошибки: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="b4233-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="b4233-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="b4233-105">Symptoms</span></span>

<span data-ttu-id="b4233-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="b4233-106">The system shows the following error message:</span></span>

> <span data-ttu-id="b4233-107">Волна %1 не подлежит очистке</span><span class="sxs-lookup"><span data-stu-id="b4233-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="b4233-108">Невозможно очистить данные волны.</span><span class="sxs-lookup"><span data-stu-id="b4233-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="b4233-109">Причина</span><span class="sxs-lookup"><span data-stu-id="b4233-109">Cause</span></span>

<span data-ttu-id="b4233-110">В настоящее время запись волны обрабатывается по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="b4233-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="b4233-111">Для поля **Статус волны** задано значение *Выполнение*.</span><span class="sxs-lookup"><span data-stu-id="b4233-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="b4233-112">При выборе **Пакетное задание** в группе **Волна** на вкладке **Волна** в области действий в поле **Статус** не устанавливается значение *Завершено*, *Ошибка* или *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="b4233-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="b4233-113">Поэтому в данный момент выполняется пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="b4233-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4233-114">Приказ</span><span class="sxs-lookup"><span data-stu-id="b4233-114">Resolution</span></span>

<span data-ttu-id="b4233-115">В области действий на вкладке **Волна** в группе **Волна** выберите **Пакетное задание**, а затем выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="b4233-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="b4233-116">Если в поле **Статус** указано значение *Выполняется*: в области действий на вкладке **Пакетное задание** в группе **Пакетное задание** выберите **Просмотр задач**.</span><span class="sxs-lookup"><span data-stu-id="b4233-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="b4233-117">Можно отслеживать ход выполнения, обновляя страницу **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="b4233-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="b4233-118">Если в поле **Статус** не указано значение *Выполняется*: в области действий на вкладке **Пакетное задание** в группе **Функции** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="b4233-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="b4233-119">В поле **Выбрать новый статус** выберите *Ожидание*.</span><span class="sxs-lookup"><span data-stu-id="b4233-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="b4233-120">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4233-120">Then select **OK**.</span></span>
