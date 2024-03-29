---
title: Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)
description: В этой статье описывается порядок работы с кодами Национальной классификации грузов, перевозимых автотранспортом (NMFC) в Microsoft Dynamics 365 Supply Chain Management
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c173057b8e1357790e780469c5806afb857be62a
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838344"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)

[!include [banner](../includes/banner.md)]

Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC) позволяют классифицировать номенклатуры, которые могут быть отгружены. Код NMFC — это обозначение, используемое для группирования товаров. Он позволяет компаниям-перевозчикам оценивать товары для отгрузки, классифицируя номенклатуры на основе таких соображений, как пригодность для автомобилей, проблемы с загрузкой, проблемы с обращением расходами и склонность к порче. Товары группируются в один из 18 классов фрахта, используя диапазон чисел от 50 до 500. Класс, в котором сгруппирован товар, основан на оценке четырех транспортных характеристик: плотность, пригодность для перевозки в контейнере, погрузочно-разгрузочные операции и обязательства. Вместе эти характеристики определяют пригодность товара к транспортировке.

Код NMFC связан с каждой номенклатурой отгрузки классы неполной нагрузки (LTL). Например, ноутбуку может быть назначен NMSC с классом 2,5, в то время как у электрических проводов может быть NMSC с классом 65.

Эта функция может помочь работникам использовать коды NMFC для классификации номенклатур отгрузки LTL. Далее приводятся некоторые примеры.

- Если компания включает описание фрахта в транспортную накладную, перевозчик получит представление о фрахте. Фрахт является важной классификацией, поскольку многие транспортные компании основывают свои бизнес-модели по типам фрахта, которые они отгружают.
- Эта классификация может оказаться обязательной для вашей компании, поскольку она используется для определения затрат на данную загрузку.
- Ваша компания может определить прибыльность логистики LTL и транспортной компании.

В этой статье описывается, как работать с кодами NMFC в Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Необходимые условия

Прежде чем можно будет создавать коды NMFC, необходимо настроить все классы фрахта LTL, которые должны быть сопоставлены с ними. Классы фрахта LTL представляют категории номенклатур, тогда как коды NMFC относятся к отдельным товарам в каждом из 18 классов фрахта. Дополнительные сведения о том, как работать с классами LTL, см. в разделе [Классы неполной загрузки (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Создайте код NMFC

Чтобы создать код NMFC, выполните следующие действия.

1. Выполните одно из следующих действий.

    - Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Коды NMFC**.
    - Перейдите в раздел **Управление транспортировкой \> Настройка \> Стандарты транспортировки \> Коды NMFC**.

1. Выберите **Создать**, чтобы создать код NMFC. Затем задайте следующие поля:

    - **Код NMFC** — введите код NMFC для типа товара.
    - **Имя** — введите имя кода NMFC.
    - **Класс LTL** — выберите класс LTL, связанный с кодом NMFC.
    - **Единица обработки BOL** — определение типа обработки по умолчанию для отгрузки.

## <a name="example-set-up-nmfc-codes"></a>Пример: настройка кодов NMFC

В следующем примере показано, как настроить два различных кода NMFC, которые могут использоваться для различных продуктов.

1. Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Коды NMFC** или **Управление транспортировкой \> Настройка \> Стандарты транспортировки \> Коды NMFC**.
1. В области действий выберите **Создать**.
1. В новой строке установите следующие значения:

    - **Код NMFC:** *92,5*
    - **Название:** *Компьютеры*
    - **Класс LTL:** *92,5*
    - **Единица обработки BOL:** *Единица*

1. На панели операций выберите **Сохранить**.
1. В области действий выберите **Создать**.
1. В новой строке установите следующие значения:

    - **Код NMFC:** *125*
    - **Название:** *Телефоны*
    - **Класс LTL:** *125*
    - **Единица обработки BOL:** *Единица*

1. На панели операций выберите **Сохранить**.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Классы неполной загрузки (LTL)](ltl-class.md)
- [Создание транспортной накладной](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
