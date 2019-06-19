---
title: Настройка сценариев оплаты накладных
description: В этом разделе описывается настройка Dynamics 365 for Retail для поддержки различных сценариев, относящихся к оплате накладных.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564978"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="245e2-103">Настройка сценариев оплаты накладных</span><span class="sxs-lookup"><span data-stu-id="245e2-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="245e2-104">В функции оплаты накладных в Dynamics 365 for Retail были добавлены следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="245e2-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="245e2-105">Оплата нескольких накладных по заказам на продажу в одной транзакции в POS.</span><span class="sxs-lookup"><span data-stu-id="245e2-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="245e2-106">Оплата накладных клиентов различного типа, включая накладные с произвольным текстом, накладные по проектам и кредит-ноты.</span><span class="sxs-lookup"><span data-stu-id="245e2-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="245e2-107">Для реализации этих сценариев необходимо настроить профиль функциональности, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="245e2-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="245e2-108">Выберите **Розничная торговля \> Настройка канала \> Настройка POS \> Профили POS \> Профили функциональности** и выберите профиль, связанный с магазинами, для которых требуется внести изменения.</span><span class="sxs-lookup"><span data-stu-id="245e2-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="245e2-109">На вкладке **Функции** настройте следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="245e2-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="245e2-110">**Накладная по заказу на продажу** — выберите **Да**, чтобы разрешить пользователям оплачивать несколько накладных по заказам на продажу в одной проводке POS.</span><span class="sxs-lookup"><span data-stu-id="245e2-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="245e2-111">**Накладная с произвольным текстом** — выберите **Да**, чтобы разрешить пользователям оплачивать несколько накладных с произвольным текстом в одной проводке POS.</span><span class="sxs-lookup"><span data-stu-id="245e2-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="245e2-112">**Накладная по проекту** — выберите **Да**, чтобы разрешить пользователям оплачивать несколько накладных по проектам в одной проводке POS.</span><span class="sxs-lookup"><span data-stu-id="245e2-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="245e2-113">**Кредит-нота по заказу на продажу** — выберите **Да**, чтобы разрешить пользователям сопоставлять несколько кредит-нот по заказам на продажу с открытыми накладными или обрабатывать возврат денежных средств клиенту по открытой кредит-ноте.</span><span class="sxs-lookup"><span data-stu-id="245e2-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="245e2-114">Оплата и сопоставление частичных сумм пока не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="245e2-114">Payment or settlement of partial amounts is not yet supported.</span></span>
