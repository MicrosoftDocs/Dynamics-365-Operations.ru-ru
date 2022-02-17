---
title: Dynamics 365 Finance и Dynamics 365 Supply Chain Management в облаке правительственного сообщества США (GCC)
description: В этой теме содержатся сведения о продуктах Microsoft Dynamics 365 US Government, доступных для квалифицированных правительственных органов и частных организаций.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062294"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance и Dynamics 365 Supply Chain Management в облаке правительственного сообщества США (GCC)

[!include [banner](../includes/banner.md)]



Выберите продукты Microsoft Dynamics 365 United States (US) Government, доступные квалифицированным государственным и частным организациям. Эти организации ограничены следующими типами:

- Государственные органы США федерального уровня, уровня штата, местные, племенные и территориальные органы
- Частные организации, которые используют Dynamics 365 US Government, чтобы предоставлять решения для правительственных субъектов или квалифицированным членам сообщества облака
- Частные субъекты, имеющие клиентские данные, которые регулируются правительственными нормативами, и Dynamics 365 US Government является подходящей службой для соответствия нормативным требованиям

Дополнительные сведения см. в разделе [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Чтобы выполнить первоначальное внедрение для проекта реализации в Microsoft Dynamics Lifecycle Services (LCS), следуйте инструкциям в разделе [Адаптация проекта реализации](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Однако не используйте ссылку на публичную службу LCS, предоставляемые в этих инструкциях. Вместо этого используйте следующий URL-адрес, чтобы открыть LCS для облака сообщества для государственных учреждений США (GCC): <https://gov.lcs.microsoftdynamics.us>.

После завершения первоначальной адаптации следуйте указаниям в разделе [Адаптация проекта](../lifecycle-services/project-onboarding.md). Снова используйте [LCS для GCC](https://gov.lcs.microsoftdynamics.us) вместо общедоступной службы LCS.

## <a name="environment-deployment"></a>Развертывание среды

После выполнения проекта адаптации можно просмотреть дополнительные возможности LCS, описанные в разделе [Lifecycle Services (LCS) для клиентов приложений Финансы и операции](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Затем перейдите к развертыванию среды.

- Чтобы развернуть управляемые корпорацией Майкрософт среды через службу LCS, следуйте указаниям в разделе [Lifecycle Services (LCS) для клиентов приложений Финансы и операции](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Для сред, размещенных в облаке, см. раздел [Развертывание сред разработки и доступ к ним](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Также необходимо выполнить процесс адаптации Resource Manager для ваших соединителей, как описано в разделе [Завершение процесса адаптации Azure Resource Manager для проектов Lifecycle Services для государственных организаций США](arm-onbarding-us-goverment.md).

> [!NOTE]
> Для проектов LCS для государственных организаций США поддерживаются только специальные подписки Azure для государственных организаций.

## <a name="features-that-arent-available"></a>Функции, которые недоступны

Некоторые функции не будут доступны для развертывания в GCC, или они не будут доступны для использования с Dynamics 365 в GCC. Например, службы Azure DevOps будут недоступны в GCC. Однако могут использоваться локальные службы Azure DevOps или общедоступные службы Azure DevOps. Подробные сведения о доступности функций см. в разделе [Доступность функций бизнес-приложений для государственных организаций США](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Вопросы и ответы

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Поддерживаются ли Dynamics 365 Finance и Dynamics 365 Supply Chain Management в GCC-High?

Нет. Dynamics 365 Finance и Dynamics 365 Supply Chain Management поддерживаются только в GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Можно ли использовать общедоступную службу Azure DevOps с модулем Finance и Supply Chain Management в GCC?

Да, можно использовать общедоступные службы Azure DevOps, если нет требований для решения, сертифицированного Федеральной программой аккредитации облачных служб (FEDRAMP). В качестве альтернативы можно использовать сервер Azure DevOps.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Можно ли развернуть среду разработки уровня 1 размещенной в облаке среды в подписке Azure Commercial?

Нет. В [LCS для GCC](https://gov.lcs.microsoftdynamics.us) необходимо использовать подписку Azure для государственных организаций для развертывания облачной среды.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Что можно сделать, если требуется пакет из библиотеки общих активов, но он недоступен в LCS для GCC?

Этот же пакет можно загрузить из библиотеки общих активов в [общедоступной службе LCS](https://lcs.dynamics.com). Кроме того, ваш партнер может помочь вам в загрузке пакета.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Доступно ли средство обновления кода в GCC?

Нет, в данный момент средство обновления кода недоступно в GCC. Однако можно создать проект перспективного клиента в [общедоступной службе LCS](https://lcs.dynamics.com) и использовать средство обновления кода. Обратите внимание, что развертывание сред в проектах перспективных клиентов невозможно.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Может ли партнер открыть запрос в службу поддержки от моего имени?

Да. Однако если ваш партнер использует идентификатор не в GCC, запрос в службу поддержки будет перенаправлен в очередь общедоступной поддержки. Для запросов в службу поддержки рекомендуется использовать объем обслуживания GCC клиента в службе LCS.

## <a name="see-also"></a>См. также

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Доступность функций бизнес-приложений для государственных организаций США](https://aka.ms/BAPFunctionalParity).
- [Руководство пользователя Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Обзор облачного развертывания](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
