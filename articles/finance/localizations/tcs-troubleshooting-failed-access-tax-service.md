---
title: Не удалось получить доступ к налоговой службе
description: В этой теме описывается, как устранять неполадки в случае сбоя доступа к службе расчета налогов.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388561"
---
# <a name="failed-to-access-tax-service"></a>Не удалось получить доступ к налоговой службе

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

В этой теме объясняется, как исправить ошибку "Сбой доступа к налоговой службе" в службе расчета налогов.

## <a name="symptoms"></a>Симптомы

В Microsoft Dynamics 365 Finance вы переходите к пункту **Налог** \> **Настройка** \> **Конфигурация налогов** \> **Параметры налоговой службы**. На вкладке **Общие** вы включаете параметр **Включить расчет налога**. Если затем попытаться выбрать значение в поле **Имя настройки функции**, произойдет ошибка. Сообщение об ошибке содержит следующий текст: "Не удалось получить доступ к налоговой службе".

## <a name="cause"></a>Причина

Эта ошибка происходит из-за того, что Finance не может получить доступ к службе расчета налогов.

## <a name="resolution"></a>Решение 

1. Выполните вход в Microsoft Dynamics Lifecycle Services (LCS).
2. На странице **Среда** на вкладке **Надстройки среды** найдите пункт **Расчет налога** и проверьте его статус. Статус должен быть **Устанавливается** или **Установлен**. Если надстройка службы расчета налогов не установлена, будет выведено сообщение об ошибке.

## <a name="mitigation"></a>Снижение риска

1. В LCS на странице **Finance** в разделе **Интеграция Power Platform** выберите **Установить новую надстройку**.
2. Перейдите в нижнюю часть страницы и выберите надстройку **Расчет налога**, чтобы установить ее.
3. Вернитесь в среду Finance и попытайтесь получить доступ к службе расчета налогов.

> [!NOTE]
> Перед установкой службы расчета налогов проверьте [необходимые условия для службы расчета налогов](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Если не удается установить надстройку, поскольку раздел **Интеграция Power Platform** недоступен, см. раздел [Обзор надстройки](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Если ошибка продолжает возникать после установки надстройки, обратитесь к системному администратору.
