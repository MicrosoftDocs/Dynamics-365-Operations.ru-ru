---
title: Создание возвратов в POS-терминале
description: В этой теме описывается, как инициировать возвраты для кассовых проводок или заказов клиентов в приложении Microsoft Dynamics 365 Commerce POS-терминала.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 496c4fe5230a599acf60fac39e51c43db372f92c
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129828"
---
# <a name="create-returns-in-pos"></a><span data-ttu-id="6e60e-103">Создание возвратов в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="6e60e-103">Create returns in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6e60e-104">В этой теме описывается, как инициировать возвраты для кассовых проводок или заказов клиентов в приложении Microsoft Dynamics 365 Commerce POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="6e60e-104">This topic describes how to initiate returns for cash-and-carry transactions or customer orders in the Microsoft Dynamics 365 Commerce point of sale (POS) app.</span></span>

> [!NOTE]
> <span data-ttu-id="6e60e-105">В выпуске Commerce версии 10.0.20 и позднее доступна новая функция, которая называется **Унифицированная обработка возвратов в POS-терминале**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="6e60e-106">Эта функция обеспечивает более согласованную и универсальную процедуру возврата в POS-терминале, независимо от типа проводки (кассовая проводка или заказ клиента) или исходного канала, в котором был создан заказ.</span><span class="sxs-lookup"><span data-stu-id="6e60e-106">This feature provides a more consistent and unified return process in POS, regardless of the transaction type (cash-and-carry transaction or customer order) or the original channel that the order was created in.</span></span> <span data-ttu-id="6e60e-107">Мы рекомендуем всем организациям включить эту новую функцию, чтобы улучшить общую надежность обработки возвратов через POS-терминал.</span><span class="sxs-lookup"><span data-stu-id="6e60e-107">We recommend that all organizations turn on this new feature to help improve the overall reliability of return processing through POS.</span></span>
>
> <span data-ttu-id="6e60e-108">После включения функции ее невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="6e60e-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="process-returns-by-using-the-return-transaction-operation"></a><span data-ttu-id="6e60e-109">Обработка возвратов с использованием операции проводки возврата</span><span class="sxs-lookup"><span data-stu-id="6e60e-109">Process returns by using the return transaction operation</span></span>

<span data-ttu-id="6e60e-110">Рекомендуется добавить операцию проводки возврата в [макет экрана](pos-screen-layouts.md) POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="6e60e-110">We recommend that you add the return transaction operation to your POS [screen layout](pos-screen-layouts.md).</span></span> <span data-ttu-id="6e60e-111">В выпусках до выпуска Commerce версии 10.0.20 операция проводки возврата правильно поддерживает обработку возвратов только для кассовых проводок.</span><span class="sxs-lookup"><span data-stu-id="6e60e-111">In releases before the Commerce version 10.0.20 release, the return transaction operation correctly supports the processing of returns for cash-and-carry transactions only.</span></span> <span data-ttu-id="6e60e-112">После включения функции **единой обработки возвратов для POS-терминала** в выпуске Commerce версии 10.0.20 или более поздней операция проводки возврата также поддерживает обработку возвратов, происходящих из заказов клиентов, таких как "самовывоз" или "доставка на дом", по которым уже были выставлены накладные.</span><span class="sxs-lookup"><span data-stu-id="6e60e-112">After you turn on the **Unified return processing experience for POS** feature in the Commerce version 10.0.20 release or later, the return transaction operation also supports the processing of returns that originate from customer orders, such as "pick up" or "ship to home" orders that are already invoiced.</span></span>

<span data-ttu-id="6e60e-113">Из операции проводки возврата пользователи могут выполнять поиск кассовых проводок или заказов клиентов, для которых осуществляется возврат, вводя любые из следующих четырех критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="6e60e-113">From the return transaction operation, users can search for a cash-and-carry transaction or a customer order to return against by entering any of the following four search criteria.</span></span> <span data-ttu-id="6e60e-114">Пользователи могут ввести эти критерии, используя клавиатуру устройства, экранную клавиатуру или сканер штрих-кодов.</span><span class="sxs-lookup"><span data-stu-id="6e60e-114">Users can enter these criteria by using a device keyboard, on-screen keypad, or bar code scanner.</span></span>

- <span data-ttu-id="6e60e-115">Код прихода</span><span class="sxs-lookup"><span data-stu-id="6e60e-115">Receipt ID</span></span>
- <span data-ttu-id="6e60e-116">Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="6e60e-116">Order number</span></span>
- <span data-ttu-id="6e60e-117">Код ссылки на канал (также называемый кодом подтверждения заказа)</span><span class="sxs-lookup"><span data-stu-id="6e60e-117">Channel reference ID (also known as the order confirmation ID)</span></span>
- <span data-ttu-id="6e60e-118">Код накладной</span><span class="sxs-lookup"><span data-stu-id="6e60e-118">Invoice ID</span></span>

<span data-ttu-id="6e60e-119">Если найдена проводка или заказ, удовлетворяющий критериям поиска, отображается страница **Возвращаемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-119">If a transaction or order is found that matches the search criteria, the **Returnable products** page appears.</span></span> <span data-ttu-id="6e60e-120">Там пользователи могут указать возвращаемые номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6e60e-120">There, users can specify the items that are being returned.</span></span> <span data-ttu-id="6e60e-121">Они также могут вводить возвращаемые количества и коды причины.</span><span class="sxs-lookup"><span data-stu-id="6e60e-121">They can also enter return quantities and reason codes.</span></span>

<span data-ttu-id="6e60e-122">Для каждой строки заказа в списке возвращаемых продуктов POS-терминал отображает информацию о первоначальном количестве покупки и количествах из всех ранее обработанных возвратов.</span><span class="sxs-lookup"><span data-stu-id="6e60e-122">For each order line in the list of returnable products, POS shows information about the original purchase quantity and the quantities from any returns that were previously processed.</span></span> <span data-ttu-id="6e60e-123">Возвращаемое количество, вводимое пользователем для строки заказа, должно быть меньше или равно значению поля **Доступно для возврата**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-123">The return quantity that a user enters for an order line must be less than or equal to the value of the **Available to return** field.</span></span>

![Страница возвращаемых продуктов](media/returnslist.png)

<span data-ttu-id="6e60e-125">Если во время обработки возвратов у пользователя имеется физический продукт и этот продукт имеет штрих-код, пользователь может отсканировать штрих-код для регистрации возврата.</span><span class="sxs-lookup"><span data-stu-id="6e60e-125">During return processing, if a user has the physical product, and that product has a bar code, the user can scan the bar code to register the return.</span></span> <span data-ttu-id="6e60e-126">Каждое сканирование штрих-кода увеличивает возвращаемое количество на одну номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="6e60e-126">Each scan of the bar code increases the return quantity by one item.</span></span> <span data-ttu-id="6e60e-127">Однако если метка штрих-кода имеет встроенное количество, это количество будет введено в поле **Возвращается сейчас**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-127">However, if the bar code label has an embedded quantity, that quantity will be entered in the **Returning now** field.</span></span>

<span data-ttu-id="6e60e-128">Пользователи могут также вручную выбрать возвращаемые номенклатуры на странице **Возвращаемые продукты**, а затем обновить поле **Возвращается сейчас**, используя область сведений справа.</span><span class="sxs-lookup"><span data-stu-id="6e60e-128">Users can also manually select items to return on the **Returnable products** page and then update the **Returning now** field by using the details pane on the right.</span></span>

<span data-ttu-id="6e60e-129">Если для проводки указывается максимальное доступное количество **Возвращается сейчас**, пользователь может выбрать операцию **Выбрать все** на панели приложения POS-терминала, чтобы задать максимальное возвращаемое количество для всех строк.</span><span class="sxs-lookup"><span data-stu-id="6e60e-129">If the maximum available **Returning now** quantity is being specified for a transaction, the user can select the **Select all** operation on the POS app bar to set the maximum returnable quantity on all lines.</span></span>

<span data-ttu-id="6e60e-130">Для каждой строки, в которой указано количество **Возвращается сейчас**, пользователь должен выбрать код причины возврата с помощью панели сведений.</span><span class="sxs-lookup"><span data-stu-id="6e60e-130">For each line that has a **Returning now** quantity, the user must select a return reason code by using the details panel.</span></span> <span data-ttu-id="6e60e-131">Для возврата по кассовым проводкам коды причин возврата настраиваются как информационные коды в профиле функциональности магазина.</span><span class="sxs-lookup"><span data-stu-id="6e60e-131">For returns of cash-and-carry transactions, the return reason codes are configured as info codes in the store's functionality profile.</span></span> <span data-ttu-id="6e60e-132">Для возвратов по заказам клиента коды причин возврата настраиваются на странице **Коды причин возврата** в Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6e60e-132">For returns of customer orders, the return reason codes are configured on the **Return reason codes** page in Dynamics 365 Commerce headquarters.</span></span>

<span data-ttu-id="6e60e-133">После настройки возвращаемого количества и кода причины для каждой номенклатуры, которая должна быть возвращена, пользователь может выбрать операцию **Возврат** на панели приложений POS, чтобы продолжить обработку.</span><span class="sxs-lookup"><span data-stu-id="6e60e-133">After the return quantity and reason code have been set for each item that must be returned, the user can select the **Return** operation on the POS app bar to proceed with the processing.</span></span> <span data-ttu-id="6e60e-134">Отображается страница проводок POS-терминала, в которой возвращаемые номенклатуры, выбранные на предыдущей странице, были добавлены в корзину.</span><span class="sxs-lookup"><span data-stu-id="6e60e-134">The POS transaction page appears, where the returnable items that were selected on the previous page have been added to the cart.</span></span> <span data-ttu-id="6e60e-135">Количества **Возвращается сейчас** для номенклатур отображаются как строки с отрицательным количеством по проводке, и рассчитывается общая сумма возврата.</span><span class="sxs-lookup"><span data-stu-id="6e60e-135">The **Returning now** quantities for the items appear as negative-quantity lines on the transaction, and the total refund is calculated.</span></span>

<span data-ttu-id="6e60e-136">Пользователи могут добавлять строки в проводку возврата, если они создают заказ на обмен.</span><span class="sxs-lookup"><span data-stu-id="6e60e-136">Users can add lines to a return transaction if they are creating an exchange order.</span></span> <span data-ttu-id="6e60e-137">Пользователи также могут добавить в проводку возврата дополнительные оперативные номенклатуры, используя операцию **Возврат продукта** для выбранной строки продаж с положительным количеством, которая была добавлена.</span><span class="sxs-lookup"><span data-stu-id="6e60e-137">Users can also add more ad-hoc return items to a return transaction by using the **Return product** operation for a selected positive-quantity sales line that has been added.</span></span>

> [!NOTE]
> <span data-ttu-id="6e60e-138">Операция **Возврат продукта** в POS-терминале не предоставляет каких-либо проверок относительно исходной проводки и позволяет вернуть любой продукт.</span><span class="sxs-lookup"><span data-stu-id="6e60e-138">The **Return product** operation in POS doesn't provide any validation against any original transaction and allows any product to be returned.</span></span> <span data-ttu-id="6e60e-139">Поэтому рекомендуется, чтобы только авторизованные пользователи имели разрешение на выполнение этой операции, или чтобы при использовании этой операции требовалось переопределение менеджера.</span><span class="sxs-lookup"><span data-stu-id="6e60e-139">Therefore, we recommend that only authorized users be allowed to perform this operation, or that a manager override be required if this operation is used.</span></span>

<span data-ttu-id="6e60e-140">Если при оформлении требуется возврат денежных средств, организации могут настроить [политики платежей по возвратам](refund_policy_returns.md), ограничивающие способы оплаты, которые могут использоваться для возврата денежных средств клиентам.</span><span class="sxs-lookup"><span data-stu-id="6e60e-140">If a refund is due at checkout, organizations can configure [refund payment policies](refund_policy_returns.md) that limit the payment methods that can be used to refund customers.</span></span> <span data-ttu-id="6e60e-141">Если исходные проводки была оплачена с использованием кредитной карты, в зависимости от процессора оплаты и конфигурации системы, у пользователей может быть возможность [выполнить возврат денежных средств на исходную карту](dev-itpro/linked-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="6e60e-141">If the original transaction was paid by using a credit card, depending on the payment processor and the system configuration, users might have the option to [issue a refund to the original card](dev-itpro/linked-refunds.md).</span></span> <span data-ttu-id="6e60e-142">В этом случае возврат денежных средств может быть обработан без необходимости повторного считывания кредитной карты клиента.</span><span class="sxs-lookup"><span data-stu-id="6e60e-142">In this case, the refund can be processed without requiring that the customer swipe their credit card again.</span></span> <span data-ttu-id="6e60e-143">Токен исходного платежа используется для выдачи возврата денежных средств.</span><span class="sxs-lookup"><span data-stu-id="6e60e-143">The original payment token is used to issue the refund.</span></span>

## <a name="other-return-options-in-pos"></a><span data-ttu-id="6e60e-144">Другие параметры возврата в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="6e60e-144">Other return options in POS</span></span>

<span data-ttu-id="6e60e-145">Когда функция **Унифицированная обработка возвратов в POS** включена, пользователи могут также использовать операцию **Показать журнал** в POS-терминале, чтобы начать возврат для кассовых проводок или заказов клиентов.</span><span class="sxs-lookup"><span data-stu-id="6e60e-145">When the **Unified return processing experience in POS** feature is turned on, users can also use the **Show journal** operation in POS to initiate a return for a cash-and-carry transaction or a customer order.</span></span> <span data-ttu-id="6e60e-146">Затем они могут выбрать проводку в журнале, а затем выбрать операцию **Возврат** на панели приложений POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="6e60e-146">They can then select a transaction in the journal and then select the **Return** operation on the POS app bar.</span></span> <span data-ttu-id="6e60e-147">Эта операция доступна только в том случае, если в заказе имеются строки с возвратом.</span><span class="sxs-lookup"><span data-stu-id="6e60e-147">This operation is available only if there are returnable lines on the order.</span></span> <span data-ttu-id="6e60e-148">Она вызывает то же взаимодействие пользователя, что и при операции **Возврат проводки**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-148">It initiates the same user experience as the **Return transaction** operation.</span></span>

<span data-ttu-id="6e60e-149">Пользователи также могут использовать операцию **Повторно вызвать заказ** в POS-терминале для поиска и повторного вызова заказов клиентов.</span><span class="sxs-lookup"><span data-stu-id="6e60e-149">Users can also use the **Recall order** operation in POS to search for and recall customer orders.</span></span> <span data-ttu-id="6e60e-150">(Эта операция не может использоваться для кассовых проводок.)</span><span class="sxs-lookup"><span data-stu-id="6e60e-150">(This operation can't be used for cash-and-carry transactions).</span></span> <span data-ttu-id="6e60e-151">В этом случае после выбора заказа клиента операция **Возврат** на панели приложений POS-терминала может быть использована для запуска возврата для заказа клиента.</span><span class="sxs-lookup"><span data-stu-id="6e60e-151">In this case, after a customer order is selected, the **Return** operation on the POS app bar can be used to initiate a return for the customer order.</span></span> <span data-ttu-id="6e60e-152">Эта операция доступна только в том случае, если в заказе имеются строки с возвратом.</span><span class="sxs-lookup"><span data-stu-id="6e60e-152">This operation is available only if there are returnable lines on the order.</span></span> <span data-ttu-id="6e60e-153">Она вызывает то же взаимодействие пользователя, что и при операции **Возврат проводки** или **Показать журнал**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-153">It initiates the same user experience as the **Return transaction** or **Show journal** operation.</span></span>

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a><span data-ttu-id="6e60e-154">Заказы на возврат разносятся в Commerce Headquarters как заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="6e60e-154">Return orders are posted to Commerce headquarters as sales orders</span></span> 

<span data-ttu-id="6e60e-155">Когда функция **Унифицированная обработка возвратов в POS** включена, все возвраты, созданные в POS, записываются в Commerce Headquarters как заказы на продажу, имеющие отрицательные строки.</span><span class="sxs-lookup"><span data-stu-id="6e60e-155">When the **Unified return processing experience in POS** feature is turned on, all returns that are created in POS are written to Commerce headquarters as sales orders that have negative lines.</span></span> <span data-ttu-id="6e60e-156">В выпусках до выпуска Commerce версии 10.0.20 пользователи могут выбрать, должны ли заказы на возврат разноситься как заказы на продажу, имеющие отрицательные строки, или же они должны быть заказами на возврат, созданными в процессе авторизации возврата товаров (RMA).</span><span class="sxs-lookup"><span data-stu-id="6e60e-156">In releases before the Commerce version 10.0.20 release, users can select whether return orders should be posted as sales orders that have negative lines, or whether they should be return orders that are created through the return merchandise authorization (RMA) process.</span></span> 

<span data-ttu-id="6e60e-157">В функции **Унифицированная обработка возвратов в POS** вариант использования процесса RMA для создания возвратов в POS-терминале была объявлена устаревшей.</span><span class="sxs-lookup"><span data-stu-id="6e60e-157">In the **Unified return processing experience in POS** feature, the option to use the RMA process to create returns in POS has been deprecated.</span></span> <span data-ttu-id="6e60e-158">После включения этой функции все возвраты будут создаваться как заказы на продажу, имеющие отрицательные строки.</span><span class="sxs-lookup"><span data-stu-id="6e60e-158">After this feature is turned on, all returns will be created as sales orders that have negative lines.</span></span>

## <a name="offline-return-processing-improvements"></a><span data-ttu-id="6e60e-159">Улучшения автономной обработки возвратов</span><span class="sxs-lookup"><span data-stu-id="6e60e-159">Offline return processing improvements</span></span>

<span data-ttu-id="6e60e-160">В большинстве случаев когда возврат обрабатывается в POS-терминале, система пытается выполнить вызов службы Real-time Service (RTS) в Commerce Headquarters для подтверждения текущих доступных для возврата количеств.</span><span class="sxs-lookup"><span data-stu-id="6e60e-160">In most cases, when a return is processed in POS, the system tries to make a real-time service (RTS) call to Commerce headquarters to validate the current quantities that are available for return.</span></span> <span data-ttu-id="6e60e-161">Эта проверка помогает защитить от мошеннических ситуаций, в которых клиент пытается вернуть одну и ту же номенклатуру в нескольких местах.</span><span class="sxs-lookup"><span data-stu-id="6e60e-161">This validation helps prevent fraudulent scenarios where a customer tries to return the same item in multiple locations.</span></span>

<span data-ttu-id="6e60e-162">Для обработки ситуаций, когда вызов службы RTS не может быть выполнен из-за проблем с сетью или подключением, процесс был установлен для периодической синхронизации данных о возвращенных количествах из Commerce Headquarters с базой данных канала магазина.</span><span class="sxs-lookup"><span data-stu-id="6e60e-162">To handle situations where the RTS call can't be made because of network or connectivity issues, a process has been put in place to periodically synchronize return quantity data from Commerce headquarters to a store's channel database.</span></span> <span data-ttu-id="6e60e-163">Такое отслеживание возвратов на стороне канала позволяет гарантировать, что количества **Доступно для возврата**, отображаемые в POS-терминале, достаточно точны даже в том случае, когда POS-терминал не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="6e60e-163">This channel-side return tracking helps ensure that the **Available to return** quantities that are shown in POS are reasonably accurate, even when POS is offline.</span></span> <span data-ttu-id="6e60e-164">Это также гарантирует, что POS-терминал может продолжать проверять информацию на стороне канала, чтобы предотвратить мошеннические возвраты.</span><span class="sxs-lookup"><span data-stu-id="6e60e-164">It also ensures that POS can continue to validate the channel-side information to help prevent fraudulent returns.</span></span>

<span data-ttu-id="6e60e-165">Чтобы использовать процесс возврата в автономном режиме соответствующим образом, организации должны спланировать пакетное задание **Обновить количества возврата** в Commerce Headquarters, чтобы оно выполнялось часто.</span><span class="sxs-lookup"><span data-stu-id="6e60e-165">To use the offline return process in the appropriate manner, organizations should schedule the **Update return quantities** batch job in Commerce headquarters so that it runs frequently.</span></span> <span data-ttu-id="6e60e-166">Рекомендуется, чтобы это задание выполнялось с той же частотой, что и P-задание, которое извлекает новые проводки из каналов Commerce в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6e60e-166">We recommend that this job run at the same frequency as the P job that pulls new transactions from Commerce channels into Commerce headquarters.</span></span>

<span data-ttu-id="6e60e-167">Задание **Обновить количества возврата** рассчитывает количество, доступное для возврата по всем заказам на продажу, имеющимся в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6e60e-167">The **Update return quantities** job calculates the quantity that is available for return for all sales orders that are found in Commerce headquarters.</span></span> <span data-ttu-id="6e60e-168">Данные, которые рассчитывает задание, должны быть отправлены в базы данных канала, чтобы можно было обновить каналы магазина.</span><span class="sxs-lookup"><span data-stu-id="6e60e-168">The data that the job calculates must then be sent to channel databases, so that the store channels can be updated.</span></span> <span data-ttu-id="6e60e-169">Для этой цели используется задание распределения **Количества по возврату** (1200).</span><span class="sxs-lookup"><span data-stu-id="6e60e-169">The **Return quantities** (1200) distribution job is used for this purpose.</span></span> <span data-ttu-id="6e60e-170">Поскольку данные о возвращаемом количестве синхронизируются с Commerce Headquarters, если возврат обрабатывается в POS-терминале, но не удается выполнить вызов службы RTS, POS-терминал может использовать данные о возвратах со стороны канала, чтобы проверит количества **Доступно для возврата** для данной строки продаж.</span><span class="sxs-lookup"><span data-stu-id="6e60e-170">Because data about the returnable quantity is synchronized from Commerce headquarters, if a return is processed in POS, but the RTS call can't be made, POS can use the channel-side return information to validate the **Available to return** quantities for a given sales line.</span></span>

<span data-ttu-id="6e60e-171">Если не удается выполнить вызовы службы RTS и POS-терминал использует данные на стороне канала для проверки возврата, предупреждающее сообщение информирует пользователей о том, что они создают "автономный" возврат.</span><span class="sxs-lookup"><span data-stu-id="6e60e-171">When RTS calls can't be made, and POS is using channel-side data for return validation, a warning message informs users that they are creating an "offline" return.</span></span> <span data-ttu-id="6e60e-172">Таким образом, они знают о том, что количество **Доступно для возврата**, отображаемое в POS-терминале, может быть устаревшим и неточным, в зависимости от того, когда задание **Обновить количества возврата** было в последний раз обработано и синхронизировано с каналом.</span><span class="sxs-lookup"><span data-stu-id="6e60e-172">Therefore, they are aware that the **Available to return** quantity that is shown in POS might be out of date and no longer accurate, depending on when the **Update return quantities** job was last processed and synchronized to the channel.</span></span>

<span data-ttu-id="6e60e-173">Например, клиент недавно выполнил возврат для строки заказа в другом канале, но данные еще не были синхронизированы с базами данных канала с помощью задания **Обновить количества возврата**.</span><span class="sxs-lookup"><span data-stu-id="6e60e-173">For example, a customer recently processed a return for an order line in another channel, but that data hasn't yet been synchronized to the channel databases through the **Update return quantities** job.</span></span> <span data-ttu-id="6e60e-174">Клиент затем переходит в другой магазин и пытается снова вернуть ту же номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="6e60e-174">The customer then goes to a different store and tries to return the same item again.</span></span> <span data-ttu-id="6e60e-175">В этом случае, если магазин не может сделать вызов службы RTS в Commerce Headquarters, чтобы получать данные о возвратах в реальном времени, POS-терминал позволит снова вернуть номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="6e60e-175">In this case, if the store can't make the RTS call to Commerce headquarters to get real-time return data, POS will allow the item to be returned again.</span></span> <span data-ttu-id="6e60e-176">Однако пользователь получает предупреждение о том, что сведения, используемые для проверки возврата, могут быть устаревшими.</span><span class="sxs-lookup"><span data-stu-id="6e60e-176">However, the user is warned that the information that is being used to validate the return might be out of date.</span></span> <span data-ttu-id="6e60e-177">Сообщение, которое получает пользователь, — это только предупредительное сообщение.</span><span class="sxs-lookup"><span data-stu-id="6e60e-177">The message that the user receives is only a warning message.</span></span> <span data-ttu-id="6e60e-178">Это не мешает пользователю продолжить обработку возврата.</span><span class="sxs-lookup"><span data-stu-id="6e60e-178">It doesn't prevent the user from continuing to process the return.</span></span>

<span data-ttu-id="6e60e-179">Если информация на стороне канала по какой-либо причине не является актуальной, и при этом выполняется автономный возврат для количества, которое превышает фактическое значение **Доступно для возврата**, может быть сформирована ошибка при выполнении разноски журнала операций, чтобы создать проводку в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6e60e-179">If the channel-side information isn't up to date for some reason, and an offline return is processed for a quantity that exceeds the actual **Available to return** quantity, an error might be generated when statement posting is run to create the transaction in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="6e60e-180">Когда функция **Унифицированная обработка возвратов в POS** включена, становятся доступными новые дополнительные функции, которые поддерживают проверку возвратов продуктов с серийными номерами.</span><span class="sxs-lookup"><span data-stu-id="6e60e-180">When the **Unified returns processing experience in POS** feature is turned on, new optional features that support the validation of serialized product returns become available.</span></span> <span data-ttu-id="6e60e-181">Дополнительные сведения см. в разделе [Возврат продуктов с контролируемыми серийными номерами в POS-терминале](POS-serial-returns.md).</span><span class="sxs-lookup"><span data-stu-id="6e60e-181">For more information, see [Return serial number–controlled products in Point of Sale (POS)](POS-serial-returns.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e60e-182">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6e60e-182">Additional resources</span></span>

[<span data-ttu-id="6e60e-183">Возврат продуктов с контролируемыми серийными номерами в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="6e60e-183">Return serial number–controlled products in Point of Sale (POS)</span></span>](POS-serial-returns.md)

[<span data-ttu-id="6e60e-184">Связанные возвраты ранее утвержденных и подтвержденных проводок</span><span class="sxs-lookup"><span data-stu-id="6e60e-184">Linked refunds of previously approved and confirmed transactions</span></span>](dev-itpro/linked-refunds.md)

[<span data-ttu-id="6e60e-185">Создание и обновление политик возврата и возмещения для канала</span><span class="sxs-lookup"><span data-stu-id="6e60e-185">Create and update a returns and refunds policy for a channel</span></span>](refund_policy_returns.md)

[<span data-ttu-id="6e60e-186">Визуальные конфигурации пользовательского интерфейса POS</span><span class="sxs-lookup"><span data-stu-id="6e60e-186">POS user interface visual configurations</span></span>](pos-screen-layouts.md)