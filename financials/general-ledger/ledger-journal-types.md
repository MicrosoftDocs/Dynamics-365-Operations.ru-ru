---
title: "Типы журнала главной книги"
description: "В этой статье описываются типы журналов, которые можно настроить для финансовых журналов. Используйте страницу имен журналов для настройки журналов, применяемых в Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: ad60a9daac6b4156126fc978c33b3fe1e86ef5ea
ms.lasthandoff: 03/31/2017


---

# <a name="ledger-journal-types"></a>Типы журнала главной книги

[!include[banner](../includes/banner.md)]


В этой статье описываются типы журналов, которые можно настроить для финансовых журналов. Используйте страницу имен журналов для настройки журналов, применяемых в Microsoft Dynamics 365 for Operations.

| Тип журнала                      | Цель                                                                                                                                                                                                                                                                                                                                                     | Введите сделки на этой странице                                |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Распределение                        | Создание проводок распределения в журнале распределения. Прежде чем создать журнал распределения, вы должны создать правило распределения на странице **Правило распределения ГК**.                                                                                                                                                                           | Обработать запрос на распределение                                     |
| Утверждение                          | Разноска утвержденных накладных поставщика по соответствующим счетам ГК.                                                                                                                                                                                                                                                                            | Журнал утверждения накладных                                       |
| Реверсирование банковского чека               | Сторнирование разнесенного чека. Чтобы использовать этот тип журнала, выберите параметр **Использовать процесс просмотра для отмены платежей** на странице **Параметры управления банком и кассовыми операциями**.                                                                                                                                                                                       | Проверить реверсирования, Отмена платежа                              |
| Отмена бланка банковского депозита    | Отмена бланка депозита. Чтобы использовать этот тип журнала, выберите параметр **Использовать процесс просмотра для отмены платежей по бланкам депозита** на странице **Параметры управления банком и кассовыми операциями**.                                                                                                                                                                       | Отмены платежей по бланкам депозита                             |
| Бюджет                            | Обработка ассигнований бюджета. Для использования этого типа журнала выберите параметр **Включить ассигнование бюджета** на странице **Параметры главной книги**. Записи в журнале бюджета будут содержать сведения на основе счетов ГК, определенных на странице **Определения разносок**.                                                        |                                                                |
| Акцепт переводного векселя клиентом  | Создание проводок принятия клиентом для переводных векселей.                                                                                                                                                                                                                                                                                              | Журнал выписки переводных векселей, Журнал перевыписки переводных векселей |
| Банковский перевод клиента          | Создание файла предъявления к оплате, который можно отправить в банк. Чтобы использовать этот тип журнала, очистите параметр **Автоматическое сопоставление** на странице **Параметры модуля расчетов** **с клиентами**.                                                                                                                                             | Предъявление к оплате                                                     |
| Выписка переводного векселя на клиента    | Создание проводки выписки переводных векселей на клиентов. Для использования этого типа журнала, очистите параметр **Создать и разнести журнал выписки автоматически при разноске накладных** на странице **Способы оплаты - клиенты**.                                                                                                                                         | Журнал выписки переводных векселей                                  |
| Клиентский платеж                  | Создание проводок клиентских платежей.                                                                                                                                                                                                                                                                                                                       | Журнал платежей                                                |
| Опротестованный переводной вексель клиента | Создание проводок протеста переводных векселей на клиентов.                                                                                                                                                                                                                                                                                                      | Журнал протеста переводных векселей                               |
| Перевыписка переводного векселя на клиента  | Создание проводок перевыписки переводных векселей на клиентов.                                                                                                                                                                                                                                                                                                       | Журнал перевыписки переводных векселей                                |
| Сопоставление переводного векселя по клиенту  | Создание проводок утверждения переводных векселей на клиентов.                                                                                                                                                                                                                                                                                                       | Журнал сопоставления переводных векселей                                |
| Ежедневно                             | Создание ежедневных проводок в общем журнале.                                                                                                                                                                                                                                                                                                             | Общий журнал                                                |
| Элиминирование                       | Создание проводок исключений в журнале исключений. Для использования этого типа журнала выберите параметры **Использовать для процесса финансового закрытия** и **Использовать для процесса финансовой консолидации** на странице **Юридические лица**. Перед использованием этого типа журнала, необходимо создать правило исключения ГК на странице **Правило исключения из ГК**. | Элиминирование                                                    |
| Бюджет ОС                | Создание записей регистрации бюджета основных средств.                                                                                                                                                                                                                                                                                                                 | Бюджет ОС                                             |
| Регистрация накладных                  | Регистрация основных сведений о накладных поставщика.                                                                                                                                                                                                                                                                                                           | Регистрация накладных                                               |
| Выплата зарплаты              | Выдача платежей на основе выписок по зарплате. Нельзя вручную вводить проводки в этот журнал. Необходимо создать выписки по оплате, а затем отправить их для платежа.                                                                                                                                                              |                                                                |
| Периодический                          | Создание периодических проводок для периодического журнала.                                                                                                                                                                                                                                                                                                      | Периодические журналы                                              |
| Разнести основные средства                 | Разноска проводок основных средств.                                                                                                                                                                                                                                                                                                                              | Основные средства                                                   |
| Проект - Расходы                | Создание проводок расходов по проекту.                                                                                                                                                                                                                                                                                                                        | Расход                                                        |
| Статистические проводки            | Создание статистических проводок.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Банковский перевод поставщика            | Создание файла предъявления к оплате переводного векселя, который можно отправить в банк.                                                                                                                                                                                                                                                                      | Журнал предъявлений к оплате                                             |
| Выплата поставщику               | Создание проводок выплат поставщикам.                                                                                                                                                                                                                                                                                                                    | Журнал платежей                                                |
| Выписка простого векселя на поставщика       | Оформление платежей поставщикам в качестве способа оплаты. Для использования этого типа журнала, очистите параметр **Создать и разнести журнал выписки автоматически при разноске накладных** на странице **Способы оплаты - поставщики**.                                                                                                                                          | Журнал выписки простых векселей                                   |
| Кластер накладных поставщиков без разноска | Создание проводок по накладным поставщика, которое еще были разнесены на временный счет прибытия.                                                                                                                                                                                                                                                             | Сведения о кластере накладных поставщика без разноски                  |
| Кластер накладных поставщиков               | Создания проводок по кластеру накладных поставщиков.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Регистрация накладной от поставщика          | Разноска накладных поставщика, находящихся в журнале.                                                                                                                                                                                                                                                                                                                 | Журнал накладных                                                |
| Перевыписка простого векселя на поставщика     | Перевыписка простого векселя, который до этого был оплачен вашим банком.                                                                                                                                                                                                                                                                      | Журнал перевыписки простых векселей                                 |
| Сопоставление простого векселя поставщика     | Создание проводок сопоставления по простому векселю поставщика.                                                                                                                                                                                                                                                                                                          | Журнал сопоставления простых векселей                                 |





