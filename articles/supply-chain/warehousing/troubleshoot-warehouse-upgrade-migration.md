---
title: Устранение неполадок при обновлении и миграции до расширенного управления складом
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c07c5894f340fde2834e95d53fa390ec5789feeca9b3902e56c333da0d143f5b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747801"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Устранение неполадок при обновлении и миграции до расширенного управления складом

[!include [banner](../includes/banner.md)]

В этой теме описывается устранение распространенных проблем, которые могут встретиться при обновлении и переходе на расширенное управление складом.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Я получаю следующее сообщение об ошибке: "java.security.cert.certPathValidatorException: не найдена привязка доверия для пути сертификации."

### <a name="issue-description"></a>Описание проблемы

Вы получаете это сообщение об ошибке в мобильном приложении управления складом, поскольку сертификаты с собственной подписью не являются доверенными для Android 8+ в локальных средах.

### <a name="issue-resolution"></a>Устранение проблемы

Используйте внешний (общий) центр сертификации (ЦС). Исправление для этой проблемы доступно в версии 1.9.0.0 приложения склада. Дополнительные сведения об этой проблеме и ее устранении см. в разделе [Устранение неполадок при подключении к мобильному приложению управления складом](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Каков утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом?

### <a name="issue-description"></a>Описание проблемы

В настоящее время вы работаете под управлением складом/запасами и с использованием базовой функции запасов, и хотите перейти к расширенной работе со складом, чтобы воспользоваться преимуществами мобильных устройств, волн и работы. Однако возникают проблемы при попытке выполнить этот переход. Например, невозможно изменить продукты таким образом, чтобы они использовали аналитики хранения (сайт, склад и местоположение), так как у продуктов имеются проводки по ним. Поэтому вы должны изучить утвержденный процесс для перехода от базовой работы со складом к расширенной работе со складом.

### <a name="issue-resolution"></a>Устранение проблемы

Для получения дополнительных сведений о процессе перехода от базовой работы со складом на расширенную работу со складом, см. следующие записи блога и документацию:

- [Включение процесса управления складом для существующих номенклатур и складов](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Миграция Microsoft Dynamics AX WMS на новые функции склада и транспортировки R3](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [Миграция элементов WMSI/WMS2](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Обновление управления складом с Microsoft Dynamics AX 2012 до Supply Chain Management](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]