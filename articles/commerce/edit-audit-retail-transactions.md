---
title: Редактирование и аудит проводок розничного магазина
description: В этом разделе описываются функции редактирования и аудита проводок магазина.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004397"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Редактирование и аудит проводок розничного магазина

[!include [banner](includes/banner.md)]



Клиенты Dynamics 365 Commerce используют собственные и сторонние POS-приложения. При работе с собственными POS-приложениями проводки магазина переносятся в Headquarters из каналов через процесс пакетной обработки. В случае сторонних приложений проводки переносятся в Headquarters через интеграцию. В обоих случаях после передачи проводок в Headquarters необходимо выполнить проверку их согласованности, чтобы в журналы, которые будут разноситься в Headquarters, попали только проверенные проводки. 

Проверка проводок Commerce может оказаться неудачной по разным причинам. Например, расхождение в данных может быть вызвано ошибкой в коде интеграции или в POS-приложении, а также ошибкой пользователя, например удалением продукта после его синхронизации с каналом или закрытием финансового периода без разноски проводок.

Хотя эти проводки помечаются и исключаются из журналов, они могут повлиять на повседневные операции разноски операций.

В Commerce можно редактировать отдельные проводки, которые не прошли проверку, и при этом сохранять историю всех изменений. 

## <a name="edit-and-audit-transactions"></a>Редактирование и аудит проводок

В Retail 10.0.5 можно редактировать только проводки с использованием наличных, такие как продажи и возвраты. Редактирование заказов клиентов и интернет-заказов не поддерживается. В Retail 10.0.6 и более поздних версий также поддерживается редактирование проводок управления кассами.

1. Установите надстройку Dynamics Excel.

2. Перейдите в рабочую область **Финансовая информация магазина**. Плитка **Ошибки проверки проводок** содержит предварительно отфильтрованное представление формы проводки, для которой не соблюдается одно или несколько правил проверки.
 
3. Откройте форму. Щелкните запись, не прошедшую проверку, выберите **Надстройка Office**, а затем выберите **Изменить выбранную проводку**. Откроется файл Excel с информацией о выбранной проводке. Он содержит следующие листы:

    - Строки: на этом листе имеются строки заголовка и продуктов, а также соответствующие данные по проводкам.
    - Платежи: на этом листе содержатся подробные сведения о строках оплаты для проводки.
    - Скидки: на этом листе содержатся сведения о скидках по проводкам.
    - Налоги: на этом листе содержатся сведения о налогах по проводкам.
    - Расходы: на этом листе содержатся сведения о расходах по проводкам.

4. В файле Excel необходимо изменить соответствующие поля, а затем загрузить эти данные в Headquarters с помощью функции публикации в надстройке Dynamics Excel. После публикации изменения будут отражены в системе. Во время публикации вносимые пользователями изменения не проверяются.

5. Чтобы открыть полный аудиторский след, выберите **Просмотр данных аудиторского следа** под заголовком **Проводка розничной торговли** для изменений на уровне заголовка или в соответствующем разделе и записи на странице проводки. Например, все изменения, относящиеся к строкам продажи, отображаются на странице **Проводки по продажам**, к платежам — на странице **Проводки по оплате** и т. д. Для аудита изменений сохраняются следующие данные:

   - Дата и время изменения
   - Поле 
   - Старое значение
   - Новое значение
   - Кто изменил

6. После внесения и публикации изменений снова выберите команду **Проверить проводки магазина**, чтобы убедиться в том, что изменения правильны и согласованы.

> [!NOTE]
> Редактировать можно только проводки, не прошедшие проверку. Если необходимо изменить проводку, которая прошла проверку, измените статус проверки такой проводки на **Ошибка** или **Нет**, после чего она станет доступной для изменений. 


## <a name="bulk-edit-transactions"></a>Массовое изменение проводок

В Retail 10.0.6 и более поздних версий поддерживается массовое изменения проводок на уровне журнала операций. 

1. Воспользуйтесь надстройкой Excel, чтобы открыть журнал операций с нужными проводками, как было описано в шагах 1–3 выше.

2. Выберите один из перечисленных ниже параметров.

    - **Изменить кассовые проводки**. Этот параметр позволяет редактировать все кассовые проводки в журнале операций Доступны следующие листы Excel.
    
       - **Проводка**: на этом листе приведена вся информация уровня заголовков по всем проводкам продаж.
       - **Проводка продаж**: на этом листе приведена вся информация уровня строк по всем проводкам продаж.
       - **Проводки по оплате**: на этом листе приведена вся информация строк оплаты по всем проводкам продаж.
       - **Проводки по скидкам**: на этом листе приведена вся информация строк скидок по всем проводкам продаж.
       - **Налоговые проводки**: на этом листе приведена вся информация строк налогов по всем проводкам продаж.
       - **Проводки расходов**: на этом листе приведена вся информация строк расходов по всем проводкам продаж.

    - **Изменить проводки управления кассой**. Этот параметр позволяет редактировать все проводки управления кассой в журнале операций Доступны следующие листы Excel.
     
       - **Проводка**: на этом листе приведена вся информация уровня заголовков по всем проводкам управления кассой.
       - **Проводки по платежному средству для внесения в банк**: на этом листе приведена вся информация по проводкам внесения средств в банк.
       - **Проводки по платежному средству для внесения в сейф**: на этом листе приведена вся информация по проводкам внесения средств в сейф.
       - **Декларирование платежных средств**: на этом листе приведена вся информация по проводкам декларирования платежных средств.
       - **Проводки по доходам/расходам**: на этом листе приведена вся информация по строкам проводок по доходам и расходам.
       - **Проводки по оплате**: на этом листе приведена вся информация по платежам для операции **Оплата накладной**, а также по проводкам по доходам и расходам.

3.  При публикации массовых изменений проводок проверка не выполняется. Вы должны самостоятельно следить точностью изменений и согласованностью данных на всех листах. Например, если вам нужно изменить дату проводки в ситуации, когда финансовый или учетный период для открытой проводки был закрыт, необходимо изменить эту дату на всех листах Excel, на которых есть столбец **Бизнес-дата**. Чтобы проверить проводки после их изменения воспользуйтесь командой **Заново проверить проводки** на странице **Журналы операций**.