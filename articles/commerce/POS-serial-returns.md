---
title: Возврат продуктов с контролируемыми серийными номерами в POS-терминале
description: В этой теме описываются возможности для проверки номенклатур с серийными номерами как части процесса возврата в приложении POS-терминала Microsoft Dynamics 365 Commerce.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129827"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="b49c9-103">Возврат продуктов с контролируемыми серийными номерами в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="b49c9-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b49c9-104">В этой теме описываются возможности для проверки номенклатур с серийными номерами как части процесса возврата в приложении POS-терминала Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b49c9-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="b49c9-105">В выпуске Commerce версии 10.0.20 и позднее доступна новая функция, которая называется **Унифицированная обработка возвратов в POS-терминале**.</span><span class="sxs-lookup"><span data-stu-id="b49c9-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="b49c9-106">Чтобы использовать проверку серийного номера во время обработки заказов на возврат в POS-терминале, необходимо включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b49c9-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="b49c9-107">Сведения о других возможностях, предоставляемых этой функцией, когда она включена, см. в разделе [Создание возвратов в POS-терминале](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="b49c9-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="b49c9-108">После включения функции ее невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="b49c9-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="b49c9-109">Параметры для проверки возвратов с серийными номерами</span><span class="sxs-lookup"><span data-stu-id="b49c9-109">Options for validating serialized returns</span></span>

<span data-ttu-id="b49c9-110">Когда функция **Унифицированная обработка возвратов в POS-терминале**, организации могут выполнять проверку возвратов номенклатур с контролируемыми серийными номерами через POS-терминал.</span><span class="sxs-lookup"><span data-stu-id="b49c9-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="b49c9-111">Эта возможность может предупредить пользователей, если серийный номер, который возвращается, отличается от серийного номера проданной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b49c9-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="b49c9-112">В выпуске Commerce версии 10.0.20 и более поздних полученное пользователями сообщение будет только предупредительным сообщением.</span><span class="sxs-lookup"><span data-stu-id="b49c9-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="b49c9-113">Пользователи могут продолжать обрабатывать возврат на основе серийного номера, отличающегося от первоначально проданного серийного номера.</span><span class="sxs-lookup"><span data-stu-id="b49c9-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="b49c9-114">Чтобы настроить проверку серийных номеров для организации после включения функции **Унифицированная обработка возвратов в POS-терминале**, перейдите к пункту **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce** в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b49c9-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="b49c9-115">На вкладке **Запасы** на экспресс-вкладке **Складские операции магазина** выберите для параметра **Включить проверку серийных номеров при возвратах через POS-терминал** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b49c9-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="b49c9-116">Обработка возвратов для номенклатур с серийными номерами в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="b49c9-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="b49c9-117">Если для параметра **Включить проверку серийных номеров при возвратах через POS-терминал** задано значение **Да**, то при возврате номенклатуры с контролем серийных номеров через POS-терминал пользователь может ввести серийный номер для строки возврата в области сведений на странице **Возвращаемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="b49c9-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="b49c9-118">Если введенный серийный номер не совпадает с исходным серийным номером, который продавался для проводки по продажам, пользователь получает предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="b49c9-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="b49c9-119">Однако приложение не препятствует разноске возврата пользователем.</span><span class="sxs-lookup"><span data-stu-id="b49c9-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="b49c9-120">В настоящее время POS-терминал поддерживает проверку серийных номеров только для строк возврата, в которых исходное заказанное количество не больше единицы.</span><span class="sxs-lookup"><span data-stu-id="b49c9-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="b49c9-121">Если исходная строка заказа на продажу была создана в канале, отличном от POS, и если количество, заказанное для номенклатуры с серийными номерами в данной строке продажи больше единицы, номенклатуру нельзя корректно вернуть через POS-терминал.</span><span class="sxs-lookup"><span data-stu-id="b49c9-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b49c9-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b49c9-122">Additional resources</span></span>

[<span data-ttu-id="b49c9-123">Создание возвратов в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="b49c9-123">Create returns in POS</span></span>](POS-returns.md)
