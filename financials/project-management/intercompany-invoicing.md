---
title: "Внутрихолдинговое выставление накладных"
description: "В этой статье представлены сведения и примеры внутрихолдингового выставления накладных по проектам в Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 8a606f81e6e66390bf0add3deeeb032ab4cbd90b
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-invoicing"></a>Внутрихолдинговое выставление накладных

[!include[banner](../includes/banner.md)]


В этой статье представлены сведения и примеры внутрихолдингового выставления накладных по проектам в Microsoft Dynamics 365 for Operations.

В организации может быть несколько подразделений, филиалов и других юридических лиц, которые обмениваются между собой продуктами и услугами в связи с проектами. Юридическое лицо, которое предоставляет услуги или продукт, называется *сдающим в аренду юридическим лицом*, а юридическое лицо, которое получает услугу или продукт, называется *заимствующим юридическим лицом*. 

На следующем рисунке показан типичный сценарий, в котором два юридических лица SI FR (заимствующее юридическое лицо) и SI USA (сдающее в аренду юридическое лицо) совместно используют ресурсы для выполнения проекта для клиента А. В этом сценарии SI FR обязуется выполнить работу для клиента А. 

[![Пример внутрихолдингового выставления накладных](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Цель — сделать управление затратами, признание выручки, налоги и трансферную цену для внутрихолдинговых проводок по проекту более мощными и гибкими. Кроме того, предоставляются следующие возможности:

-   Создание накладных клиента для проекта в заимствующем юридическом лице с помощью внутрихолдинговых табелей учета рабочего времени, расходов и накладных поставщика в сдающем в аренду юридическом лице.
-   Поддержка расчетов налогов и косвенных затрат.
-   Перенос признания выручки в сдающем в аренду юридическом лице и времени признания затрат заимствующим юридическим лицом.
-   Начисление дохода по незавершенному производству (НЗП) в сдающем в аренду юридическом лице.
-   Настройка трансферной цены, которая может основываться на различных моделях ценообразования. Далее приводятся некоторые примеры.
    -   **Количество** — сумма, введенная в поле **Ценообразование**, является фактическими затратами на количество или единицу.
    -   **Сумма накладных расходов** — цена/стоимость проводки плюс сумма накладных расходов, которые были введены в поле **Ценообразование**.
    -   **Процент накладных расходов** — трансферная цена представляет собой цену/стоимость на проводку, умноженная на процент накладных расходов, введенных в поле **Ценообразование**.
    -   **Процент от цены продажи** — процент от цены продажи, передаваемый сдающему в аренду юридическому лицу.
    -   **Сумма ниже цены продажи** — сумма, которую удерживает заимствующее юридическое лицо от цен продажи до передачи сдающему в аренду юридическому лицу.
    -   **Процентная маржа** — число, вводимое в поле **Ценообразование**, является процентной маржой, выраженной в виде процента от цены продажи.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Пример 1. Настройка параметров для внутрихолдингового выставления накладных
В этом примере компания USSI является сдающим в аренду юридическим лицом, и ее ресурсы сообщают о времени работы на заимствующее юридическое лицо (FRSI), которое владеет контрактом с конечным клиентом. Часы и расходы, о которых сообщают сотрудники USSI, могут быть включены в накладную по проекту, создаваемую FRSI. Кроме того, есть третий источник проводок, которые могут поступать от сдающего в аренду юридического лица (в данном примере это USSI), когда оно предоставляет услуги общих поставщиков дочерним компаниям (например, FRSI) и передает эти затраты в проекты этих дочерних компаний. Все соответствующие документы накладных и расчеты налогов выполняются в Dynamics 365 for Operations. 

Например, компания FRSI должна быть клиентов в юридическом лице USSI, а компания USSI должна быть поставщиком в юридическом лице FRSI. Затем можно настроить внутрихолдинговые отношения между двумя юридическими лицами. В следующей процедуре показано, как настроить параметры таким образом, чтобы оба юридических лица могли участвовать во внутрихолдинговом выставлении накладных.

1.  Настройте FRSI в качестве клиента в юридическом лице USSI, а USSI — в качестве поставщика в юридическом лице FRSI. Существует три способа выполнения шагов, необходимых для выполнения этой задачи.
    | Шаг | Точка входа                                                                       | описание   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | А    | В USSI щелкните **Расчеты с клиентами** &gt; **Клиенты** &gt; **Все клиенты**. | Создайте новую запись клиента для FRSI и выберите группу клиентов.                                                                                                                                                                                                                           |
    | млрд    | В FRSI щелкните **Расчеты с поставщиками** &gt; **Поставщики** &gt; **Все поставщики**.        | Создайте новую запись поставщика для USSI и выберите группу поставщиков.                                                                                                                                                                                                                               |
    | К    | В FRSI откройте созданную запись поставщика.                            | В области действий на вкладке **Общие** в группе **Настроить** щелкните **Внутрихолдинговый**. На странице **Внутрихолдинговый** на вкладке **Торговые отношения** установите ползунок **Активно** в положение **Да**. В поле **Компания-клиент** выберите запись клиента, созданную на шаге А. |

2.  Щелкните **Управление и учет по проектам** &gt; **Настройка** &gt; **Параметры модуля "Управление и учет по проектам"** и перейдите на вкладку **Внутрихолдинговый**. Способ настройки параметров зависит от того, являетесь ли вы заимствующим юридическим лицом или сдающим в аренду юридическим лицом.
    -   Если вы являетесь заимствующим юридическим лицом, выберите категорию закупок, которая должна использоваться для сопоставления накладных поставщиков, создаваемых автоматически.
    -   Если вы являетесь сдающим в аренду юридическим лицом, для каждого заимствующего юридического лица выберите категорию проекта по умолчанию для каждого типа проводки. Категории проекта используются для настройки налогов, если категория выставленных накладных во внутрихолдинговых проводках существует только в заимствующем юридическом лице. Можно выбрать начисление дохода для внутрихолдинговых проводок. Это начисление выполняется при разноске накладных, а затем реверсируется при разноске внутрихолдинговой накладной.

3.  Щелкните **Управление и учет по проектам** &gt; **Настройка** &gt; **Цены** &gt; **Трансферная цена**.
4.  Выберите валюту, тип проводки и модель трансферной цены. Валюта, используемая в накладной, — это валюта, настроенная в записи клиента для заимствующего юридического лица в сдающем в аренду юридическом лице. Валюта используется для сопоставления записей в таблице трансферных цен.
5.  Щелкните **Главная книга** &gt; **Настройка разноски** &gt; **Внутрихолдинговый учет** и настройте отношение между USSI и FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Пример 2. Создание и разноска внутрихолдингового табеля учета рабочего времени
Сдающее в аренду юридическое лицо USSI должно создать и разнести табель учета рабочего времени для проекта заимствующего юридического лица FRSI. Существует два способа выполнения шагов, необходимых для выполнения этой задачи.

| Шаг | Точка входа                                                                       | описание                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| А    | **Управление и учет по проектам** &gt; **Табели учета рабочего времени** &gt; **Все табели учета рабочего времени** | Создайте новый табель учета рабочего времени. В строке табеля учета рабочего времени в поле **Юридическое лицо** выберите **FRSI**. В поле **Код проекта** выберите проект в FRSI. Введите количество часов для каждого дня недели. |
| B    | Страница **Табель учета рабочего времени**                                                                | После выполнения workflow-процесса разнесите табель учета рабочего времени и запишите код ваучера.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Пример 3. Создание и разноска внутрихолдинговой накладной поставщика
Сдающее в аренду юридическое лицо USSI должно создать и разнести внутрихолдинговую накладную поставщика для проекта заимствующего юридического лица FRSI. Эта накладная поставщика представляет внештатный труд и расходы, которые были выполнены и понесены поставщиками, оплачиваемыми компанией USSI. Существует два способа выполнения шагов, необходимых для выполнения этой задачи.

| Шаг | Точка входа                                                                                      | описание                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| А    | **Расчеты с поставщиками** &gt; **Накладные** &gt; **Открытые накладные поставщиков** &gt; **Новая накладная поставщика** | Создайте новую накладную поставщика и введите услуги, которые были получены от имени проекта FRSI.                                                                                                                                                                                  |
| B    | Страница **Накладная поставщика**                                                                      | Введите строки, представляющие внештатные услуги от имени FRSI. На экспресс-вкладке **Сведения о строке** на вкладке **Проект** для строки накладной в поле **Компания проекта** введите **FRSI**. Введите проект и соответствующую информацию. Затем разнесите накладную поставщика. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Пример 4. Создание и разноска внутрихолдинговой накладной
Сдающее в аренду юридическое лицо USSI должно создать и разнести внутрихолдинговую накладную. Существует два способа выполнения шагов, необходимых для выполнения этой задачи.

| Шаг | Точка входа                                                                                             | описание                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| А    | **Управление и учет по проектам** &gt; **Накладные по проекту** &gt; **Внутрихолдинговая накладная клиента**  | Щелкните **Создать**, чтобы отрыть страницу **Создать внутрихолдинговую накладную**.                                                                                  |
| млрд    | **Управление и учет по проектам** &gt; **Накладные по проекту** &gt; **Внутрихолдинговые накладные клиента** | На странице **Создать внутрихолдинговую накладную** введите юридическое лицо, укажите проводку, которую следует включить, и щелкните **Поиск**. |
| К    | **Управление и учет по проектам** &gt; **Накладные по проекту** &gt; **Внутрихолдинговые накладные клиента** | Выберите проводки, по которым следует выставить накладные, или нажмите кнопку **Выбрать все**, чтобы выставить накладные по всем проводкам в списке, затем нажмите кнопку **OK**.                  |
| D    | Страница **Внутрихолдинговая накладная**                                                                       | Отображается предложение по внутрихолдинговой накладной клиента.                                                                                             |
| E    | Страница **Внутрихолдинговая накладная**                                                                       | Щелкните **Разнести**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Пример 5. Разноска накладной поставщика и выставление накладной для клиента
Когда сдающее в аренду юридическое лицо USSI разносит внутрихолдинговую накладную клиента, создается соответствующая ожидающая накладная поставщика в заимствующем юридическом лице FRSI. После разноски накладной поставщика FRSI также выставляет накладные для клиента проекта по часам, введенным USSI. Существует три способа выполнения шагов, необходимых для выполнения этой задачи.

| Шаг | Точка входа                                                                                        | описание                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| А    | **Расчеты с поставщиками** &gt; **Накладные** &gt; **Накладные поставщиков, ожидающие обработки**                            | Просмотрите накладную, чтобы убедиться, что значения табеля учета рабочего времени включены, а затем разнесите накладную поставщика.                  |
| млрд    | **Управление и учет по проектам** &gt; **Накладные по проекту** &gt; **Предложения по накладным для проекта** | Создайте новую накладную по проекту и убедитесь, что отображаются почасовые проводки, которые были разнесены.            |
| C    | Страница **Накладная по проекту**                                                                       | Выберите накладную по проекту и нажмите кнопку **Просмотр сведений** для просмотра суммы продаж и затрат. Затем разнесите накладную. |





