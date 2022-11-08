---
title: Справочные коды ошибок модуля оформления заказа
description: В этой статье описываются справочные коды ошибок модуля оформления заказа, которые отображаются в отправляемых пользователям сообщениях об ошибках в Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728254"
---
# <a name="checkout-module-error-reference-codes"></a>Справочные коды ошибок модуля оформления заказа

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

В этой статье описываются коды ошибок модуля оформления заказа, которые отображаются в отправляемых пользователям сообщениях об ошибках в Microsoft Dynamics 365 Commerce.

В Dynamics 365 Commerce появились стандартные ссылки на ошибки, которые могут быть включены в ошибки оформления заказа интернет-канала, которые предоставляются клиентам в сети. В Commerce версии 10.0.31 и более поздних сообщения об ошибках в модуле оформления заказа включают коды ошибок и не отображают ненужные сведения для клиента в Интернете. Коды ошибок относятся к ошибкам, которые подробно описаны в этой статье.

В зависимости от возникшей ошибки, таблица в этой статье содержит следующие сведения:

- Описание условия, вызвавшего ошибку, или дополнительные сведения
- Сведения для рассмотрения в конфигурациях среды или соединителей платежей
- Сведения, на которые можно ссылаться в обращении поддержки, если требуется дополнительная помощь

## <a name="prerequisites"></a>Необходимые условия

Чтобы включить справочные коды ошибок модуля оформления заказа, перечисленные ниже, в конструкторе сайтов для вашего сайта перейдите к пункту **Параметры сайта \> Расширения**, и в разделе **Корзина и оформления заказа** выберите команду **Включить улучшенную передачу сообщений отображения ошибок интернет-канала**. 

## <a name="checkout-module-error-reference-codes"></a>Справочные коды ошибок модуля оформления заказа

Используйте следующую таблицу для получения дополнительных сведений о ссылках на код ошибки, предоставляемых клиентами или возникающим в интернет-магазине. Прокрутите вправо, чтобы просмотреть столбец **Описание ошибки**.

| Код ошибки | Код ошибки, связанной с Dynamics | Описание ошибки |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Не удалось авторизовать платеж. В **TokenizedPaymentCard** отсутствует код типа карты или указанный код типа карты не поддерживается. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Отклонено. Не удалось авторизовать платеж. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Не удалось авторизовать платеж. Требуются дополнительные сведения от клиента. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | К сожалению, что-то пошло не так. Не удалось получить результат принятия платежа по карте. Повторите попытку или обратитесь к системному администратору. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Не удается произвести платеж, поскольку отсутствуют свойства платежа торговца. Обратитесь к системному администратору. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Не удается получить службу платежных средств для операции. Проверьте настройку способа оплаты для выбранного типа платежного средства. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Платеж со счета клиента уже применен, разрешен только один платеж на проводку. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Лимит по счету клиента отличается от суммы к уплате. Попробуйте другой способ оплаты или обратитесь за помощью в службу поддержки клиентов. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Платеж со счета клиента превышает общую сумму к уплате за перечисленные номенклатуры. Повторите попытку или обратитесь за помощью в службу поддержки клиентов. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Для платежа по счету клиента требуется его собственный счет или соответствующий счет накладной в строке платежного средства. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | В данный момент не удается обработать платеж со счета клиента. Превышено значение нижнего предела. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Этому клиенту не разрешено платить в кредит. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | К сожалению, что-то пошло не так. Не удалось отменить платеж. Повторите попытку. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | При обработке платежа произошла ошибка. Повторите попытку позже. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Сумма платежа лояльности превышает допустимую для карты лояльности, используемой в данной проводке. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Сумма возврата денежных средств лояльности превышает допустимую для карты лояльности, используемой в данной проводке. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Не найден номер карты лояльности. Активируйте карту лояльности с этим номером или введите номер другой карты лояльности, а затем повторите попытку. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Номер карты лояльности недоступен. Введите другой номер карты лояльности и повторите попытку. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Данная карта лояльности не действительна для погашения баллов лояльности для этой транзакции. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Произошла ошибка, связанная с номером подарочного сертификата. Попробуйте другой номер подарочного сертификата или обратитесь за помощью в службу поддержки клиентов. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Сумма к оплате превышает баланс в подарочном сертификате. Введите другую сумму и повторите попытку. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Проводка не может содержать больше одной строки с оплатой баллами по программе лояльности. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | В информации о платеже отсутствуют данные, или они неверны. Проверьте информацию о платеже и повторите попытку. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | В настоящее время обработать заказ невозможно. Повторите попытку позже. |
| CCR025     | Время ожидания внешнего интерфейса для API-интерфейса оформления заказа | Истекло время ожидания операции внешнего интерфейса. Убедитесь, что заказ был обработан в Dynamics 365 Commerce Headquarters. |
| CCR026     | Изменена исходная авторизованная сумма | Сумма заказа изменилась по сравнению с исходной суммы авторизации, обработанной платежным шлюзом. Это может быть обусловлено истечением срока действия купона, рекламной акции или продажи. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | При обработке платежа произошла ошибка. Ссылка, указанная для API корзины, имеет другую ссылку, чем ожидалось (отметка потенциальной несогласованности в процессе оформления заказа). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Выбранный способ оплаты вызвал ошибку. Обратитесь в службу поддержки, чтобы проверить параметры учетной записи, или повторите попытку, указав другой способ оплаты. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Вопросы и ответы по платежам](dev-itpro/payments-retail.md)

[Модуль оформления заказа](add-checkout-module.md)

[Модуль платежа](payment-module.md)
