---
title: Создание электронных документов и обновление данных приложений с помощью электронной отчетности (ER)
description: Можно разработать форматы электронной отчетности (ER), которые могут использоваться в приложении для создания исходящих электронных документов.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093881"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="3423c-103">Создание электронных документов и обновление данных приложения с помощью электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="3423c-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3423c-104">Можно разработать форматы электронной отчетности (ER), которые могут использоваться в приложении для создания исходящих электронных документов.</span><span class="sxs-lookup"><span data-stu-id="3423c-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="3423c-105">Можно также создать форматы ER, которые анализируют входящие электронные документы и используют содержимое в таких документах для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="3423c-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="3423c-106">С помощью этой функции можно использовать один формат ER для создания исходящих электронных документов, а затем обновить данные приложения.</span><span class="sxs-lookup"><span data-stu-id="3423c-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="3423c-107">Эта функция может использоваться в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="3423c-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="3423c-108">Чтобы предотвратить повторяющееся использование данных приложения в последующих процессах, можно пометить данные приложения сразу же после их использования для создания электронных документов.</span><span class="sxs-lookup"><span data-stu-id="3423c-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="3423c-109">Например, можно пометить проводки по оплате можно пометить как обработанные сразу же после их включения в созданное сообщение по платежу.</span><span class="sxs-lookup"><span data-stu-id="3423c-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="3423c-110">Чтобы сохранить подробные сведения об обработке электронных документов, которые были созданы с использованием логики ER.</span><span class="sxs-lookup"><span data-stu-id="3423c-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="3423c-111">Например, уникальный идентификатор сообщения об оплате, создаваемый с помощью выражения ER.</span><span class="sxs-lookup"><span data-stu-id="3423c-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="3423c-112">Выражение основывается на информации, введенной в диалоговом окне ER, когда формат ER используется для создания документов.</span><span class="sxs-lookup"><span data-stu-id="3423c-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="3423c-113">Для получения дополнительных сведений о данной функции, компоненте, см. ряд руководств "Создание документов электронной отчетности с обновлением данных" (часть бизнес-процесса 7.5.4.3 "Приобретение/разработка компонентов ИТ-услуг и решений" (10677)), в которых дано описание отчетности и архивирования Интрастат.</span><span class="sxs-lookup"><span data-stu-id="3423c-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="3423c-114">Для выполнения определенных действий в этих руководствах необходимы следующие файлы.</span><span class="sxs-lookup"><span data-stu-id="3423c-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="3423c-115">Загрузите и сохраните эти файлы на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="3423c-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="3423c-116">Конфигурация модели данных: Интрастат (модель)</span><span class="sxs-lookup"><span data-stu-id="3423c-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="3423c-117">Конфигурация сопоставления модели ER: Интрастат (сопоставление)</span><span class="sxs-lookup"><span data-stu-id="3423c-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="3423c-118">Конфигурация формата ER: Интрастат (формат)</span><span class="sxs-lookup"><span data-stu-id="3423c-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
