---
title: Настройка назначений ER, относящиеся к записи управления печатью
description: В этой теме объясняется, как настроить назначения, относящиеся к записи управления печатью, для формата электронной отчетности, настроенного для создания исходящих документов.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1e06fafe8d8bbe92ddf4fcd94d7271a1fbb6362a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413613"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Настройка назначений ER, относящиеся к записи управления печатью

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как пользователь с ролью системного администратора или сотрудника по расчетам с клиентами может выполнять следующие задачи:

- Настройте назначения с именами [Электронная отчетность (ER)](general-electronic-reporting.md) для решения ER, которое создает накладные с произвольным текстом.
- Присвоение назначения ER отдельной записи [управления печатью](document-reporting-services.md).

Процедуры можно выполнить в компании USMF. Написание кода не требуется.

## <a name="introduction"></a>Введение

Можно настроить [места назначения](electronic-reporting-destinations.md) для каждой папки в компоненте исходящих файлов [конфигурации](general-electronic-reporting.md#FormatComponentOutbound) [формата](general-electronic-reporting.md#Configuration) электронной отчетности (ER), используемой для создания исходящего документа. При выполнении формата электронной отчетности данного типа, если есть соответствующие права доступа, можно также изменять настроенные параметры пункта назначения во время выполнения.

В Microsoft Dynamics 365 Finance **версии 10.0.17 и более поздних** код действия можно [настроить](er-apis-app10-0-17.md) для формата электронной отчетности, чтобы указать действие, выполняемого пользователями путем выполнения формата электронной отчетности. Например, в модуле **Расчеты с клиентами** в настройках управления печатью можно выбрать формат электронной отчетности, который создает конкретный деловой документ, например накладную с произвольным текстом. Затем можно выбрать **Просмотр** для предварительного просмотра накладной или **Печать**, чтобы отправить ее на принтер. Если действие передается в выполняемый формат электронной отчетности во время выполнения, можно [настроить другие пункты назначения электронной отчетности для других действий пользователя](er-action-dependent-destinations.md).

В Finance **версии 10.0.21 и более поздней** именованное место назначения можно [настроить](er-apis-app10-0-21.md) для формата ER и назначить записи управления печатью, обрабатываемой при запуске этого формата ER. Например, в модуле **Расчеты с клиентами** в параметрах управления печатью необходимо настроить запись **Оригинал** для выполнения следующих действий:

- Выполнение формата ER.
- Отправка созданной накладной клиенту по электронной почте.
- Настройте запись **Копия** для однократного выполнения формата.
- Печать копии накладной на сетевом принтере.

В этом случае необходимо настроить другие назначения ER для выполняемого формата ER, а также выбрать места назначения для других записей управления печатью.

## <a name="prerequisites"></a>Необходимые условия

Перед тем как начать, нужно включить функцию **Разрешить настройку мест назначения ER для каждого элемента управления печатью** в рабочей области [Управление функциями](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Исходный код также должен быть изменен, чтобы получить возможность настройки именованных назначений ER в текущем экземпляре Finance и включить [новый](er-apis-app10-0-21.md) API ER.

Кроме того, в конфигурация ER **Накладная с произвольным текстом (Excel)** должна быть [импортирована](er-download-configurations-global-repo.md) в ваш экземпляр Finance.

## <a name="configure-a-new-er-destination"></a>Настройка нового места назначения ER

1. Перейдите в раздел **Расчеты с клиентами** \> **Накладные** \> **Все накладные с произвольным текстом**.
2. Выберите накладную для счета клиента **US-001**.
3. На странице **Накладная с произвольным текстом** на вкладке **Накладная** в группе **Управление печатью** выберите **Управление печатью**.
4. На странице **Настройка управления печатью** разверните **Модуль — Расчеты с клиентами** \> **Документы** \> **Накладная с произвольным текстом**, выберите запись **Оригинал** и выполните следующие шаги:

    1.  Обратите внимание на текущие настройки выбранной записи:
        -   Отчет по умолчанию SSRS **FreeTextInvoice.Report** выбран в поле **Формат отчета**.
        -   Имя **\<Default\>** отображается в поле **Назначение** и сообщается, что для назначенного отчета SSRS не выбрано пользовательское назначение. 
    2.  В поле **Формат отчета** выберите конфигурацию формата ER **Настраиваемая накладная с произвольным текстом (Excel)**.
        -   Имя поля **Назначение** изменяется на **Имя назначения**.
        -   Имя **\<No named destination\>** отображается в поле **Имя назначения** и сообщается, что для назначенного формата ER не выбрано назначение с именем.
    3.  Нажмите кнопку со стрелкой вправо поля **Имя назначения**.    
    4. На странице **Назначение электронной отчетности с именем** в поле **Имя** введите **Основное назначение**.
    5. Нажмите **Сохранить**.
    6. На экспресс-вкладке **Назначение файла** [настройте](er-destination-type-email.md) назначение **Электронная почта** для компонента **Отчет**.
    7. Закройте страницу **Назначение электронной отчетности с именем**.
    8. На странице **Настройка управления печатью** в поле **Имя назначения** выберите назначение с именем **Основное назначение**.

    ![Настройка именованного назначения ER для выбранного формата ER и назначение его настроенной записи управления печатью на странице Настройка управления печатью](./media/er-named-destinations-01.gif)

    Теперь вы настроили именованное назначение ER **Основное назначение** для формата **Накладная с произвольным текстом (Excel)** и назначили его записи управления печатью **Оригинал** в **Модуль — расчеты с клиентами** \> **Документы** \> **Накладная с произвольным текстом**.

5. Разверните **Модуль — расчеты с клиентами** \> **Организация — US-001** \> **Накладная с произвольным текстом**, выберите запись **Оригинал** и выполните следующие действия:

    1. Выберите и удерживайте (или щелкните правой кнопкой мыши) запись, затем выберите **Переопределить**.
    2. Нажмите кнопку со стрелкой вправо поля **Имя назначения**.
    3. На странице **Назначение электронной отчетности с именем** на панели операций выберите **Создать**.
    4. В поле **Имя** введите **Назначение US-001**.
    5. На экспресс-вкладке **Назначение файла** [настройте](er-destination-type-print.md) назначение **Принтер** для компонента **Отчет**.
    6. Закройте страницу **Назначение электронной отчетности с именем**.
    7. На странице **Настройка управления печатью** в поле **Имя назначения** выберите назначение с именем **Назначение US-001**.

    ![Настройка именованного назначения ER для выбранного формата ER и назначение его настроенной записи управления печатью на странице Настройка управления печатью](./media/er-named-destinations-02.gif)

    Теперь вы настроили именованное назначение ER **Назначение US-001** для формата **Накладная с произвольным текстом (Excel)** и назначили его записи управления печатью **Оригинал** в **Модуль — расчеты с клиентами** \> **Организация — US-001** \> **Накладная с произвольным текстом**.

После обработки накладной с произвольным текстом выполняется формат **Накладная с произвольным текстом (Excel)**, и происходит одно из следующих событий:

- Если накладная с произвольным текстом относится к клиенту, отличному от US-001, созданный документ отправляется по электронной почте.
- Если накладная с произвольным текстом относится к клиенту US-001, созданный документ идет на печать.

> [!NOTE]
> Если именованное назначение не определено для записи управления печатью, которая обрабатывается во время выполнения, используются назначения ER по умолчанию, если они доступны для выполняющегося формата ER.

> [!IMPORTANT]
> На странице **Назначение электронной отчетности** (**Администрирование организации** \> **Электронная отчетность** \> **Назначение электронной отчетности**) при выборе формата ER, для которого был настроено по крайней мере одно именованное назначение, вы получаете уведомление о наличии именованных назначений.
>
> ![Уведомление о существовании настроенных именованных назначений для выбранного формата ER на странице назначения электронной отчетности](./media/er-named-destinations-03.png)
>
> При удалении назначения по умолчанию также удаляются все именованные места назначения. Если для записей управления печатью были выбраны именованные назначения, выбор этих именованных назначений отменяется.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Копирование существующего назначения ER в новое именованное назначение

Если для формата ER существует именованное назначение ER по умолчанию, его можно использовать в качестве шаблона для новых назначений ER. Чтобы создать новое назначение ER, которое основано на назначении по умолчанию, выберите **Копировать из значения по умолчанию** на странице **Назначение электронной отчетности с именем**. Новое назначение называется **По умолчанию**. Этот шаг можно повторять столько раз, сколько необходимо.

Можно выбрать любое существующее именованное назначение в качестве шаблона для нового именованного назначения. Чтобы создать новое именованное назначение ER, которое основано на выбранном назначении, выберите **Копировать** на странице **Назначение электронной отчетности с именем**. Новое назначение имеет то же имя, что и выбранное именованное назначение, но добавляется суффикс "Копия". Этот шаг можно повторять столько раз, сколько необходимо.

## <a name="security-considerations"></a>Вопросы безопасности

Именованные назначения ER можно настроить на странице **Настройка управления печатью** только в том случае, если имеется [разрешение](../sysadmin/role-based-security.md#permissions) на выполнение этой задачи. Разрешение может быть предоставлено, если **Настройка места назначения форматов электронной отчетности** [(обязанность)](../sysadmin/role-based-security.md#duties) назначена для одной из ваших [ролей безопасности](../sysadmin/role-based-security.md#security-roles). Дополнительные сведения см. в разделе [Вопросы безопасности](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности (ER)](general-electronic-reporting.md)

[Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)

[Изменения в API платформы электронной отчетности для Application update 10.0.17](er-apis-app10-0-17.md)

[Изменения в API платформы электронной отчетности для Application update 10.0.21](er-apis-app10-0-21.md)

[Измените код, чтобы разрешить пользователям настраивать и использовать именованные назначения ER](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]