---
title: Оповещение клиентов с помощью уведомлений по электронной почте
description: В этом разделе представлена информация о том, как настроить правила, которые отправляют по электронной почте уведомления о предопределенных событиях.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546970"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="a2b5e-103">Оповещение клиентов с помощью уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="a2b5e-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a2b5e-104">В Microsoft Dynamics 365 for Finance and Operations можно определить пользовательские правила оповещений, которые контролируют отфильтрованные представления данных и автоматически отправляют уведомления по электронной почте при возникновении предварительно определенных событий.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="a2b5e-105">Возможность отправлять уведомления по электронной почте доступна для всех поддерживаемых типов оповещений и может также быть включена для существующих правил создания оповещений.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="a2b5e-106">Встроенные элементы управления можно использовать для создания правил оповещения, которые отслеживают отфильтрованные представления системных пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="a2b5e-107">Отслеживая значение поля **Состояние**, можно также настроить правила оповещений, которые отправляют сообщение электронной почты в случае сбоя выполнения пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="a2b5e-108">После создания этих правил оповещения больше не нужно проверять отчеты на предмет изменения в бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="a2b5e-109">Вместо этого можно позволить интеллектуальной службе обнаружения изменений Finance and Operations выполнять наблюдение за вас.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="a2b5e-110">Оповещения клиентов зависят от подсистемы электронной почты, которая предоставляется за счет интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="a2b5e-111">Рекомендуется использовать поставщика протокола Simple Mail Transfer Protocol (SMTP), чтобы распределение сообщений электронной почты не зависело от локального почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="a2b5e-112">Для отправки уведомлений по электронной почте клиентам следует настроить интегрированные службы электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="a2b5e-113">Уведомления по электронной почте отправляются получателям от имени владельцев оповещений.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="a2b5e-114">Дополнительные сведения о настройке электронной почты в Finance and Operations см. в разделе [Настройка и отправка сообщений электронной почты](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="a2b5e-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="a2b5e-115">На следующем рисунке показано диалоговое окно **Создать правило генерации оповещений**, которое теперь включает параметр **Отправить сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="a2b5e-116">[![Диалоговое окно создания правила генерации оповещений, в котором для параметра "Отправить сообщение электронной почты" задано значение "Да"](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="a2b5e-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a2b5e-117">Если для параметра **Отправить сообщение электронной почты** установлено значение **Да**, уведомления с оповещениями будут продолжать доставляться из центра действий.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="a2b5e-118">Шаблоны сообщений электронной почты с оповещениями</span><span class="sxs-lookup"><span data-stu-id="a2b5e-118">Alert notification email templates</span></span>

<span data-ttu-id="a2b5e-119">Служба отправляет оповещения по электронной почте с использованием заранее определенных шаблонов электронной почты, которые содержат базовые сведения оповещения.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="a2b5e-120">На следующем рисунке показана структура оповещений, когда они получены по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="a2b5e-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="a2b5e-121">[![Основанные на шаблонах оповещения для создания записи, изменений полей и удаления шаблона](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="a2b5e-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
