---
title: Тип места назначения ER архива
description: В этой теме приводятся сведения о настройке места назначения архива для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745593"
---
# <a name="archive-destination"></a>Место назначения архива

[!include [banner](../includes/banner.md)]

Можно настроить место назначения архива для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов. На основании настройки места назначения созданный документ сохраняется в виде вложения записи списка заданий ER.

Этот параметр можно использовать для отправки созданного документа в папку Microsoft SharePoint или хранилище Microsoft Azure. Задайте для параметра **Включено** значение **Да** для отправки выходных данных в место назначения, которое определяется выбранным типом документа. Для выбора доступны только типы, в которых для группы задано значение **Файл**. [Типы](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) документов определяются в разделе **Управление организацией** \> **Управление документами** \> **Типы документов**. Конфигурация для мест назначения электронной отчетности аналогична конфигурации системы управления документами.

[![Страница типов документов](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Расположение определяет, где сохранен файл. После включения места назначения **Архив** результаты можно сохранить в архиве заданий. Можно просмотреть результаты в пункте **Управление организацией** \> **Электронная отчетность** \> **Архивированные задания электронной отчетности**.

> [!NOTE]
> Выберите тип документа для архива заданий в пункте **Управление организацией** \> **Рабочие области** \> **Электронная отчетность** \> **Параметры электронной отчетности**. Дополнительные сведения см. в разделе [Настройка платформы для электронной отчетности (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Можно сохранить файл в указанной папке SharePoint. Чтобы задать сервер SharePoint по умолчанию, перейдите **Управление организацией** \> **Управление документами** \> **Параметры правления документами**. На вкладке **SharePoint** настройте папку SharePoint. Затем ее можно выбрать в качестве папки, в которой будет сохранены выходные данные ER. Местонахождение **SharePoint** должно быть выбрано для этого типа документа.

[![Выбор папки SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Хранилище Azure

Если в качестве расположения типа документа указан **Хранилище Azure**, можно сохранить файл в хранилище Azure.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности (ER)](general-electronic-reporting.md)
- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)
- [Настройка управления документами](../../fin-ops/organization-administration/configure-document-management.md)
