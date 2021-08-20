---
title: Включение Power BI для глобального учета запасов
description: В этой теме описывается, как включить Microsoft Power BI для глобального складского учета.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 562b56a85ad2f40cb673f8f2101bf92c39853d1f1a087d0498b6f7d19d1cca01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773353"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Включение Power BI для глобального учета запасов

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Можно закреплять плитки, панели мониторинга и отчеты из учетной записи [PowerBI.com](https://powerbi.com/) в вашей рабочей области приложения Microsoft Dynamics 365.

## <a name="prerequisites"></a>Необходимые условия

Прежде чем можно будет включить отчетность Power BI, должны быть выполнены следующие условия:

- Вы должны быть системным администратором в приложении Dynamics 365.
- Необходимо иметь учетную запись [PowerBI.com](https://powerbi.com/).
- В учетной записи Power BI должна быть хотя бы одна панель мониторинга и один отчет.
- Вы должны быть администратором вашей учетной записи Azure Active Directory (Azure AD).
- Домен Azure AD должен быть тем же доменом, который использовался для учетной записи [PowerBI.com](https://powerbi.com/).

## <a name="setup"></a>Настройка

Чтобы настроить интеграцию Power BI, выполните следующие действия.

1. Выполните вход в [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Перейдите к **библиотеке общих ресурсов**, выберите **модель отчета Power BI** в качестве типа актива и загрузите пакет **Глобальный складской учет**. 
1. Выполните вход в [PowerBI.com](https://app.powerbi.com/) и отправьте файл **Глобальный учет запасов** Power BI, выполнив следующие шаги:

    1. Выберите **Создать**.
    1. Выберите **Отправить файл**.
    1. Выберите файл отчета **Глобальный учет запасов** Power BI.

1. Настройте отчет **Глобальный учет запасов** Power BI, выполнив следующие шаги:

    1. Перейдите **Моя рабочая область**, найдите набор данных для глобального складского учета и затем в меню **Параметры** выберите **Настройки**.
    1. В **Настройки глобального учета запасов** разверните **Параметры** и обновите все необходимые параметры.

1. Зарегистрируйте приложение, как описано в [Настройка интеграции PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Интегрируйте файл отчета **Глобальный учет запасов** Power BI в Dynamics 365 Supply Chain Management, выполнив следующие шаги:

    1. Перейдите в раздел **Администрирование системы \> Настройка \> Конфигурация PowerBI.com**.
    1. Выберите **Правка**.
    1. Выберите **Включить интеграцию PowerBI.Com**.
    1. В поле **Код приложения** введите код приложения.
    1. В поле **Ключ приложения** введите ключ приложения.
    1. Нажмите **Сохранить**.

1. Обновите страницу, чтобы отображалось диалоговое окно входа Power BI.
1. На вкладке **Параметры** выберите **Открыть каталог отчетов**, а затем выберите файл отчета **Глобальный учет запасов** Power BI, который был отправлен ранее.
1. Обновите страницу. Вы увидите, что отчет добавлен.
1. В **Отчеты Power BI** выберите ссылку **Глобальный учет запасов**.

Дополнительные сведения см. в разделе [Настройка интеграции PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
