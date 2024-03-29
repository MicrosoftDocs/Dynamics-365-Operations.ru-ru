---
title: Инжиниринговые компаний и правила владения данными
description: В этой статье объясняется, как можно использовать одну или несколько технологических компаний, чтобы обеспечить централизованное создание и ведение основных данных для продуктов. Инженерная компания представляет собой компанию, которая владеет технологическими продуктами и его техническими данными.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47662203669d5dd466990be397c9a4aaf1dd9932
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875549"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Инжиниринговые компаний и правила владения данными

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Инженерные компании и операционные компании

Чтобы обеспечить централизованное создание и ведение основных данных для продуктов, можно использовать одну или несколько *инженерных компаний*. Инженерная компания владеет технологическими продуктами и их техническими данными. Она всегда связано с (основана на) существующим *юридическим лицом*, которое также является компанией. Через это соединение система устанавливает центральную точку входа для всех инженерных данных для технологических продуктов в инженерной компании. В этой центральной точке входа создаются технологические продукты и сохраняются инженерные данные. Из нее технологические продукты и инженерные данные выпускаются в *операционные компании*, которые являются другими юридическими лицами. (Дополнительные сведения об управлении выпуском см. в разделе [Выпуск структур продуктов](release-product-structure.md).) Эти операционные компании будут использовать инженерные данные в том виде, в котором они были разработаны инженерной компанией. Все данные логистики обслуживаются локально каждой инженерной компанией и рабочей компанией.

Чтобы создать инженерную компанию, перейдите в раздел **Управление техническими изменениями \> Настройка \> Инженерные организации**. Выберите **Создать**, введите имя для инженерной компании и выберите существующую компанию (юридическое лицо), на которой она основана.

При интеграции с внешними системами управления жизненным циклом продуктов (ПЛМ) необходимо создать бизнес-единицу (типа компании), который станет внешней компанией.

## <a name="engineering-product-categories-and-engineering-companies"></a>Категории инженерных продуктов и инженерные компании

*Категории технологических продуктов* помогают обеспечить создание технологических продуктов в соответствии с бизнес-правилами компании и их требуемое поведение. Дополнительные сведения о категориях технологических продуктов см. в разделе [Инженерные версии и категории технологических продуктов](engineering-versions-product-category.md).

Каждая категория технологических продуктов относится к конкретной инженерной компании и может создавать только продукты, принадлежащие данной компании. Аналогично, право на поддержание инженерного продукта также принадлежит компании, связанной с категорией технологического продукта для данного продукта.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Данные, принадлежащие инженерной компании

Так как инженерная компания владеет инженерными данными, она управляет следующими процессами:

- **Создание технологических продуктов:** каждая инженерная компания может создавать новые технологические продукты только на основе категории технологических продуктов, которая ей принадлежит. В некоторых случаях операционные компании сохраняют собственные локальные данные, имеющие отношение к этим продуктам.
- **Создание технологических версий:** когда компания создает новый технологический продукт, система автоматически создает для него исходную инженерную версию. Новые версии этого продукта могут создаваться только инженерной компанией, владеющей им.
- **Создание и ведение инженерных атрибутов:** когда компания создает новый технологический продукт, система автоматически добавляет в него инженерные атрибуты. Только владеющая инженерная компания сможет создавать и поддерживать значения для этих атрибутов. Дополнительные сведения об инженерных атрибутах см. в разделе [Инженерные атрибуты и поиск инженерных атрибутов](engineering-attributes-and-search.md).
- **Создание и поддержка спецификаций, которые подключены к инженерным версиям:** владеющая инженерная компания может напрямую связать спецификацию с версией инженерного продукта. Когда эти спецификации выпускаются для других юридических лиц, изменения в инженерных данных в спецификациях будут ограничиваться следующим образом:

    - Операционная компания не может удалить выпущенные строки спецификации.
    - Инженерные поля в строках спецификаций доступны только для чтения для операционной компании. Все остальные поля являются полями внедрения логистики и могут редактироваться операционной компанией.
    - Операционная компания может добавить строки спецификации в ту же спецификацию. Таким образом, она может добавлять локальные дополнения, такие как упаковочные материалы или смазочные жидкости.
    - Операционная компания может добавить абсолютно новую локальную спецификацию. Это изменение может потребоваться в тех случаях, когда, например, в процессе выпуска не указана спецификация. Операционная компания владеет и поддерживает эти локальные спецификации. Дополнительные сведения об управлении выпуском см. в разделе [Структуры выпущенных продуктов](release-product-structure.md).
    - Все локальные спецификации и строки спецификаций сохраняются, когда инженерная компания обновляет свою спецификацию.

- **Создание и поддержка маршрутов, которые подключены к инженерным версиям:** владеющая инженерная компания может напрямую связать маршрут с каждой инженерной версией. Когда эти маршруты выпускаются для других юридических лиц, изменения в данных в маршрутах ограничиваются следующим образом:

    - Другие юридические лица не могут удалить инженерные данные по маршрутам.
    - Остальные юридические лица могут добавлять операции к маршруту. Таким образом, они могут добавлять шаги локального маршрута.
    - Операционные компании могут добавить абсолютно новые локальные маршруты. Это изменение может потребоваться если, например, вы не включили маршруты в процессе выпуска. Операционные компании владеют и поддерживают эти локальные маршруты. Дополнительные сведения об управлении выпуском см. в разделе [Структуры выпущенных продуктов](release-product-structure.md).
    - Все изменения, сделанные локально, сохраняются, когда обновления из инженерной компании выпускаются снова в маршруты.

- **Создание и сопровождение технологических документов:** инженерная компания может прикладывать технологические документы к каждой из технологических версий.

    - Когда эти документы выпускаются для других юридических лиц, эти документы защищаются от удаления операционной компанией.
    - Другие юридические лица могут добавлять совершенно новые локальные документы. Операционная компания владеет и поддерживает эти локальные документы.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]