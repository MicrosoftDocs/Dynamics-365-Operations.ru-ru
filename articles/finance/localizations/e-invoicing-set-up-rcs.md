---
title: Настройка Regulatory Configuration Service (RCS)
description: В этой статье описывается, как настроить службу Regulatory Configuration Service (RCS).
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 63a4f77d6e80133947dff678cef3885167ec55be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285798"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Настройка Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

В этой статье описывается, как настроить службу Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Включение функций глобализации

1. Войдите в учетную запись RCS.
2. Выберите плитку **Управление функциями**.
3. В рабочей области **Управление функциями** выберите **Функции глобализации** в списке и выберите **Включить**.

Плитка для рабочей области **Функции глобализации** должна теперь появиться на главной панели мониторинга RCS.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Настройка параметров для интеграции RCS с модулем электронного выставления накладных

1. В рабочей области **Функции глобализации** в разделе **Связанные параметры** выберите **Параметры электронной отчетности**.
2. На вкладке **Электронное выставление накладных** в поле **Универсальный код ресурса (URI) конечной точки службы** введите соответствующую конечную точку службы для своего географического расположения Microsoft Azure, как показано в следующей таблице.

    | География центра обработки данных Azure | Универсальный код ресурса (URI) конечной точки службы |
    |----------------------------|----------------------|
    | Соединенные штаты              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Европа                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Соединенное Королевство             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Азия                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Япония                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Швейцария                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Бразилия                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Объединенные Арабские Эмираты       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Австралия                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Канада                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Франция                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Индия                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Убедитесь, что в поле **Код приложения** установлено значение **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Это значение является фиксированным значением. Убедитесь, что введен только глобальный уникальный идентификатор (GUID), и что значение не содержит никаких других символов, таких как пробелы, запятые, точки или кавычки.
4. В поле **Код среды LCS** введите идентификатор вашей среды Microsoft Dynamics Lifecycle Services (LCS). Это значение представляет собой ссылку на среду Finance или Supply Chain Management, которая будет использоваться со службой электронного выставления накладных. Чтобы получить идентификатор, войдите в [LCS](https://lcs.dynamics.com/), откройте проект, затем на вкладке **Управление средой** в разделе **Сведения о среде** найдите поле **Код среды**.

    > [!IMPORTANT]
    > Если надстройка электронного выставления накладных устанавливается в нескольких средах Finance или Supply Chain Management в LCS, всегда используйте код среды последней установленной среды. Если вы решили установить надстройку в новой среде после настройки и работы с функцией электронного выставления накладных, обновите поле **Код среды LCS** в RCS до самого последнего значения.

5. Выберите **Сохранить** и закройте страницу.

## <a name="configuration-providers"></a>Поставщики конфигураций

Поставщики конфигурации можно использовать, чтобы отличать владельцев конфигураций электронной отчетности (ER), используемых в процессах электронного выставления накладных, и владельцев функций глобализации. Для всех функций глобализации, предоставляемых корпорацией Майкрософт и опубликованных в глобальном репозитории, поставщик конфигурации устанавливается в значение **Microsoft** (`http://microsoft.com`).

Можно корректировать только конфигурации электронной отчетности и функции глобализации, принадлежащие поставщику активной конфигурации. Эти конфигурации и функции можно использовать в качестве шаблонов для создания конфигураций и функций, относящихся к активному поставщику конфигураций, чтобы их можно было скорректировать.

Сначала создайте поставщиков конфигураций. Затем установите один из них в качестве активного. Невозможно установить поставщика конфигурации **Microsoft** в качестве активного.

### <a name="create-a-configuration-provider"></a>Создание поставщика конфигураций

1. В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Поставщики конфигурации**.
2. Выберите **Создать**.
3. В поле **Имя** введите уникальное имя для поставщика конфигурации.
4. В поле **Интернет-адрес** введите уникальный URL-адрес поставщика конфигурации.
5. Выберите **Сохранить** и закройте страницу.

### <a name="select-a-configuration-provider-as-active"></a>Выберите поставщика конфигурации как активного

1. В списке поставщиков конфигурации выберите поставщик конфигурации, который необходимо сделать активным.
2. Выберите **Установить активные**.

## <a name="import-er-configurations-from-the-global-repository"></a>Импорт конфигураций электронной отчетности из глобального репозитория

1. В рабочей области **Электронная отчетность** в разделе **Связанные ссылки** выберите **Поставщики конфигурации**.
2. В списке поставщиков конфигурации выберите **Microsoft**, затем выберите **Репозитории**.
3. Выберите **Глобальный**, затем в области действий выберите **Открыть**.
4. Импортируйте следующие модели электронной отчетности:

    - **Модель контекста накладной клиента**
    - **Модель накладных**
    - **Финансовые документы** (для сценариев Бразилии, если это необходимо)
    - **Модель ответного сообщения**

5. Если **Сопоставление модели накладных** не было импортировано автоматически, импортируйте его.
6. Закройте страницу.
