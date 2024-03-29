---
title: Реверсирование платежа поставщику
description: В этой статье описывается разница между реверсированием, удалением, аннулированием и отклонением платежа, и как сторнировать чек поставщика.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheelo
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db82446d42a6d6fd69757d837fb8544e9b2fb224
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715812"
---
# <a name="reverse-a-vendor-payment"></a>Реверсирование платежа поставщику

[!include [banner](../includes/banner.md)]

В этой статье описывается разница между реверсированием, удалением, аннулированием и отклонением платежа. Кроме того, объясняются два метода для реверсирования чека поставщика. 

Иногда, после того как платеж поставщика был разнесен, платеж необходимо реверсировать. Реверсирование отличается от удаления, аннулирования или отклонения платежа. Вы можете удалить платеж, только если он имеет статус **Создано**. Этот статус показывает, что платеж был создан, но пока не был произведен. Это ограничение всегда применяется, независимо от метода платежа. Вы можете аннулировать неразнесенные чеки после их генерирования, но до их разноски. Если произведенная оплата сделана как электронный платеж (EFT), то вы можете отклонить платеж до его разноски. Чтобы отклонить платеж, измените значение **Статус платежа**. Аннулированный или отклоненный платеж можно сгенерировать после изменения значения параметра **Статус платежа** обратно на **Нет**. 

После того как платеж разнесен, используются реверсирования. Платежи, которые сделаны электронно, нельзя реверсировать после их разноски. Вместо этого необходимо создать новую проводку для суммы платежа, чтобы вернуть задолженность назад на счет поставщика. Предусмотрено два метода реверсирования разнесенных чеков. В одном методе реверсирования разносятся сразу же после нажатия **Отмена платежа** на странице **Чек**. В другом методе при нажатии кнопки **Отмена платежа** на странице **Чек** реверсирование отправляется в журнал сторнирований банковских чеков в модуле "Управление банком и кассовыми операциями", где проверяющий может разнести или отклонить реверсирование. 

Чтобы узнать, который метод ваша организация использует, посмотрите страницу **Параметры управления банком и кассовыми операциями**. Если для параметра **Использовать процесс просмотра для отмены платежей** задано значение **Да**, то реверсирования отправляются в журнал сторнирований банковских чеков для проверки. В следующей таблице описываются различия методов реверсирования чеков.

| Если реверсирования чеков не проверяются перед разноской в организации                                                                                                                                  | Если реверсирования чеков проверяются перед разноской в организации                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Чек сторнируется сразу же после нажатия кнопки **OK** на странице **Чек**.                                                                                                                      | Чек реверсируется не сразу. Создается журнал реверсирования чеков для просмотра. Если журнал реверсирования чеков удалить, чек можно реверсировать повторно.                                                                                                                                                                                                                                                                |
| Записи учета для исходного чека реверсируются.                                                                                                                                         | Счет ГК из первоначальной записи учета чека может быть не разнесен. Финансовые аналитики из журнала исходного чека используются как финансовые аналитики по умолчанию в журнале реверсирования чеков. Значения по умолчанию можно изменить. Когда журнал реверсирования чеков разнесен, счета главной книги для модуля "Расчеты с поставщиками" вводятся автоматически из профилей разноски, которые могли измениться. |
| Структуры учета, которые использовались при разноске исходного чека, используются для реверсирования чека, даже если структура счета была изменена. Комбинация счетов не проверяется. | При изменении структуры счета после разноски исходного чека может потребоваться новая финансовая аналитика для реверсирования чека. Эта финансовая аналитика может быть не введена автоматически из журнала первоначального платежа. Комбинация счетов проверяется при разноске реверсирования чека.                                                                                                        |
| Фиксированные аналитики не применяются к реверсированию, чтобы помочь гарантировать, что будут реверсированы те же счета ГК.                                                                                      | Фиксированные аналитики применяются к журналу реверсирования чеков во время разноски. Значение финансовой аналитики может не существовать в записи учета для исходного чека в зависимости от того, когда была определена фиксированная аналитика.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Реверсирование разнесенных чеков без просмотра
Если в организации требуется разнести реверсирования чеков сразу при нажатии кнопки **Отмена платежа** на странице **Чеки**, выполните следующие действия. На странице **Параметры управления банком и кассовыми операциями** задайте для параметра **Использовать процесс просмотра для отмены платежей** значение **Нет**. На странице **Чеки** вы можете выбрать чек для обращения и выбрать **Отмена платежа**. Затем можно ввести дату и выбрать причину сторнирования.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Реверсирование разнесенных чеков после просмотра в журнале реверсирования чеков
Если ваша организация хочет проверять реверсирования чеков перед их разноской, создайте журнал сторнирований банковских чеков для проверки и на странице **Параметры управления банком и кассовыми операциями** задайте для параметра **Использовать процесс просмотра для отмены платежей** значение **Да**. На странице **Чеки** вы можете выбрать чек для обращения и выбрать **Отмена платежа**. Затем можно ввести дату и выбрать причину сторнирования. Финансовая причина должна быть настроена для обоих типов "Банк" и "Поставщик". Также необходимо выбрать имя журнала для создания журнала в журнале сторнирований банковских чеков.

### <a name="review-a-reversal"></a>Проверка сторнирования

Если вы пользователь, который должен проверять реверсирования, вы можете одобрить и разнести журнал или отклонить реверсирование путем удаления журнала. На странице **Журнал реверсирования чеков** вы можете выбрать журнал реверсирования для проверки, затем нажать **Строки**. Вы можете проверить сторнированный чек, затем выберите один из следующих параметров утверждения:

-   Чтобы утвердить и разнести журнал сторнирования, щелкните **Разноска** или **Разноска и перенос**.
-   Чтобы отклонить реверсирование, удалите журнал реверсирования чеков.

> [!NOTE]
> Удаление журнала приведет к удалению реверсирования из системы, но исходный чек останется на странице **Чек**. Статус этого чека больше не будет **Отмена незаконченного процесса**.

## <a name="results-of-posting-a-reversal"></a>Результат разноски сторнирования
При разноске проводок сторнирования чека происходят следующие события:

-   Статус чека обновляется до состояния **Отмена**.
-   Если во время реверсирования на странице реверсирования был выбран параметр **Выверить**, чек выверяется (выбран параметр **Выверено**) и не появляется на странице **Выверка счетов**.
-   Операция сторнирования разносится на банковский счет, который использовался при выпуске чека, что приводит к увеличению сальдо банковского счета.
-   Операция разносится в главную книгу.
-   Сведения об изменениях обновляются в группе полей **История** на странице **Чек**.

> [!NOTE] 
> При реверсировании чека, который был выпущен для проводки внутрихолдинговой торговли, корреспондирующие записи поступают из настройки учета для внутрихолдинговой торговли, а не из исходной проводки. Если сторнированный чек был выпущен для платежа поставщику, также происходят следующие события:

-   Исходный платеж по накладной, с которым был сопоставлен платеж по чеку, не используется (сопоставление отменяется).
-   Для реверсирования платежа проводка разносится на счет поставщика, и реверсированный платеж сопоставляется с исходным платежом. Поле **Последний ваучер сопоставления** на странице **Проводки по поставщику** для исходной выплаты поставщику обновляется, чтобы отразить код операции сторнированной проводки.

Если сторнированный чек был выпущен для возвращения клиенту, также происходят следующие события:

-   Для реверсирования платежа проводка разносится на счет клиента, и сопоставление между исходным платежом и документом, с которым первоначально был сопоставлен платеж, реверсируется (создается отрицательный платеж).
-   Сторнирование платежа применяется по отношению к исходному платежу. Поле **Последний ваучер сопоставления** на странице **Проводки по клиенту** для исходного платежа клиента обновляется, чтобы отразить код операции сторнированной проводки.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
