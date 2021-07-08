---
title: Вопросы и ответы по сбросу киоска данных
description: В этой теме представлены ответы на некоторое часто задаваемые вопросы о сбросе киоска данных.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266617"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="e0d49-103">Вопросы и ответы по сбросу киоска данных</span><span class="sxs-lookup"><span data-stu-id="e0d49-103">Data mart resets FAQ</span></span>

<span data-ttu-id="e0d49-104">В этой теме представлены ответы на некоторое часто задаваемые вопросы о сбросе киоска данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="e0d49-105">Сброс киоска данных может занять много времени и, в зависимости от обстоятельств, может быть необязательным.</span><span class="sxs-lookup"><span data-stu-id="e0d49-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="e0d49-106">Таким образом, в этой теме содержатся сведения об обстоятельствах, когда в киоск данных может быть сброшен, а также в ситуации, когда это вряд ли поможет.</span><span class="sxs-lookup"><span data-stu-id="e0d49-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="e0d49-107">Что такое сброс киоска данных?</span><span class="sxs-lookup"><span data-stu-id="e0d49-107">What is a data mart reset?</span></span>

<span data-ttu-id="e0d49-108">Сброс киоска данных отключит задачи интеграции, удалит все данные киоска данных, а затем снова включит интеграцию.</span><span class="sxs-lookup"><span data-stu-id="e0d49-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="e0d49-109">Чтобы убедиться в том, что старые данные не вставлены, можно запустить этот сброс киоска данных только после завершения существующих задач.</span><span class="sxs-lookup"><span data-stu-id="e0d49-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="e0d49-110">При попытке сбросить киоск данных до завершения всех задач может быть получено сообщение, например, "Не удалось обработать сброс киоска данных из-за активной задачи.</span><span class="sxs-lookup"><span data-stu-id="e0d49-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="e0d49-111">Повторите попытку позже".</span><span class="sxs-lookup"><span data-stu-id="e0d49-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="e0d49-112">Когда необходимо выполнить сброс киоска данных?</span><span class="sxs-lookup"><span data-stu-id="e0d49-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="e0d49-113">Если одно или несколько из приведенных ниже утверждений применимы к вашей ситуации, организация может получить преимущества от сброса киоска данных:</span><span class="sxs-lookup"><span data-stu-id="e0d49-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="e0d49-114">База данных приложения была восстановлена.</span><span class="sxs-lookup"><span data-stu-id="e0d49-114">The application database was restored.</span></span>
- <span data-ttu-id="e0d49-115">Вы открыли запрос в службу поддержки, а специалист службы технической поддержки дал вам инструкцию выполнить сброс киоска данных в рамках шага устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="e0d49-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="e0d49-116">Когда сброс киоска данных не нужен?</span><span class="sxs-lookup"><span data-stu-id="e0d49-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="e0d49-117">Вот некоторые случаи, когда не рекомендуется выполнять сброс киоска данных:</span><span class="sxs-lookup"><span data-stu-id="e0d49-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="e0d49-118">У вас возникли проблемы с производительностью, связанные с синхронизацией данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="e0d49-119">У вас есть повторяющийся шаблон сброса по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="e0d49-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="e0d49-120">**Отсутствующие данные** — если вы заметили, что данные отсутствуют, откройте запрос в службу поддержки Майкрософт для просмотра формата отчета и возможных ошибок синхронизации данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="e0d49-121">**Состояние зависшей интеграции**</span><span class="sxs-lookup"><span data-stu-id="e0d49-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="e0d49-122">**Устаревшие записи** — устаревшие записи сами по себе не обязательно оправдывают сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="e0d49-123">Если имеется большой набор данных, выполнение процесса сброса займет некоторое время, но маловероятно, что это приведет к улучшению.</span><span class="sxs-lookup"><span data-stu-id="e0d49-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="e0d49-124">Если я сбрасываю киоск данных, я потеряю уже разработанные мной отчеты?</span><span class="sxs-lookup"><span data-stu-id="e0d49-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="e0d49-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="e0d49-125">No.</span></span> <span data-ttu-id="e0d49-126">Ваши отчеты хранятся в таблицах SQL, на которые не повлияют сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="e0d49-127">Если вы не уверены в том, что все созданные отчеты были удалены, можно создать резервные копии проектов, которые важно не потерять.</span><span class="sxs-lookup"><span data-stu-id="e0d49-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="e0d49-128">Чтобы создать резервные копии дизайнов, откройте конструктор отчетов и перейдите **Компания \> Компании \> Шаблоны \> Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="e0d49-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="e0d49-129">Все пользователи должны выйти из системы, прежде чем можно будет сбросить киоск данных?</span><span class="sxs-lookup"><span data-stu-id="e0d49-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="e0d49-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="e0d49-130">No.</span></span> <span data-ttu-id="e0d49-131">Пользователи могут продолжать работать в системе во время сброса киоска данных.</span><span class="sxs-lookup"><span data-stu-id="e0d49-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="e0d49-132">Однако до завершения сброса они не смогут получить доступ к отчетам, созданным с помощью Financial Reporter.</span><span class="sxs-lookup"><span data-stu-id="e0d49-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
