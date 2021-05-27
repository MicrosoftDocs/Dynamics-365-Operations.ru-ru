---
title: Настройка информации о группе TDS, PAN и TAN для поставщиков и клиентов
description: В этой теме объясняется, как настроить сведения о группе налога, удержанного в источнике (TDS), номере постоянного счета (PAN) и номере налогового счета (TAN) для поставщиков и клиентов.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023539"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Настройка информации о группе TDS, PAN и TAN для поставщиков и клиентов

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как настроить сведения о группе налога, удержанного в источнике (TDS), номере постоянного счета (PAN) и номере налогового счета (TAN) для поставщиков и клиентов.

1. Перейдите **Расчеты с поставщиками \> Поставщики \> Все поставщики** или **Расчеты с клиентами \> Клиенты \> Все клиенты**.

    [![Страница "Все поставщики"](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. В области действий выберите **Создать**, чтобы создать поставщика или клиента, и введите требуемые сведения. Или выберите существующего поставщика или клиента.
3. На экспресс-вкладке **Накладные и поставка** в разделе **Подоходный налог** установите параметр **Рассчитать подоходный налог** как **Да**, чтобы рассчитать подоходный налог, TDS или налог, удержанный в источнике (TDS), для поставщика или клиента.
4. TDS для накладной по покупке рассчитывается на основе группы TDS по умолчанию, которая определена для поставщика или клиента. В поле **Группа TDS** выберите группу TDS по умолчанию.

    > [!NOTE]
    > Если выбрать группу TDS в поле **Группа TDS**, поля **Группа подоходного налога** и **Группа TCS** становятся недоступными.

5. На экспресс-вкладке **Сведения о налоге** в разделе **Сведения о PAN** в поле **Статус** выберите статус постоянного номера счета для поставщика или клиента:

    - **Недоступно** — у поставщика или клиента нет PAN.
    - **Получено** — у поставщика или клиента есть PAN.
    - **Применяется** — поставщик или клиент подали заявку на PAN.
    - **Недопустимо** — у поставщика или клиента есть PAN, но он недопустимый.

6. Если выбрано **Получено** в поле **Статус**, чтобы указать, что у поставщика или клиента есть PAN, введите PAN в поле **Номер**. PAN должен состоять из пяти букв, затем четырех цифр, а затем одной буквы. Пример: **ABCDE1260A**.
7. Если выбрано **Применено** в поле **Статус**, чтобы указать, что поставщик или клиент подал заявку на PAN, введите справочный номер в поле **Справочный номер**.
8. В поле **Суть налогоплательщика** выберите суть категории налогоплательщика, к которой относятся поставщик или клиент:

    - Организация
    - HUF
    - Утверждение
    - Индивидуальный
    - AOP
    - BOI
    - Локальный орган
    - Прочее

    [![Экспресс-вкладка "Сведения о налоге"](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. На панели операций на вкладке **Поставщик** в группе **Регистрация** выберите **Регистрационные номера**, чтобы открыть страницу **Управление адресами**.
10. На странице **Управление адресами** на экспресс-вкладке **Сведения о налоге** выберите **Добавить** или **Изменить**, чтобы открыть страницу **Управление сведениями о налогах**, где можно вести запись регистрации налога.
11. На странице **Управление сведениями о налоге** на экспресс-вкладке **Подоходный налог** в поле **Номер налогового счета (TAN)** введите TAN. TAN должен состоять из четырех букв, затем пяти цифр, а затем одной буквы. Пример: **AFGH54821T**.
12. Закройте страницу.