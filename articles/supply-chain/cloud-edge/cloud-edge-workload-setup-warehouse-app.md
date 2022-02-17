---
title: Настройка мобильного приложения Warehouse Management для облачных и пограничных единиц масштабирования
description: В этой теме объясняется, как настроить мобильные приложения Warehouse Management для складов, обслуживаемых облачной или пограничной единицей масштабирования.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071661"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Настройка мобильного приложения Warehouse Management для облачных и пограничных единиц масштабирования

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как настроить мобильные приложения Warehouse Management, чтобы их можно было использовать на складах, обслуживаемых облачной или пограничной единицей масштабирования.

## <a name="prerequisites"></a>Необходимые условия

Прежде чем начать настройку мобильных устройств для подключения к облачной или пограничной единице масштабирования, убедитесь, что они могут подключиться к узлу предприятия. Дополнительные инструкции см. в разделе [Установка и подключение мобильного приложения Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Дополнительная настройка при выполнении мобильного приложения Warehouse Management для единицы масштабирования

В рамках [процесса развертывания для рабочих нагрузок единицы масштабирования склада](cloud-edge-landing-page.md#scale-unit-manager-portal) большая часть данных, необходимых для подключения устройств мобильного приложения Warehouse Management, автоматически синхронизируется с концентратором предприятия в единицу масштабирования. Однако необходимо ввести данные на странице **приложений Azure Active Directory** (**Администрирование системы \> Настройка \> Приложения Azure Active Directory**) в развертывании единицы масштабирования. Кроме того, может потребоваться обновить значение **Компания** по умолчанию для кода пользователя или создать нового пользователя. Пользователи, связанные с компанией, которая не существует в развертывании единицы масштабирования, не смогут войти в систему, когда мобильное приложение Warehouse Management будет подключено к этой единице масштабирования.

> [!NOTE]
> Поскольку данные на странице **приложений Azure Active Directory** не синхронизированы, эти данные необходимо изменить вручную, если необходимо переместить рабочие нагрузки склада в другую единицу масштабирования.

Помните, что как часть настройки подключения для мобильного приложения Warehouse Management указанный URL-адрес ресурса Azure Active Directory должен использоваться для единицы масштабирования вместо концентратора предприятия.
