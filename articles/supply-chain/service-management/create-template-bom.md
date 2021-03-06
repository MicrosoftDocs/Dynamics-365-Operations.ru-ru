---
title: Создание шаблона спецификации
description: Можно создать шаблон спецификации, используя множество методов.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 781df7611ec1e3ee9d3013f971232700df38ada0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836310"
---
# <a name="create-a-template-bom"></a>Создание шаблона спецификации   

[!include [banner](../includes/banner.md)]


Можно создать шаблон спецификации, используя любой из перечисленных ниже методов. Для всех методов поля **Дата начала** и **Дата окончания** необязательны, они предназначены только для сведений.

## <a name="create-a-template-bom-manually"></a>Создание шаблона спецификации вручную

1.  Перейдите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.

2.  Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.

3.  В разделе **Копировать строки спецификации из ссылки** выберите параметр **Вручную**.

4.  В поле **Код номенклатуры** введите номенклатуру типа **Спецификация**.

5.  В поле **Имя** введите имя шаблона.

6.  В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.

7.  Нажмите **ОК**.

Будет создан новый пустой шаблон спецификации.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Создание шаблона спецификации на основе другого шаблона спецификации

1.  Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.

2.  Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.

3.  В разделе **Копировать строки спецификации из ссылки** выберите параметр **Шаблон спецификации**.

4.  В поле **Номер ссылки** выберите имеющийся шаблон спецификации, который необходимо скопировать в новый шаблон.

5.  В поле **Имя** введите имя шаблона.

6.  В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.

7.  Нажмите **ОК**.

Будет создан новый шаблон спецификации с использованием строк, которые соответствуют строкам исходного шаблона спецификации.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Создание шаблона спецификации на основе спецификации номенклатуры

1.  Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.

2.  Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.

3.  В разделе **Копировать строки спецификации из ссылки** выберите **Спецификация**.

4.  В поле **Номер ссылки** выберите версию спецификации. Номенклатура типа "Спецификация" будет скопирована в раздел **Код номенклатуры**.

5.  В поле **Имя** введите имя шаблона.

6.  В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.

7.  Нажмите **ОК**.

Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификации**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Создание шаблона спецификации на основе спецификации производства

1.  Выберите **Управление сервисным обслуживанием** \> **Настройка** \> **Объекты обслуживания** \> **Шаблоны спецификаций**.

2.  Выберите **Создать**, чтобы открыть форму **Создать шаблон спецификации**.

3.  В разделе **Копировать строки спецификации из ссылки** выберите **Производство**.

4.  В поле **Номер ссылки** выберите производственную спецификацию.

5.  В поле **Имя** введите имя шаблона.

6.  В полях **Дата начала** и **Дата окончания** введите интервал дат, в течение которого шаблон спецификации будет активен.

7.  Нажмите **ОК**.

Будет создан новый шаблон спецификации с использованием строк, которые будут соответствовать строкам спецификации, перечисленным в форме **Спецификация**.

## <a name="see-also"></a>См. также

[Шаблоны спецификаций](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]