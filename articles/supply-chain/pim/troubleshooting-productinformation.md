---
title: Устранение неполадок в информации о продукте
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с информацией о продукте.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841535"
---
# <a name="troubleshoot-product-information"></a>Устранение неполадок в информации о продукте

В этом разделе описывается устранение проблем, которые могут встретиться при работе с информацией о продукте.

## <a name="i-cant-delete-a-released-product"></a>Не удается удалить выпущенный продукт.

### <a name="issue-description"></a>Описание проблемы

Удалить выпущенный продукт и все его варианты можно только в том случае, если выпущенный продукт не имеет каких-либо связанных проводок.

### <a name="issue-resolution"></a>Устранение проблемы

Выполните следующие действия, чтобы удалить выпущенный продукт или шаблон продукта.

1. Закройте все открытые проводки по номенклатурам.
1. Сократите запасы до 0 (нуля).
1. Выполните закрытие запасов.
1. Удалите все варианты продуктов для шаблона продукта, который необходимо удалить.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Можно ли изменить код номенклатуры выпущенного продукта?

В большинстве случаев нельзя редактировать коды номенклатур для выпущенных продуктов, так как это изменение приведет к повреждению данных. Номер номенклатуры можно изменить только в том случае, если необходимо восстановить повреждения данных, которые были вызваны предыдущим переименованием первичного ключа этого выпущенного продукта, как упоминалось в списке [удаленных или устаревших функций для Finance and Operations 10.0.0 с обновлением платформы 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Если вы хотите иметь возможность редактировать коды номенклатур для выпущенных продуктов, [проголосуйте за эту идею на портале идей](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Принцип очистки по умолчанию из продукта не вводится в строку спецификации.

### <a name="issue-description"></a>Описание проблемы

При добавлении номенклатуры в строку спецификации система не использует сведения о принципе очистки по умолчанию, которые настроены для данной номенклатуры. Иными словами, принцип очистки из номенклатуры не появляется на странице **Строка спецификации**.

### <a name="issue-resolution"></a>Устранение проблемы

Если в строке спецификации указан принцип очистки, он будет применяться к этой строке спецификации. Однако если принцип очистки пуст или не задан для строки спецификации, принцип очистки, установленный для номенклатуры, по-прежнему будет применяться к этой строке спецификации, даже если он не отображается в строке спецификации.

Логика задания значений по умолчанию для других функций в Microsoft Dynamics 365 Supply Chain Management обычно не работает таким образом. Однако текущее поведение изменить нельзя. В противном случае некоторые существующие настройки, полагающиеся на него, могут быть нарушены.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Система позволяет сохранять повторяющиеся штрих-коды для разных номенклатур или для одной и той же номенклатуры с различной аналитикой.

В настоящее время система не применяет принудительно уникальные штрих-коды, и добавление этого ограничения было бы радикальным изменением. Фактически, корпорация Майкрософт имеет свидетельства того, что некоторые существующие установки клиентов будут сломаны этим изменением. Однако мы будем рассматривать более широкие изменения в проектировании, чтобы включить эту функцию в будущем.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>При редактировании шаблонов записей номенклатуры выводится следующее сообщение об ошибке: "Местоположение склада не может быть создано, так как номенклатура не является складской. Для хранения номенклатур необходимо выбрать параметр учитываемого в запасах продукта для связанной группы номенклатурных моделей."

### <a name="issue-description"></a>Описание проблемы

Эта проблема возникает, если выполнить следующие шаги для попытки создания шаблона для номенклатуры, которая не хранится в запасах.

1. Откройте выпущенный продукт, который не хранится в запасах.
1. На панели операций откройте вкладку **Параметры** и выберите **Сведения о записи**.
1. В диалоговом окне **Сведения о записи** выберите **Шаблон компании**.

В этом случае вы получите следующее сообщение об ошибке:

> Местоположение склада не может быть создано, так как номенклатура не хранится в запасах. Для хранения номенклатур необходимо выбрать параметр учитываемого в запасах продукта для связанной группы номенклатурных моделей.

### <a name="issue-resolution"></a>Устранение проблемы

Процесс создания шаблонов продуктов требует дополнительной логики для конкретного продукта. Таким образом, нельзя использовать для этой цели универсальную кнопку **Шаблон компании**. Вместо этого выполните следующие действия.

1. Откройте выпущенный продукт.
1. В области действий на вкладке **Продукт** в группе **Создать** выберите **Шаблон \> Создать общий шаблон**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Текст справки по умолчанию, добавляемый в атрибуты продукта, не введен в выпущенный продукт.

Описание и текст справки, добавляемые в атрибуты продукта, не отображаются или не вводятся по умолчанию в выпущенные продукты. Такое поведение предусмотрено разработчиками.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Введенное по умолчанию количество отличается, когда оно регистрируется из спецификации и регистрируется из версии спецификации.

### <a name="issue-description"></a>Описание проблемы

По умолчанию при добавлении номенклатуры в спецификацию количество устанавливается равным 1 вместо количества, определенного в поле **Мин. количество по заказу** на странице **Параметры заказа по умолчанию** для выбранного продукта. Однако если при добавлении номенклатуры из версии спецификации выбрана номенклатура и вариант, количество, введенное по умолчанию, принимает во внимание минимальное количество, которое задается в настройках заказа по умолчанию для определенных аналитик.

### <a name="issue-resolution"></a>Устранение проблемы

Это поведение является ожидаемым. Однако тот факт, что логика отличается в спецификации и в версии спецификации, является известной проблемой. Тем не менее, такое поведение не изменится, так как изменение может повлиять на многие различные сценарии для клиентов.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>В выпущенных сведениях о продукте невозможно изменить присоединенные изображения, отправленные из информационного объекта вложений документов продуктов.

### <a name="issue-description"></a>Описание проблемы

Эта проблема может возникнуть, если изображение прикрепляется к номенклатуре с помощью информационного объекта *Вложения документов продуктов*. В этом случае изображение номенклатуры отображается для данной номенклатуры. Однако если выбрано значение **Изменить изображение**, в списке загруженных изображений ничего не отображается. Кроме того, для этой номенклатуры не отображаются вложения.

### <a name="issue-resolution"></a>Устранение проблемы

Сущность *EcoResProductDocumentAttachmentEntity* (*Вложения документов продуктов*) импортирует вложения документов для *продуктов*, но не для *выпущенных продуктов*. (Выпущенные продукты также называются *номенклатурами*.) Чтобы просмотреть вложения для номенклатуры на странице **Сведения о выпущенных продуктах**, следует использовать сущность *EcoResReleasedProductDocumentAttachmentEntity* (*Вложения документов выпущенных продуктов*) вместо этого.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Соединитель Microsoft Flow показывает следующее сообщение об ошибке: "Обновление не разрешено для поля ProductNumber."

### <a name="issue-description"></a>Описание проблемы

Эта проблема возникает при попытке обновить поле **Номер продукта** с помощью сущности *Выпущенные продукты* версии V2 и Microsoft Flow.

### <a name="issue-resolution"></a>Устранение проблемы

Это поведение является ожидаемым. Возможность редактирования номера продукта для выпущенного продукта была удалена в Dynamics 365 Finance and Operations 10.0.0 с обновлением платформы 24, чтобы предотвратить повреждение данных. В исключительных случаях, когда необходимо восстановить повреждение данных, вызванное предыдущим переименованием первичного ключа выпущенного продукта, вы можете попросить службу поддержки Майкрософт, чтобы временно удалить это ограничение.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Не удается создать вариант выпущенного продукта в другом юридическом лице.

### <a name="issue-description"></a>Описание проблемы

При попытке выпуска шаблона продукта без вариантов и последующего создания вариантов в каждом юридическом лице (компании), когда они необходимы, вы не сможете выпустить варианты, используя предложения вариантов. Вы также не сможете создавать варианты вручную.

### <a name="issue-resolution"></a>Устранение проблемы

Такое поведение предусмотрено разработчиками. Отношения шаблона продукта и аналитик, которые может принимать шаблон, хранятся на общем уровне. Таким образом, невозможно создать доступные аналитики для общего шаблона продукта в конкретном юридическом лице, где эти аналитики выпускаются, а затем реплицировать процесс в каждом юридическом лице, где эти аналитики требуются. Вместо этого необходимо изменить процесс выпуска для адаптации к спроектированному процессу.

Ниже приводится процесс выпуска продуктов.

1. Создайте общий шаблон продукта и аналитики, которые могут быть выпущены юридическим лицам.
1. Выпустите продукты для юридических лиц, используя предложения вариантов или вручную добавляя комбинации, которые должны быть выпущены.

Кроме того, можно непосредственно создать выпущенный продукт.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>При выпуске варианта в другой компании появляется следующее сообщение об ошибке: "Вариант продукта с указанными аналитиками уже был создан."

### <a name="issue-description"></a>Описание проблемы

Если вариант продукта уже был выпущен в компании A, и вы пытаетесь выпустить его в компании B с помощью кнопки **Создать** на странице **Варианты выпущенного продукта**, появится следующее сообщение об ошибке:

> Вариант продукта с выбранными аналитиками уже создан.

### <a name="issue-resolution"></a>Устранение проблемы

Кнопка **Создать** на странице **Варианты выпущенного продукта** создает вариант и выпускает его в контексте компании. Если этот вариант уже был создан, нельзя использовать кнопку **Создать**, чтобы выпустить его в другой компании.

Чтобы исправить ошибку, откройте страницу **Шаблон продукта** и выберите **Выпустить продукт**, чтобы выпустить существующий вариант в нужной компании.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]