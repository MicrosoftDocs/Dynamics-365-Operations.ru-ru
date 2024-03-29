---
title: Декларация подоходного налога для Египта
description: В этой статье объясняется, как настраивать и создавать декларации по подоходному налогу для Египта.
author: AdamTrukawka
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.search.scope: ''
ms.openlocfilehash: 83def72f1ff0423d1c2d217847082fa9bf1c3bca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269385"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Декларация подоходного налога для Египта (EG-00005)

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Обзор
В этой статье объясняется, как настроить и создать декларацию по подоходному налогу и формы декларации по подоходному налогу 41 и 11 для юридических лиц в Египте. 

Все египетские организации должны готовить форму 41, которая суммирует все налоги, удерживаемые с местных поставщиков и поставщиков услуг. В дополнение к форме 41 необходимо создать форму 11, чтобы подробно описать удержанный налог с иностранных поставщиков. 

Отчет **Декларация по подоходному налогу** в Dynamics 365 Finance включает в себя следующие отчеты:

- № формы декларации 41
- № формы декларации 11
    
    
## <a name="prerequisites"></a>Необходимые условия
Основной адрес юридического лица должен быть в Египте.
В рабочей области **Управление функциями** следующая функция должна быть включена:

   - **Глобальный подоходный налог**

Дополнительные сведения о включении этих функций см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

1. Перейдите в раздел **Налог** > **Настройка** > **Параметры** > **Параметры главной книги**, затем на вкладке **Подоходный налог** установите для параметра **Включить глобальный подоходный налог** значение **Да**.
2. В рабочей области **Электронная отчетность** импортируйте из репозитория следующий форматы электронной отчетности:

    - Excel декларации подоходного налога (EG)

    > [!NOTE]
    > Вышеприведенный формат основан на **модели налоговой декларации** и использует **сопоставление модели налоговой декларации**. Эта дополнительная конфигурация будет импортирована автоматически.

Дополнительные сведения об импорте конфигураций электронной отчетности см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Загрузка конфигураций электронной отчетности

Реализация форм декларации подоходного налога для Египта основана на конфигурациях электронной отчетности (ER). Дополнительные сведения о возможностях и концепциях настраиваемой отчетности см. в разделе [Электронная отчетность](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

В случае рабочих сред и сред пользовательского приемочного тестирования (UAT) следуйте инструкциям в статье [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Для создания деклараций подоходного налога в египетской организации необходимо загрузить следующие конфигурации:

- Tax declaration model.version.82.xml или более поздняя версия
- Tax declaration model mapping.version.82.133.xml или более поздняя версия
- WHT Declaration Excel (EG).version.82.21 или более поздняя версия

После окончания загрузки конфигураций электронной отчетности из Lifecycle Services (LCS) или глобального репозитория выполните следующие действия.

1. Перейдите в раздел рабочей области **Электронная отчетность** и выберите плитку **Конфигурации отчетности**.
1. На странице **Конфигурации** на панели действий выберите **Exchange > Загрузить из XML-файла**.
1. Отправьте все файлы в том порядке, в котором они указаны в предыдущих пунктах. После загрузки всех конфигураций дерево конфигурации должно присутствовать в Финансах.

## <a name="set-up-application-specific-parameters"></a>Настройка параметров конкретного приложения

Параметр параметров конкретного приложения, позволяет пользователям определять критерии классификации и расчета налоговых проводок в каждой строке сформированного отчета, в зависимости от конфигурации **группы номенклатур подоходного налога** или других критериев, установленных в определении поиска.

Форма "декларирование подоходного налога" 41 включает столбец, в котором проводка по подоходному налогу должна классифицироваться в соответствии с классификацией налогового органа с именем **Тип кода скидки**. Вместо включения этих новых классификаций в качестве новые данные при разноске проводок классификации будут определяться на основе различных уточняющих запросов, введенных в **конфигурации** > **Настройка параметров для конкретного приложения** > **Настройка** в соответствии с требованиями отчетов по подоходному налогу для Египет. 

Следующая конфигурация используется для классификации проводок в отчете декларирование подоходного налога форма 41:

- **DiscountTaxTypeLookup**-> столбец № 18 

Выполните следующие действия, чтобы настроить различные подстановки, используемые для создания декларации по подоходному налогу и соответствующих отчетов по книгам. 

1. В рабочей области **электронной отчетности** выберите **конфигурации** > **Настройка**, чтобы настроить правила, определяющие, как проводки классифицируются в отчете о декларации по подоходному налогу. 
2. Выберите текущую версию и на экспресс-вкладке **Поиск** выберите имя поиска. Например, **DiscountTaxTypeLookup**. Этот поиск определяет список типов скидок, необходимых для налогового органа.
3. На экспресс-вкладке **условия** выберите **Добавить** и в новой строке столбца **результат поиска** выберите соответствующую строку, представляющую классификацию в **столбце 18**.
4. В столбце **группы номенклатур подоходного налога** выберите связанный код, который используется для идентификации классификации. Например, **разрешенная скидка**.  
5. Повторите шаги 3 и 4 для всех доступных поисков.
6. Снова выберите **Добавить** для включения конечной строки записи, а в столбце **Результат поиска** выберите **неприменимо**. 
7. В остальных столбцах выберите **не пусто**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Настройте параметры главной книги

Чтобы создать отчет формы декларации подоходного налога в Microsoft Excel, укажите формат электронной отчетности на странице **Параметры главной книги**.

1. Перейти к **Налог** > **Настройка** > **Параметры главной книги**.
2. На вкладке **подоходный налог** в поле **Сопоставление формата декларации подоходного налога** выберите **Excel декларации подоходного налога (EG)**. Если оставить это поле пустым, стандартный налоговый отчет будет создан в формате SSRS.


![Форма декларации.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Создание форм декларации подоходного налога
Процесс подготовки и отправки формы декларации подоходного налога за конкретный период основан на проводках по подоходному налогу, разнесенных в ходе задания по сопоставлению и разноске платежа. Дополнительные сведения о глобальном подоходном налоге см. в разделе [глобальный подоходный налог](../general-ledger/global-withholding-tax-overview.md).

Выполните следующие шаги для создания налоговой декларации.

1. Переход к **Налог** > **декларации** > **подоходный налог** > **платеж подоходного налога*.
2. Выберите период сопоставления, а затем выберите начальную дату для отчета. 
3. Введите дата проводки и нажмите кнопку **ОК**.
4. В открывшемся диалоговом окне выберите один или несколько типов форм **Форма № 41**, **Форма № 11** или **нет**. Если выбрано значение **нет**, создается стандартный отчет. 
5. Выберите язык. Все отчеты переводятся в **en-us** и **ar-eg**.
6. Введите ветвь и имя банка, в котором будет оплачен налоговый платеж.
7. Выберите тип бизнеса, а затем введите номера чеков и документов. 
8. Введение типа объекта. 
9. Ввод имени лица, зарегистрированного для назначения формы, и нажмите кнопку **ОК**, чтобы подтвердить создание отчета. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
