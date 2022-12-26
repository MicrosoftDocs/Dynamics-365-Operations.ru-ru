---
title: Обзор Dynamics 365 Payment Connector для Adyen
description: В этой статье представлен обзор соединителя Microsoft Dynamics 365 Payment Connector для Adyen.
author: rassadi
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.openlocfilehash: 58d88e023b73ce19331bd6f54644a62d8f6f35af
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812095"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Обзор Dynamics 365 Payment Connector для Adyen

[!include [banner](../includes/banner.md)]

В этой статье представлен обзор соединителя Microsoft Dynamics 365 Payment Connector для Adyen. и представлен полный список поддерживаемых функций и функциональных возможностей. В связанных статьях описывается регистрация для Adyen, конфигурация соединителя, часто задаваемые вопросы и руководство по устранению неполадок для некоторых типичных проблем.

## <a name="key-terms"></a>Ключевые термины

| Срок | Описание |
|---|---|
| Соединитель платежей | Расширение, облегчающее взаимодействие между Microsoft Dynamics 365 Commerce (и связанными компонентами) и службой платежей. Соединитель, описанный в этой статье, был реализован с помощью стандартного пакета средств разработки программного обеспечения (SDK) платежей. |
| Карта присутствует | Относится к проводкам платежа, в которых физическая карта представлена и используется в соединителе платежного терминала с POS-терминалом Dynamics 365. |
| Карта отсутствует | Относится к проводкам платежа, в которых физическая карта отсутствует, например, в сценариях электронной коммерции или центра обработки вызовов. В этих сценариях информация, связанная с платежом, вручную вводится на веб-сайте электронной коммерции, в потоке центра обработки вызовов или на POS-терминале или платежном терминале. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Поддерживаемые функции, функциональность, версии и терминалы

Стандартный платежный соединитель Dynamics 365 Payment Connector для Adyen использует стандартный SDK для платежей. Поэтому у него нет специальных возможностей, которые были бы недоступны для других соединителей платежей.

### <a name="supported-versions"></a>Поддерживаемые версии

#### <a name="microsoft-dynamics-365-supported-versions"></a>Поддерживаемые версии Microsoft Dynamics 365
Собственный готовый платежный соединитель Dynamics 365 Payment Connector для Adyen поддерживается в Microsoft Dynamics 365 Finance версии 8.1.3 (январь 2019) или более поздней версии, и в Microsoft Dynamics 365 Retail версии 8.1.3 или более поздней. Однако сторонние лица по-прежнему могут разрабатывать другие соединители платежей для Adyen для более ранних версий Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Поддерживаемые версии встроенного ПО Adyen

В приведенном ниже списке описываются минимальные и максимальные версии встроенного ПО Adyen, поддерживаемые для каждой версии Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS версии 10.0.25
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS версии 10.0.26
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS версии 10.0.27
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS версии 10.0.28
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS версии 10.0.29
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS версии 10.0.30
| Минимальная версия встроенного ПО Adyen | Максимальная версия встроенного ПО Adyen |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen может выпустить обновления дополнительных версий после того, как компания Microsoft испытала основную версию. Если основная версия поддерживается, то в одной и той же основной версии можно иметь дополнительные обновления версий. Эти обновления обычно являются исключительно целевыми исправлениями и не требуют полного повторного тестирования, если эта же основная версия встроенного ПО была ранее протестирована. Обновления не должны превышать максимальную версию встроенного ПО Adyen, указанную в документации. 
>
> Миграция с версии встроенного ПО Adyen более ранней версии, чем 53, на версию 53 требуется POS KB **4577957** для ежемесячных обновлений Commerce, версий с 10.0.11 до 10.0.14. Если одна из этих версий используется и не содержит исправления, после обновления платежного терминала будут разрешены платежи только через NFC. Применение исправления к POS устраняет эту проблему. Если версия POS-терминала старее версии 10.0.11, создайте запрос поддержки,в котором отметьте, что для неработающего MPOS необходимо исправление KB **4577957**.
> 
> Для версий встроенного ПО Adyen с 59p7 по 62p9 операция **обналичивания подарочного сертификата** запрашивает ввод ПИН-кода дважды в сценариях, в которых подарочный сертификат введен вручную. Эта проблема не воспроизводится при считывании подарочного сертификата. Adyen изучает. 

### <a name="supported-payment-terminals"></a>Поддерживаемые платежные терминалы
Соединитель платежей Dynamics 365 Payment Connector для Adyen использует преимущества независимого от устройств [API-интерфейса платежного терминала Adyen](https://www.adyen.com/blog/introducing-the-terminal-api). Он поддерживает все платежные терминалы, поддерживаемые данным интерфейсом прикладного программирования (API). Полный список поддерживаемых платежных терминалов см. на странице [POS-терминалы Adyen](https://www.adyen.com/pos-payments/terminals).

В следующем видеоролике описываются возможности платежного терминала Adyen Castles SE1 Android.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bKeM]

### <a name="supported-payment-instruments"></a>Поддерживаемые платежные средства

#### <a name="supported-debit-and-credit-cards"></a>Поддерживаемые дебетовые и кредитные карты

| Марка | Вариант | Карта присутствует | Электронная коммерция | Центр обработки вызовов |
|---|---|:-:|:-:|:-:|
| MasterCard | Кредит | ✔ | ✔ | ✔ |
| MasterCard | Дебет | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Кредит | ✔ | ✔ | ✔ |
| VISA | Дебет | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | Кредит | ✔ | ✔ | ✔ |
| AMEX | Дебет | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Коммерческая | ✔ | ✔ | ✔ |
| AMEX | AMEX Потребительская | ✔ | ✔ | ✔ |
| AMEX | AMEX Корпоративная | ✔ | ✔ | ✔ |
| AMEX | AMEX Малый бизнес | ✔ | ✔ | ✔ |
| Обнаружить | Стандартная | ✔ | ✔ | ✔ |
| Обнаружить | Android Pay | ✔ |  |  |
| Обнаружить | Apple Pay | ✔ |  |  |
| Обнаружить | Samsung Pay | ✔ |  |  |
| Diners   | Стандартная | ✔ | ✔ | ✔ |
| Dineromail | Стандартная | ✔ | ✔ | ✔ |
| JCB | Стандартная | ✔ | ✔ | ✔ |
| Union Pay\* | Стандартная | ✔ |  |  |
| Interac Debit\* | Стандартная | ✔ |  |  |

\*Повторяющиеся маркеры карт Interac и Union Pay не предоставляются Adyen, поэтому они не могут поддерживаться для карты, отсутствующей в проводке.

#### <a name="supported-gift-cards"></a>Поддерживаемые подарочные сертификаты
| Схема | Карта присутствует | Карта отсутствует |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Для поддержки этих внешних схем подарочных сертификатов с помощью платежного соединителя Dynamics 365 Payment Connector для Adyen необходимо выполнить дополнительные шаги. Дополнительные сведения см. в разделе [Поддержка внешних подарочных карт](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Поддерживаемые кошельки

| Схема | Карта присутствует | Карта отсутствует |
|---|---|---|
| Alipay | Поддержка будет добавлена в будущем выпуске. | Нет |
| WeChat | Поддержка будет добавлена в будущем выпуске. | Нет |

#### <a name="supported-card-present-input-methods"></a>Поддерживаемые методы ввода наличия карты
| Метод ввода | Поддерживается | Примечания |
|---|:-:|---|
| Вставка | ✔ | |
| Считывание | ✔ | |
| Прикосновение | ✔ | |
| Ручной ввод через пользовательский интерфейс POS-терминала |  | Не поддерживается в данный момент |
| Ввод вручную через платежный терминал. | ✔ | Поддерживает ручной ввод кредитовых, дебетовых и подарочных карт со вводом ПИН-кода. | 


#### <a name="supported-card-present-countries"></a>Поддерживаемые страны/регионы наличия карты

В следующих странах имеются доступные компоненты Commerce, а также поддержка наличия карт, представленная Adyen. Для текущей международной доступности Commerce посетите [страницу международной доступности](/dynamics365/get-started/availability).

| Страна или регион | Поддерживается |
| --- | :-: |
| Австралия | ✔ |
| Австрия | ✔ |
| Бельгия | ✔ |
| Канада | ✔ |
| Чешская республика | ✔ |
| Дания | ✔ |
| Эстония | ✔ |
| Финляндия | ✔ |
| Франция | ✔ |
| Германия | ✔ |
| Гонконг, САР | ✔ |
| Венгрия | ✔ |
| Исландия | ✔ |
| Ирландия | ✔ |
| Италия | ✔ |
| Япония | Будущий выпуск |
| Латвия | ✔ |
| Литва | ✔ |
| Малайзия | ✔ |
| Нидерланды | ✔ |
| Новая Зеландия | ✔ |
| Норвегия | ✔ |
| Польша | ✔ |
| Сингапур | ✔ |
| Швейцария | ✔ |
| Испания | ✔ |
| Швеция | ✔ |
| Швейцария | ✔ |
| Соединенное Королевство | ✔ |
| Соединенные Штаты | ✔ |
| Бразилия | Будущий выпуск |

#### <a name="supported-card-not-present-countries"></a>Поддерживаемые страны/регионы отсутствия карты

Следующие страны или регионы поддерживаются Adyen для карты, которая не представлена в проводках. [Обратитесь в Adyen](https://www.adyen.com/contact/sales) для получения подробной информации о поддержке по определенной стране или региону. Для текущей международной доступности Commerce посетите [страницу международной доступности](/dynamics365/get-started/availability).

| Страна или регион | 
| --- |
| Аргентина |
| Армения |
| Австралия |
| Австрия |
| Бахрейн |
| Бельгия |
| Бразилия |
| Болгария |
| Канада |
| Чили |
| Китай |
| Колумбия |
| Хорватия |
| Кипр |
| Чешская республика  |
| Дания |
| Египет |
| Эстония |
| Финляндия |
| Франция |
| Грузия |
| Германия |
| Гибралтар |
| Греция |
| Гернси |
| Гонконг, САР |
| Венгрия |
| Исландия |
| Индия |
| Индонезия |
| Ирландия |
| Остров Мэн |
| Израиль |
| Италия |
| Япония |
| Джерси |
| Республика Корея |
| Кувейт |
| Латвия |
| Литва |
| Люксембург |
| Малайзия |
| Мальта |
| Мексика |
| Марокко |
| Нидерланды |
| Новая Зеландия |
| Норвегия |
| Перу |
| Польша |
| Португалия |
| Катар |
| Румыния |
| Саудовская Аравия |
| Сербия |
| Сингапур |
| Словакия |
| Словения |
| ЮАР |
| Испания |
| Швеция |
| Швейцария |
| Тайвань |
| Танзания |
| Таиланд |
| Турция |
| Объединенные Арабские Эмираты (ОАЭ) |
| Соединенное Королевство |
| Соединенные Штаты Америки, включая Пуэрто-Рико  |

#### <a name="supported-dynamics-365-payment-features"></a>Поддерживаемые функции платежей Dynamics 365

В следующей таблице показан набор функций, которые поддерживает платежный соединитель Dynamics 365 Payment Connector для Adyen. Эти функции используют усовершенствования, которые появились в пакете SDK для платежей и некоторых компонентах в декабре 2018 года. Они не являются эксклюзивными для соединителя платежей Dynamics 365 Payment Connector для Adyen. Дополнительные сведения о том, как использовать эти усовершенствования для другого соединителя платежей, см. в разделе [Создание сквозной интеграции платежей для платежного терминала](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Схема | Карта присутствует | Карта отсутствует |
|---|:-:|:-:|
| [Сальдо подарочного сертификата для обналичивания](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Предотвращение дублирования платежей](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Многоканальная токенизация | ✔ | ✔ |
| Связанные возвраты денежных средств | ✔<br>(Начиная с 10.0.1) | ✔<br>(Начиная с 10.0.1) |
| [Сохранение онлайн-платежей](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Начиная с 10.0.2) | 
| [Внешние подарочные сертификаты для центра обработки вызовов и электронной коммерции](./gift-card.md) | ✔<br>(Начиная с 10.0.10) | 
| [Перенаправление платежей SCA](../adyen_redirect.md) | | ✔<br>(Начиная с 10.0.12) |
| [Выделенные платежные терминалы и запросы на принтер и кассовый лоток](../pos-multi-hws.md) | ✔<br>(Начиная с 10.0.12) | |
| [Поддержка чаевых на уровне SDK через соединитель Adyen](tipping.md) | ✔<br>(Начиная с 10.0.14) | |
| [Инкрементный сбор данных для выставления накладных по заказам](incremental-capture.md) |  | ✔<br>(Начиная с 10.0.18) |
| [Платежи с помощью бумажника](../wallets.md) |  | ✔<br>(Начиная с 10.0.20) |
| [Google Pay с Adyen](google-pay-adyen.md) |  | ✔<br>(Начиная с 10.0.27) |

## <a name="next-steps"></a>Далее

Информацию о регистрации на соединитель платежей Dynamics 365 Payment Connector для Adyen и его настройке см. в разделе [Настройка соединителя платежей Dynamics 365 Payment Connector для Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка Dynamics 365 Payment Connector для Adyen](adyen-connector-setup.md)

[Вопросы и ответы по Dynamics 365 Payment Connector для Adyen](adyen-connector-faq.md)

[Устранение неполадок с Dynamics 365 Payment Connector для Adyen](adyen-connector-troubleshoot.md)

[Вопросы и ответы по платежам](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]