---
title: Создание каталога закупаемой продукции
description: В этой статье объясняется, как создать каталог закупаемой продукции.
author: GalynaFedorova
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e35e8c5b5c93fa9aac914f04e7ea658748cb052
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869556"
---
# <a name="create-a-procurement-catalog"></a>Создание каталога закупаемой продукции

[!include [banner](../../includes/banner.md)]

В этой статье объясняется, как создать каталог закупаемой продукции. Эта задача обычно выполняется специалистом по закупкам. Вы также узнаете, как сотрудники могут использовать каталог при создании заявки. Перед созданием каталога в системе должна существовать иерархия категорий закупаемой продукции. Иерархия наследуется новым каталогом вместе со всеми продуктами в иерархии. Это руководство можно использовать в компании с демонстрационными данными USMF, в которой доступна иерархия категорий закупаемой продукции, а также примеры, используемые в шагах процедуры.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Убедитесь, что иерархия категорий закупаемой продукции существует.
1. Выберите **область переходов > Модули > Закупки и источники > Категории закупаемой продукции**. Иерархия категорий закупаемой продукции доступна в компании с демонстрационными данными USMF, и продукты добавлены в категорию **Оборудование для офиса/компьютеры**. Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство, чтобы пролистать категорию. Если иерархия была недоступна, ее можно создать, нажав кнопку **Создать**. Это можно делать только один раз.  
2. Закройте страницу.

## <a name="create-a-catalog"></a>Создание каталога
1. Выберите **область переходов > Модули > Закупки и источники > Каталоги > Каталоги закупаемой продукции**.
2. Выберите **Создать каталог закупаемой продукции**, чтобы открыть раскрывающееся диалоговое окно.
3. В поле **Имя** введите значение.
4. Нажмите **ОК**.
5. В дереве разверните узел **КОРПОРАТИВНЫЕ КАТЕГОРИИ ЗАКУПАЕМОЙ ПРОДУКЦИИ**.
6. В дереве разверните узел **ОФИСНОЕ ОБОРУДОВАНИЕ**.
7. В дереве выберите узел **Компьютеры**.

  - Продукты из категории закупаемой продукции отображаются в списке. Если необходимо добавить продукт в категорию, это можно сделать на странице **Иерархия категорий закупаемой продукции** или на странице **Сведения о номенклатуре**.  
  - Тип обновления **По умолчанию** определяет, будут ли новые продукты, добавленные в иерархию категорий закупаемой продукции, отображаться сразу же в каталоге. Если для типа обновления задано значение **Динамический**, изменения будут отображаться незамедлительно. Если для типа обновления задано значение **Статический**, новые продукты будут отображаться только для пользователей, использующих каталог после повторной публикации каталога. Действие **Опубликовать** доступно в области действий в верхней части страницы. Если продукты удаляются из иерархии категорий закупаемой продукции, изменение отображается немедленно независимо от значения в поле типа обновления **По умолчанию**.  

8. На панели действий выберите **Навигация по категории** и убедитесь, что выбрано значение **Включить**.
9. Выберите **Активировать каталог**.
10. Закройте страницу.

## <a name="make-the-catalog-visible"></a>Отображение каталога
1. Выберите **область навигации > Модули > Закупки и источники > Настройка > Политики > Политики закупок**.
2. Выберите **Политика закупок USMF**. Необходимо выбрать политику закупок для юридического лица, с которым связан работник и в котором профиль пользователя может заказывать продукты. В компании с демонстрационными данными USMF администратор связан с работником **Julia Funderburk**, и она заказывает продукты в USMF по умолчанию.  
3. Выберите только что созданный каталог.
4. Нажмите **ОК**.

## <a name="use-the-catalog"></a>Использование каталога
1. Перейдите в **область перехода > Модули > Закупки и источники > Заявки на покупку > Все заявки на покупку**.
2. Выберите **Создать**.
3. В поле **Имя** введите значение.
4. Нажмите **ОК**.
5. Выберите **Добавить продукты**.
6. В списке найдите и выберите требуемую запись. Можно использовать иерархию категорий слева или фильтр вверху списка, чтобы отфильтровать продукты.  
7. Выберите **Добавить в строки**.
8. Нажмите **ОК**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]