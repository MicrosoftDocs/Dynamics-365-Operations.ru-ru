---
title: Страница списка проводок по поставщику
description: В этой теме содержится информация о странице списка "Проводки по поставщику" в Microsoft Dynamics 365 Finance.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6008a968568806bdf2c3194d32aecf9f67dbce2b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179650"
---
# <a name="vendor-transactions-list-page"></a>Страница списка проводок по поставщику

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Просмотр сопоставлений

Кнопка **Просмотр сопоставлений** в области действий обеспечивает быстрый доступ к истории сопоставления и подробной информации о проводке сопоставления. Также можно отображать дополнительные проводки, связанные с выбранной проводкой — либо потому что они входят в то же сопоставление, либо потому что они представляют собой платежи, созданные в том же журнале платежей.

1. Выберите **Расчеты с поставщиками \> Все поставщики**.
2. Выберите поставщика, по которому имеются проводки, а затем в области действий на вкладке **Поставщик** выберите **Проводки**.
3. Выберите проводку, которую требуется изучить, а затем в области действий выберите **Просмотр сопоставлений**.

    Появится диалоговое окно **Просмотр сопоставлений** с выбранной проводкой и всеми документами, которые с ней сопоставлены. Это диалоговое окно напоминает представление истории сопоставления, однако включает в себя все связанные документы.

4. В этом диалоговом окне можно выполнять различные задачи. Выберите один или несколько ваучеров, а затем выберите одну из следующих кнопок:

    - **Просмотр связанной информации** — отображение всех проводок журнала платежей и проводок финансового журнала для поставщика, которые были созданы в журналах, в которых были созданы документы, отображаемые в списке. Например, если отображается платеж, то все платежи в журнале платежей, в котором он был создан, будут отображаться. Если отображается накладная или платеж, созданный в общем журнале, будут отображены все документы в общем журнале, в котором он был создан. Также отображаются все сопоставления, связанные со списком документов. При просмотре связанных платежей название этой кнопки меняется на **Просмотр сопоставлений**. Выберите **Просмотр сопоставлений**, чтобы отобразить только те проводки, которые отображались при первом открытии диалогового окна **Просмотр сопоставлений**.
    - **Просмотр журнала** — просмотр истории сопоставлений для ваучеров. Выберите **Закрыть**, чтобы закрыть диалоговое окно.
    - **Просмотр учета** — отображаются все ваучеры, связанные с выбранными документами. Выберите **Закрыть**, чтобы закрыть диалоговое окно.
    - **Экспорт** — экспорт выбранных ваучеров в Microsoft Excel.
    - **Сопоставление проводок** — эта кнопка отображается, только если исходный выбранный документ не был полностью сопоставлен. Если ее нажать, появится диалоговое окно **Сопоставление проводок**, где можно выбрать проводки для сопоставления.
    - **Отменить сопоставление** — эта кнопка отображается, только если исходный выбранный документ был полностью сопоставлен. Если ее нажать, появится диалоговое окно **Отменить сопоставление**, где можно отменить сопоставления, сделанные для этого документа.

## <a name="global-transactions"></a>Глобальные проводки

Кнопка **Глобальные проводки** также отображается на странице списка **Проводки по поставщику**. Эта кнопка позволяет просмотреть все проводки по поставщику во всех юридических лицах. На странице списка **Проводки по поставщику** отображаются проводки только для юридических лиц, к которым у пользователя есть доступ в соответствии с его параметрами безопасности.

На странице списка отображаются все операции для поставщиков, которые имеют тот же код субъекта, что и поставщик, с которого вы начали. Например, если поставщик US-001 в одном юридическом лице имеет тот же код субъекта, что и поставщик DE-001 в другом юридическом лице, отображаются все проводки для обоих кодов поставщика.

Меню на странице списка **Проводки по поставщику** могут быть разными в зависимости от юридического лица в проводке. Например если какая-либо функция доступна только для швейцарских юридических лиц, пункты меню для этой функции отображаются только при выборе швейцарский проводки.

Чтобы получить доступ к этой функции, выполните следующие действия.

1. Выберите **Расчеты с поставщиками** \> **Все поставщики**.
2. Выберите поставщика, а затем в области действий на вкладке **Поставщик** в группе **Проводки** выберите **Глобальные проводки**.

## <a name="more-transaction-filters"></a>Другие фильтры для проводок

Фильтр для отображения открытых проводок заменен новым фильтром, который позволяет просматривать больше сочетаний проводок. В поле **Показать** доступны следующие варианты:

- **Все** — отображение всех проводок для выбранных поставщиков (открытых и закрытых).
- **Закрыто** — отображение только тех проводок, которые полностью сопоставлены и закрыты.
- **Открыто** — отображение только тех проводок, которые не сопоставлены полностью.
- **Открыть в том числе закрытые на дату или после нее** — отображение только проводок, которые еще не были полностью сопоставлены в указанную дату или после нее. При выборе этого параметра можно изменить дату, которая отображается рядом с фильтром. Проводки, у которых значение параметра **Дата последнего сопоставления** совпадает с указанной вами датой или позже нее, отображаются в списке, даже если по состоянию на текущую дату эти проводки полностью сопоставлены. Однако сальдо представляет собой сальдо по состоянию на текущую дату, а не по состоянию на выбранную дату.

Установите флажок **Скрыть переоценки валюты**, чтобы скрыть проводки валютной переоценки.

## <a name="modify-due-dates-and-discount-dates"></a>Изменение сроков оплаты и дат скидок

Вы можете изменять сроки оплаты и даты скидок для открытых проводок по клиентам. В выпуске 8.1 теперь можно добавить сроки оплаты на странице списка **Проводки по поставщику**. Щелкнув дату срока оплаты на странице списка **Проводки по поставщику**, также можно изменить сроки оплаты, даты скидок, условия оплаты и условия скидок по оплате в диалоговом окне **Обновление срока оплаты и даты скидок по оплате**.

### <a name="activate-the-feature"></a>Активация функции

Чтобы добавить на страницу списка **Проводки по поставщику** сроки оплаты и иметь возможность изменять параметры оплаты для проводки с помощью диалогового окна **Обновление срока оплаты и даты скидок по оплате**, выполните следующие действия.

1. Выберите **Расчеты с поставщиками \> Настройка \> Параметры расчетов с поставщиками**.
2. На вкладке **Сопоставления** установите параметр **Показать срок оплаты и разрешить изменения** в значение **Да**.
3. Для работы этой функции в проводки по поставщикам были добавлены новые поля. Эти поля будут заполняться при совершении новой проводки. Они также заполняются при открытии диалогового окна **Обновление срока оплаты и даты скидок по оплате**. Установив для параметра **Показать срок оплаты и разрешить изменения** значение **Да**, вы увидите диалоговое окно **Обновить сведения об оплате**.  Чтобы сразу же обновить существующие проводки, выберите **Обновить все существующие проводки**. Или, чтобы заполнять поля только для новых проводок, выберите **Продолжить без обновления**.

Срок оплаты добавляется на страницу списка **Проводки по поставщику**, чтобы можно было легко изменять сроки оплаты и даты скидок по оплате для проводок.

### <a name="modify-the-payment-settings"></a>Изменение параметров оплаты

На странице списка **Проводки по поставщику** отображаются все проводки по поставщику. При выборе срока оплаты для проводки открывается диалоговое окно. В этом диалоговом окне отображается базовая дата для расчетов срока оплаты и скидок, дата, соответствующая сроку оплаты, условия оплаты, условия скидки и даты скидок по оплате.

Каждое поле по-своему влияет на проводку при его редактировании:

- **Редактировать базовую дату** — срок оплаты и даты скидок меняются, как если бы базовая дата была равна дате документа.
- **Редактировать срок оплаты** — изменяется только дата, соответствующая сроку оплаты
- **Редактировать даты скидок** — изменяются только даты скидки.
- **Редактировать условия оплаты** — изменяется дата, соответствующая сроку оплаты, в зависимости от базовой даты и условий оплаты.
- **Редактировать условия скидки по оплате** — изменяются скидки по оплате, в зависимости от базовой даты и условий скидок по оплате.

Закончив редактировать параметры оплаты, выберите **Закрыть** для сохранения изменений.