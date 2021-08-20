---
title: Настройка двойной записи из Lifecycle Services
description: В этой теме объясняется, как настроить подключение двойной записи из Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 060734154607263b5fed80b21fc9355b513ea26e3b1be88498310905531dceaa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729051"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Настройка двойной записи из Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме объясняется, как включить двойную запись из Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Необходимые условия

Необходимо завершить интеграцию Power Platform, как описано в следующих темах:

+ [Интеграция Power Platform — включение в ходе развертывания среды](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Интеграция Power Platform — настройка после развертывания среды](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Настройка двойной записи для новых сред Dataverse

Выполните следующие действия, чтобы настроить двойную запись со страницы **Сведения о среде** LCS:

1. На странице **Сведения о среде** раскройте раздел **Интеграция Power Platform**.

2. Выберите кнопку **Приложение двойной записи**.

    ![Интеграция с Power Platform.](media/powerplat_integration_step2.png)

3. Ознакомьтесь с условиями и выберите **Настроить**.

4. Нажмите **ОК**, чтобы продолжить.

5. Можно отслеживать ход выполнения, периодически обновляя страницу сведений о среде. Настройка обычно занимает не более 30 минут.  

6. После завершения настройки появится сообщение о том, что процесс был успешным или произошла ошибка. Если настройка завершилась с ошибкой, отображается соответствующее сообщение об ошибке. Перед переходом к следующему шагу необходимо исправить все ошибки.

7. Выберите **Связать со средой Power Platform** для создания связи между Dataverse и базами данных текущей среды. Это обычно занимает менее 5 минут.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Связать со средой Power Platform.":::

8. После завершения связывания отображается гиперссылка. Используйте ссылку для входа в область администрирования двойной записи в среде Finance and Operations. Отсюда можно настроить сопоставления сущностей.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Настройка двойной записи для существующей среды Dataverse

Для настройки двойной записи существующей среды Dataverse необходимо создать [запрос в службу поддержки](../../lifecycle-services/lcs-support.md) Майкрософт. Запрос должен включать следующее:

+ Код вашей среды Finance and Operations.
+ Имя вашей среды из Lifecycle Services.
+ Код организации Dataverse или код среды Power Platform из центра администрирования Power Platform. В запросе запросите, чтобы идентификатор был экземпляром, используемым для интеграции Power Platform.

> [!NOTE]
> Невозможно удалить связь среды с помощью LCS. Чтобы отменить связь среды, откройте рабочую область **Интеграция данных** в среде Finance and Operations, затем выберите **Удалить ссылку**.

## <a name="linking-mismatch"></a>Несоответствие ссылок

Возможно, что ваша среда LCS связана с одним экземпляром Dataverse, в то время как среда с двойной записью связана с другим экземпляром Dataverse. Несоответствие ссылок может привести к непредсказуемому поведению и попытке передать данные в неправильную среду. Рекомендуемая среда, используемая для двойной записи, является той, которая была создана как часть интеграции Power Platform, и долгосрочной; это единственный способ установить связь между средами.

Если в среде имеется несоответствие ссылок, LCS отображает предупреждение на странице сведений о среде как "Корпорация Майкрософт определила, что ваша среда связана через двойную запись с другим местом назначения, нежели указано в интеграции Power Platform, что не рекомендуется":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Несоответствие ссылки интеграции Power Platform.":::

При возникновении такой ошибки в зависимости от потребностей существует два варианта:

+ [Отмените связь и повторно свяжите среды с двойной записью (выполните сброс или изменение связи)](relink-environments.md#scenario-reset-or-change-linking), как указано на странице сведений о среде LCS. Это идеальный вариант, так как его можно выполнить без поддержки Майкрософт.  
+ Если требуется сохранить связь в двух случаях, можно попросить службу поддержки Майкрософт изменить интеграцию Power Platform для использования существующей среды Dataverse, как описано в предыдущем разделе.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
