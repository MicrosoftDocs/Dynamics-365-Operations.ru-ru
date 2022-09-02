---
title: Завершение, публикация и развертывание функции глобализации
description: В этой статье содержится информация о жизненном цикле функций глобализации.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 11378991a24e1a5f5e213d64f0f414db2e5c2573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279911"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Завершение, публикация и развертывание функции глобализации

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Версии функции электронного выставления счетов

Функции электронного выставления счетов управляются версиями. При создании новой версии номер версии автоматически увеличивается на единицу.

Версии функции электронного выставления накладных следуют жизненному циклу, имеющему три состояния:

- **Черновик** — если версия функции имеет этот статус, можно изменить ее атрибуты конфигурации и ее артефакты (например, конфигурации формата файла).
- **Завершено** — этот статус указывает, что редактирование версии компонента завершено, и не планируется вносить в нее какие-либо дополнительные изменения. Когда версия функции имеет этот статус, вы больше не можете редактировать ее или какие-либо ее компоненты.
- **Опубликовано** — этот статус указывает, что эта версия функции была опубликована в глобальном репозитории, связанном с вашей организацией. Когда версия функции имеет этот статус, вы больше не можете редактировать ее или какие-либо ее компоненты.

Можно указать дату **Действует с** для новой версии функции электронного выставления накладных. Таким образом можно определить версию по умолчанию, которую можно использовать, или которую можно перезаписать, когда функция разворачивается в среде службы.

Чтобы изменить статус версии функции электронного выставления накладных, выполните следующие действия.

1. Выполните вход в учетную запись Regulatory Configuration Services (RCS).
2. В рабочей области **Функция глобализации** в разделе **Функции** выберите плитку **Электронное выставление накладных**.
3. В левой части страницы **Функции электронного выставления накладных** выберите функцию электронного выставления накладных.
4. На вкладке **Версии** в правой части страницы выберите версию.
5. Выберите **Изменить статус**, затем выберите **Завершено** (если текущий статус **Черновик**) или **Опубликовано** (если текущий статус **Завершено**).
6. В окне сообщения выберите **Да**, чтобы подтвердить запрос.

Изменение статуса **Завершено** вручную на статус **Опубликовано** не является обязательным. Версии функций электронного выставления накладных автоматически обновляются до статуса **Опубликовано** при их развертывании в среде службы.

Можно отслеживать статус в столбце **Статус версии функции** на вкладке **Версии**.

## <a name="deploy-feature-versions"></a>Развертывание версий функций

В RCS можно использовать команду **Развернуть**, чтобы опубликовать версию функции электронного выставления накладных в целевой среде службы или подключенном приложении.

1. В левой части страницы **Функции электронного выставления накладных** выберите функцию электронного выставления накладных.
2. На вкладке **Версии** в правой части страницы выберите версию функции электронного выставления накладных, которую необходимо развернуть в среде обслуживания или подключенном приложении. Выбранная версия должна иметь статус **Завершено** или **Опубликовано**.
3. Выберите **Развернуть**, затем выберите один или оба из следующих вариантов, чтобы определить цель развертывания:

    - **Подключенное приложение** — конфигурация, предоставляемая настройкой приложения, записывается в экземпляр Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management, ранее связанный с ней.
    - **Среда службы** — версия функции электронного выставления накладных разворачивается в среде службы. После этого модуль электронного выставления накладных готов к получению и обработке электронных документов, которые отправляются из Finance или Supply Chain Management.

> [!NOTE]
> Обычно изменяются параметры функции электронной отчетности (ER), которая должна быть развернута в среде службы. Изменения в подключенном приложении будут редкими. Разворачивать новые версии в подключенном приложении следует только при изменении соответствующих параметров приложения.

Чтобы определить, развернута ли конкретная версия функции электронного выставления накладных в определенной среде, просмотрите сведения на вкладке **Среды**.

## <a name="remove-feature-versions"></a>Удаление версий функций

В RCS можно выбрать **Отмена** для удаления определенной версии функции электронного выставления накладных из среды службы, если она была развернута там.

> [!IMPORTANT]
> Кнопка **Отмена** работает только для среды службы. Она не удаляет ничего из подключенного приложения для текущей функции электронного выставления накладных.

## <a name="rebase-electronic-invoicing-features"></a>Повторное размещение функций электронного выставления накладных

Если одна функция электронного выставления накладных является производной от другой, можно выбрать **Повторно разместить**, чтобы обновить производную функцию с изменениями, которые были введены в исходной (родительской) функции.

Чтобы повторно разместить производную версию созданной функции, выполните следующие действия.

1. Получите последнюю версию функции, импортировав ее из глобального репозитория. Дополнительные сведения см. в разделе [Импорт функции из глобального репозитория](e-invoicing-import-feature-global-repository.md).
2. В списке функций выберите функцию для повторного размещения.
3. На вкладке **Версии** выберите **Создать**, чтобы создать черновую версию.
4. Выберите **Повторно разместить**.
5. В диалоговом окне **Повторно разместить** выберите версию функции, куда следует выполнить повторное размещение.
6. Нажмите **ОК**.
7. Просмотрите компоненты функции и внесите необходимые изменения.
8. Выберите **Изменить статус** для завершения повторного размещения функции. После завершения повторного размещения можно выполнить дополнительные действия.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Получение определенной версии функций электронного выставления накладных

При создании новой версии функции электронного выставления накладных система создает копию последней версии функции. Чтобы использовать более раннюю версию функции в качестве основы для новой версии, выберите версию, затем выберите команду **Получить эту версию**. Создается новая черновая версия функции, которая является копией выбранной версии.