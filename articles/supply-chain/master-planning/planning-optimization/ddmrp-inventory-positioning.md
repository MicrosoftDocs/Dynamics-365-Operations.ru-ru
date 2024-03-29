---
title: Позиционирование запасов
description: В этой статье приводятся сведения о стратегическом позиционировании запасов, которое включает в себя определение точек рассоединения в цепи поставок, где можно создавать запасы в наличии, чтобы помочь уменьшить значения времени упреждения и компенсировать шоковые воздействия на цепочку поставок.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689547"
---
# <a name="inventory-positioning"></a>Позиционирование запасов

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Стратегическое позиционирование запасов включает определение точек рассоединения в цепи поставок, где можно создавать запасы в наличии. Этот подход в основном используется для того, чтобы помочь в уменьшении значений времени упреждения и компенсации шоковых событий в цепочке поставок. Это позволяет уменьшить "эффект хлыста", так как изменчивость спроса не передается вниз по всей цепочке поставок. (*Эффект хлыста* описывает ситуацию, когда небольшие колебания спроса на уровне розничной торговли могут привести к лавинообразному возрастанию флуктуаций спроса на уровнях оптовой торговли, дистрибутора, производителя и поставщика сырья.)

Позиционирование запасов — это первый шаг при планировании материальных ресурсов по запросу (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Позиционирование запасов для производства

В этом разделе представлен пример, в котором показано, как принимать решения по позиционированию запасов при производстве типичного продукта подушек. У подушек имеется многоуровневая спецификация (BOM), как показано на следующем рисунке.

![Пример многоуровневой спецификации для подушек.](media/ddmrp-bom-example.png "Пример многоуровневой спецификации для подушек")

### <a name="choose-your-decoupling-points"></a>Выбор точек рассоединения

При выборе места размещения точек рассоединения учитывайте все приведенные ниже аспекты каждой номенклатуры в спецификации:

- Внешняя изменчивость
- Широта использования и гибкость запасов
- Защита критических операций
- Время терпимости клиента
- Горизонт видимости заказов на продажу
- Потенциальное время упреждения на рынке

В примере подушек вы можете разместить первую точку рассоединения на номенклатуре *пенопластовые бруски* по следующим причинам:

- Трудно найти поставщиков материалов, используемых для изготовления пенопластовых брусков, а доступность сильно меняется. Таким образом, выполняется критерий *внешняя изменчивость*.
- Пенопластовые бруски можно разрезать на множество различных форм и размеров, чтобы создавать пенопластовые вкладыши для других производимых вами продуктов помимо подушек. Таким образом, выполняется критерий *Широта использования и гибкость запасов*.

Затем можно разместить следующую точку рассоединения на номенклатуре *тканевый набор*, которая является предварительно раскроенной тканью для подушек. Вы можете выбрать эту точку, потому что у вас только один станок для раскройки ткани. Поэтому выполняется критерий *защиты критических операций*.

Наконец, можно поместить последнюю точку рассоединения в номенклатуру "готовые подушки". Эту точку можно выбрать, поскольку у вас очень малое *время терпимости клиента* в продажах, поскольку *горизонт видимости заказов на продажу* довольно короткий. Таким образом, необходимо обеспечить наличие запасов в наличии для соответствия входящим заказам. Можно также задать более высокую цену, сохранив такое короткое время упреждения, на что указывает критерий *потенциальное рыночное время упреждения*.

На основе этого анализа на следующем рисунке показано, как выглядят спецификация подушек. Желтые символы запасов выделяют точки рассоединения.

![Пример спецификации с выделенными точками рассоединения.](media/ddmrp-bom-decoupling-example.png "Пример спецификации с выделенными точками рассоединения")

### <a name="calculate-your-decoupled-lead-time"></a>Расчет несвязанного времени упреждения

В этом разделе показано, как рассчитать новые значения времени упреждения после введения точек рассоединения.

На следующем рисунке для примера подушек, который был запущен в предыдущем разделе, значения времени упреждения отображаются в серых прямоугольниках в верхнем левом углу каждого компонента спецификации. Рамки, которые имеют красный контур, обозначают номенклатуры, которые определяют суммарное время упреждения (сумма наиболее продолжительных времен упреждения на каждом уровне спецификации). Это время упреждения составляет 21 день при запуске с нуля.

![Пример спецификации со значениями времени упреждения.](media/ddmrp-bom-lead-times-example.png "Пример спецификации со значениями времени упреждения")

Однако при применении ранее выбранных точек рассоединения эти рассоединенные номенклатуры всегда будут храниться на складе. Поэтому они будут иметь время упреждения, равное 0 (нулю). Новое время упреждения для подушек теперь всего пять дней: два дня для приобретения ниток и три дня для производства подушек. Это время упреждения называется *несвязанное время упреждения*.

![Пример независимого времени упреждения.](media/ddmrp-bom-decoupled-lead-time-example.png "Пример независимого времени упреждения")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Стратегическое позиционирование запасов в модели розничной торговли

Так как у розничных продавцов в запасах имеются только готовые продукты, спецификации не являются проблемой. Однако, розничные торговцы все равно могут использовать DDMRP, настроив стратегическое позиционирование запасов и уровни буфера на основе местоположений хранения в сети распределения.

На следующем рисунке показан пример компании, в которой имеется центр распределения в Сиэтле и магазины в Бостоне, Атланте и Портленде.

![Точки рассоединения в зависимости от местоположения в модели розничной торговли.](media/ddmrp-retail-decoupl-points-example.png "Точки рассоединения в зависимости от местоположения в модели розничной торговли")

Можно решить, что время перемещения, требуемое для перемещения одеял между центром дистрибуции и магазинами, нарушает ваше *время терпимости клиента*, так как клиенты ожидают, что одеяло будет в наличии при посещении магазина. В этом случае вы настроите точку рассоединения для номенклатуры "одеяло" для каждого из трех магазинов. Каждый магазин будет иметь различные уровни буфера, основанные на времени упреждения, шаблонах спроса и т. д.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Реализация позиционирования запасов в Dynamics 365 Supply Chain Management

В этом разделе описывается, как реализовать стратегию позиционирования запасов в Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Настройка групп покрытия номенклатуры, которые создают точки рассоединения

Номенклатуры становятся точками рассоединения, когда они принадлежат к группе покрытия, которая настроена со значением параметра **Код покрытия**, равным *Точка рассоединения*. Таким образом, первым шагом в процессе настройки DDMRP является определение групп покрытия, которые необходимо реализовать для стратегии DDMRP, а затем их создание с помощью следующих шагов.

1. Выберите **Сводное планирование \> Настройка \> Покрытие \> Группы покрытия**.
1. На панели операций выберите **Создать** для создания группы покрытия.
1. Введите информацию, определяющую группу покрытия, и выберите календарь, который будет использоваться.
1. На вкладке **Общие** задайте в поле **Код покрытия** значение *Точка рассоединения*. Эта настройка приведет к тому, что все номенклатуры, принадлежащие данной группе покрытия, будут рассматриваться как точки рассоединения для DDMRP. При этом также включаются все параметры DDMRP для данной группы, как описано далее в этой процедуре.
1. На вкладке **Прочее** в разделе **Параметры DDMRP** задайте следующие поля:

    - **Коэффициент времени упреждения** — укажите коэффициент (в виде десятичного значения от 0 до 1), чтобы контролировать влияние, которое должно иметь время упреждения, когда для номенклатур в данной группе покрытия рассчитываются минимальный и максимальный уровни запасов. В общем случае чем дольше время упреждения номенклатуры, тем ниже должен быть его коэффициент времени упреждения. Меньший коэффициент времени упреждения может привести к появлению более низких минимальных и максимальных уровней запасов, в результате чего они вызывают меньшие по объему и более частые заказы. Методология DDMRP рекомендует значение между 0,20 и 0,40 для номенклатур, которые имеют продолжительное время упреждения, между 0,41 и 0,60 для номенклатур со средним временем упреждения и между 0,61 и 1,00 для номенклатур, которые имеют короткое время упреждения. Дополнительную информацию см. в разделе [Профиль и уровни буфера](ddmrp-buffer-profile-and-levels.md).
    - **Коэффициент изменчивости** — укажите коэффициент (в виде десятичного значения от 0 до 1), чтобы контролировать влияние, которое должна иметь изменчивость спроса, когда для номенклатур в данной группе покрытия рассчитываются минимальный уровень запасов. В общем случае чем больше изменчивость спроса на номенклатуру, тем выше ее коэффициент изменчивости. Более высокий коэффициент изменчивости создает более высокий уровень минимальных запасов. Методология DDMRP рекомендует значение между 0,00 и 0,40 для номенклатур, которые имеют низкую изменчивость, между 0,41 и 0,60 для номенклатур со средней изменчивостью и между 0,61 и 1,00 для номенклатур, которые имеют высокую изменчивость. Дополнительную информацию см. в разделе [Профиль и уровни буфера](ddmrp-buffer-profile-and-levels.md).
    - **Период минимума, максимума и точки заказа** — укажите частоту расчета значений буфера (*Ежедневно* или *Еженедельно*).

1. На вкладке **Прочее** в разделе **Среднесуточное потребление** задайте следующие поля:

    - **Среднесуточное потребление на основании** — выберите, на каких периодах времени должны быть основаны расчеты среднесуточного потребления (ADU). Выберите одно из следующих значений:

        - *В прошлом* — учитывать только потребление в прошлом за количество дней, указанное в поле **Прошлый период (дни)**. ADU вычисляется как общий спрос на номенклатуру в течение расчетного периода (в единицах складского учета), деленный на количество дней в расчетном периоде.
        - *Вперед* — учитывать только прогнозируемое потребление в будущем (включая прогнозы) за количество дней, указанное в поле **Будущий период (дни)**. ADU вычисляется как общий спрос на номенклатуру в течение расчетного периода (в единицах складского учета), деленный на количество дней в расчетном периоде. 
        - *Смешанный* — учитывать как прошлое, так и будущее потребление. Применяется все параметры для поля **Прошлый период (дни)**, поля **Будущий период (дни)** и параметры смешивания. 

            *Смешанное ADU* = (\[*Вес прошлого* × *Прошлое ADU*\] + \[*Вес будущего* × *Будущее ADU*\]) ÷ (*Вес прошлого* + *Вес будущего*)

    - **Прошлый период (дни)** — введите число прошедших дней (до текущей даты включительно), которые система должна учитывать при расчете среднесуточного потребления номенклатур в данной группе покрытия. Этот параметр применяется только в том случае, если в поле **Среднесуточное потребление на основании** задано значение *Прошлое* или *Смешанное*.
    - **Будущий период (дни)** — введите число дней в будущем (от текущей даты до указанного дня), которые система должна учитывать при расчете среднесуточного потребления номенклатур в данной группе покрытия. Этот параметр применяется только в том случае, если в поле **Среднесуточное потребление на основании** задано значение *Вперед* или *Смешанное*.
    - **Относительный вес прошлого периода для смешанного среднесуточного потребления** — введите вес (в процентах), который будет применяться к прошлому периоду при расчете среднесуточного потребления. Этот параметр применяется только в том случае, если в поле **Среднесуточное потребление на основании** задано значение *Смешанное*.
    - **Относительный вес будущего периода для смешанного среднесуточного потребления** — введите вес (в процентах), который будет применяться к будущему периоду при расчете среднесуточного потребления. Этот параметр применяется только в том случае, если в поле **Среднесуточное потребление на основании** задано значение *Смешанное*.

1. Во всех других вкладках и полях введите подробные настройки, используемые для расчета потребностей в номенклатуре, которая связана с данной группой покрытия.

### <a name="set-an-item-as-a-decoupling-point"></a>Задание номенклатуры в качестве точки рассоединения

Чтобы задать номенклатуру как точку рассоединения, выполните следующие действия.

1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
1. Найдите и выберите выпущенную номенклатуру, которую необходимо настроить для DDMRP.
1. В области действий на вкладке **План** выберите **Покрытие номенклатуры**.
1. На странице **Покрытие номенклатуры** могут быть уже перечислены несколько записей покрытия номенклатуры, каждая из которых применяется к разным сочетаниям аналитик хранения и продукта. Можно выбрать существующую запись покрытия номенклатуры, которая применяется к измерениям, в которых необходимо создать точку рассоединения. Или можно выбрать **Создать** в области действий, чтобы создать новую запись покрытия номенклатуры.
1. Запись покрытия номенклатуры настраивается как обычно. Необходимо, как минимум, указать сайт и склад, на котором будет применяться точка рассоединения.
1. Пока соответствующая запись остается выбранной, выберите вкладку **Общие**.
1. Установите флажок **Использовать определенные параметры**.
1. Задайте в поле **Группа покрытия** группу покрытия, настроенную для создания точек рассоединения (как описано в предыдущем разделе).
1. Теперь номенклатура настроена в качестве точки рассоединения. Обычно при использовании DDMRP здесь также настраиваются параметры, которые влияют на размеры буфера и количество дозаказа. Однако эту настройку можно выполнить позднее. Дополнительные сведения об этих настройках см. в разделе [Настройка буферов для номенклатуры точки рассоединения](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Чтобы запланировать номенклатуры, которые не являются точками рассоединения, выполните те же шаги, которые были выполнены при использовании стандартного планирования потребностей в материалах (MRP).
