---
title: Подключение периферийных устройств к POS
description: В этой статье описываются способы подключения периферийных устройств к Retail POS.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897116"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Подключение периферийных устройств к POS

[!include [banner](includes/banner.md)]

В этой статье описываются способы подключения периферийных устройств к Retail POS.

> [!NOTE]
> Подробные инструкции по установке см. в разделе [Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md) и [Настройка, установка и активация Modern POS (MPOS)](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Ключевые компоненты

Некоторые компоненты используются для определения отношений между магазином, регистрами POS или каналами в магазине и периферийными устройствами, которые используют эти регистры или каналы для обработки проводок. В этом разделе описывается каждый компонент и объясняется, как он должен использоваться в развертывании магазина.

### <a name="pos-registers"></a>POS-регистраторы

Навигация: щелкните **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Регистры**.

Регистр POS — это объект, используемый для определения характеристик конкретного экземпляра POS. Эти характеристики включают профиль оборудования или настройку для периферийных устройств, которые будут использоваться в регистре, магазин, с которым сопоставлен этот регистр, и визуальной взаимодействие с пользователем, который входит в этот регистр.

### <a name="devices"></a>Оборудование

Навигация: щелкните **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Устройства**.

Устройство — это объект, представляющий физический экземпляр устройства, которое сопоставлено с регистром POS. При создании устройства оно сопоставляется с регистром POS. Объект устройства отслеживает сведения об активации регистра POS, типе используемого клиента и пакете приложения, развернутом на определенном устройстве. Устройства могут быть двух типов: **Retail modern POS** (MPOS) или **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS представляет собой клиентское приложение POS, установленное в ОС Windows 8.1 или более поздней версии операционной системы на базе ПК. Если тип приложения **Retail modern POS** сопоставлен с устройством, пакет загрузки может быть указан для определенного устройства. Пакет загрузки можно настроить для включения различных версий пакета установки. Возможность развертывать различные пакеты обеспечивает гибкость в случаях, когда различные регистры POS могут требовать различные интеграции. MPOS развертывается вместе со встроенной станцией оборудования.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS — это POS на основе браузера. Поскольку Cloud POS выполняется в браузере, он не требует Windows 8.1 или более поздней версии операционной системы на базе ПК. Если тип предложения **Retail Cloud POS** сопоставляется с определенным устройством в Headquarters, это устройство можно использовать в браузере, не загружая и не устанавливая пакет. Cloud POS требует наличия станции оборудования для использования оборудования помимо сканирования штрих-кодов на основе считывателя кредитных карт с клавиатурой.

### <a name="hardware-profile"></a>Профиль оборудования

Перейдите **Розничная торговля и коммерция \> Настройка канала \> Настройка POS \> Профили POS \> Профили оборудования**.

Профиль оборудования определяет оборудование, подключенное к ККМ POS через интегрированную или общую станцию оборудования. Профиль оборудования также используется для указания параметров процессора платежей, которые должны использоваться при взаимодействии с пакетом средств разработки программного обеспечения (SDK) платежей. Пакет SDK платежей развертывается в рамках станции оборудования.

### <a name="hardware-station"></a>Станция оборудования

Навигация: перейдите к пункту **Retail и Commerce \> Каналы \> Магазины \> Все магазины**, выберите магазин, а затем перейдите на экспресс-вкладку **Станции оборудования**.

Станция оборудования — это экземпляр бизнес-логики, который управляет периферийными устройствами POS. Станция оборудования устанавливается автоматически вместе с MPOS. Кроме того, станцию оборудования можно установить как отдельный компонент, а затем открыть из MPOS или Cloud POS с помощью веб-службы. Станцию оборудования необходимо определить на уровне канала.

## <a name="scenarios"></a>Сценарии

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS с подключенными периферийными устройствами

[![Традиционная фиксированная POS.](./media/traditional-300x279.png)](./media/traditional.png)

Для подключения MPOS к периферийным устройствам POS в сценарии традиционной фиксированной POS сначала перейдите в регистр и назначьте ему профиль оборудования. Регистры POS находятся в разделе **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Регистры**. 

После назначения профиля оборудования синхронизация меняется на базу данных канала с помощью графика распределения **Регистры**. Графики распределения находятся в разделе **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**. 

Затем настройте выделенную станцию оборудования в канале. Выберите **Retail и Commerce \> Каналы \> Магазины \> Все магазины** и выберите магазин. 

Затем на экспресс-вкладке **Станции оборудования** выберите **Добавить** для добавления станции оборудования. Выберите **Выделенная** в качестве типа аппаратной станции, затем введите описание. Поле **Профиль оборудования** можно оставить пустым, так как профиль оборудования, используемый в этом сценарии, берется из POS-терминала. Затем синхронизируйте изменения с каналом, используя график распределения **Конфигурация канала**. Графики распределения находятся в разделе **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**. 

Наконец, в MPOS используйте операцию **Выбор станции оборудования**, чтобы выбрать станцию оборудования, совпадающую со значением, ранее введенным для описания, и настройте станцию оборудования как **Активная**. 

> [!NOTE]
> - Для некоторых изменений профиля оборудования, например денежных ящиков, требуется открыть новую смену после синхронизации изменений с каналом.
> - Cloud POS необходимо использовать автономную станцию оборудования для связи с периферийными устройствами.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS или Cloud POS с автономной станцией оборудования

[![Общие периферийные устройства.](./media/shared-300x254.png)](./media/shared.png)

В этом сценарии автономная станция оборудования совместно используется клиентами MPOS и Cloud POS. Для этого сценария требуется создать общую станцию оборудования и указать пакет загрузки, порт и профиль оборудования, который использует станция оборудования. Можно определить новую станцию оборудования, выбрав экспресс-вкладку **Станции оборудования** в отдельном канале (**Retail и Commerce \> Каналы \> Магазины \> Все магазины**) и добавив новую станцию оборудования типа **Общая**. 

Далее предоставьте описание, которое поможет кассиру определить станцию оборудования. В поле **Имя узла** введите URL-адрес хоста-компьютера в следующем формате: `https://<MachineName:Port>/HardwareStation`. (Замените **&lt;MachineName:Port&gt;** фактическим именем компьютера станции оборудования.) Для изолированной станции оборудования необходимо также указать код терминала электронных платежей (EFT). Это значение определяет терминал EFT, подключаемый к станции оборудования, когда соединитель платежей обменивается данными с поставщиком платежных услуг. 

Далее на компьютере, на котором установлена станция оборудования, перейдите к каналу в Headquarters и выберите станцию оборудования. Затем выберите **Загрузить**, чтобы загрузить установщик станции оборудования, и установите станцию оборудования. Дополнительные сведения о том, как установить станцию оборудования, см. в разделе [Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md). 

Затем в MPOS или Cloud POS используйте операцию **Выбор станции оборудования**, чтобы выбрать станцию оборудования, установленную ранее. Выберите **Соединение**, чтобы установить безопасную связь между POS и станцией оборудования. Этот шаг необходимо выполнить один раз для каждой комбинации POS и станции оборудования. 

После соединения станции оборудования та же операция используется для активации станции оборудования во время и использования. В этом сценарии профиль оборудования должен быть назначен общей станции оборудования, а не самой ККМ. Если по какой-либо причине станции оборудования не назначен профиль оборудования напрямую, то будет использоваться профиль оборудования, назначенный ККМ.

## <a name="client-maintenance"></a>Обслуживание клиентов

### <a name="registers"></a>Регистры

Управление регистрами POS осуществляется в основном с помощью самих регистров, а также с помощью профилей, назначенных регистрам. Управление атрибутами, относящимися к отдельным регистрам, осуществляется на уровне регистра. Эти атрибуты включают хранилище, в котором используется регистр, номер регистра, описание и код терминала EFT, характерный для самого регистра.

### <a name="pos-profiles"></a>Профили POS

Профили POS находятся в разделе **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Профили POS**. Полезно управлять многими аспектами регистра с помощью профилей, поскольку профили могут совместно использоваться многими регистрами. Профили могут быть сопоставлены с отдельным регистром или, если профиль является действительным для всего магазина, с магазином. В следующих разделах описываются профили POS и то, как они используются.

#### <a name="offline-profile"></a>Профиль автономной работы

Автономный профиль настраивается на уровне магазина. Он используется для указания параметров загрузки для проводок, которые выполняются в регистре POS, когда регистр не подключен к базе данных канала.

#### <a name="functionality-profile"></a>Профиль функциональности

Профиль функциональности настраивается на уровне магазина. Он используется для указания параметров на уровне магазина для функций, которые могут выполняться в POS. Профиль функциональности управляет следующими возможностями. Эти возможности организованы по экспресс-вкладке.

- Экспресс-вкладке **Общее**:

    - Международная организация по стандартизации (ISO).
    - Создание клиента в автономном режиме.
    - Профиль чека по электронной почте.
    - Центральная проверка подлинности при подключении персонала.

- Экспресс-вкладка **Функции**:

    - Управление входом в систему и расширенным входом в систему.
    - Аспекты POS, связанные с финансами и валютой, например возможность вводить цены с клавиатуры и указание того, требуются ли десятичные знаки для дополнительной валюты.
    - Включение регистрации времени с помощью POS.
    - Способ отображения продуктов и платежей в POS и чеках.
    - Управление закрытием дня.
    - Параметры сохранения проводок базы данных канала.
    - Способ поиска и создания клиентов в POS.
    - Способ расчета скидок.

- Экспресс-вкладка **Сумма**:

    - Максимальные и минимальные допустимые цены.
    - Применение и расчет скидок.

- Экспресс-вкладка **Инфокоды**:

    - Все аспекты управления инфокодами в POS. Более подробные сведения см. в разделе [Информационные коды и группы информационных кодов](info-codes-retail.md).

- Экспресс-вкладка **Нумерация чеков**:

    - Указание масок нумерации чеков, которые могут включать сегменты для номера магазина, номера терминала, константы и то, будут ли печататься продажи, возвраты, заказы на продажу и предложения в отдельной последовательности или они все будут следовать одной и той же последовательности.

#### <a name="receipt-profiles"></a>Профили чеков

Профили чеков назначаются принтерам в профиле оборудования. Они используются для указания типов чеков, которые печатаются на определенном принтере. Профили включают параметры для форматов чеков и параметры, которые определяют, будут ли чеки печататься всегда или кассир будет получать запрос на указание того, следует ли печатать чек. Различные принтеры также могут использовать различные профили чеков. Например, принтер 1 является стандартным принтером термальных чеков, и поэтому имеет меньший формат чеков. Однако принтер 2 является принтером полноразмерных чеков, который используется для печати только чеков по заказам клиентов, требующих больше места. Дополнительные сведения см. в разделе [Настройка профиля чеков](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Профили оборудования

Профили оборудования были описаны в рамках настройки клиента ранее в этой статье. Профили оборудования назначаются прямо POS-терминалу или общей станции оборудования и используются для указания типов устройств, используемых в конкретном POS-терминале или в станции оборудования. Профили оборудования также используются для указания параметров EFT, которые используются для связи с SDK платежей.

#### <a name="visual-profiles"></a>Визуальные профили

Визуальные профили используются для указания темы для конкретной ККМ и назначаются на уровне ККМ. Профили включают параметры типа приложения, которое используется (MPOS или Cloud POS), цвета выделения и темы, схемы шрифтов, фона страницы входа и фона POS. Дополнительные сведения см. в разделе [Создание визуальных профилей POS-терминалов](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Настраиваемые поля

Пользовательские поля можно создавать для добавления полей, которые не поставляются вместе с POS. Дополнительные сведения об использовании пользовательских полей см. в разделе [Работа с пользовательскими полями (запись блога)](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Текст

Строки по умолчанию можно переопределить в POS с помощью записей текста языка. Чтобы переопределить строку в POS, добавьте новую строку текста языка. Затем укажите код, строку по умолчанию, которую следует переопределить, и текст, который должен отображаться в POS вместо строки по умолчанию.

### <a name="channel-reports-configuration"></a>Конфигурация отчетов канала

Настройка отчетов, доступных в канале розничной торговли, выполняется на странице **Конфигурация отчетов канала**. Можно создать новые отчеты, предоставив XML-определение отчета и назначив отчет определенной группе разрешений в POS.

### <a name="devices"></a>Устройства

Устройства описаны ранее в этой статье. Они используются для управления активацией определенного регистра POS. Устройства также используются для указания приложения, используемого для определенного регистра, и пакета установки, который должен использоваться для установки клиента MPOS. Ниже перечислены состояния активации устройства:

- **Ожидание** — устройство готово к активации.
- **Активировано** — устройство было активировано.
- **Деактивировано** — устройство деактивировано в Headquarters или с помощью POS.
- **Отключено** — устройство отключено.

Дополнительные сведения, связанные с активацией, включают работника, который изменил статус активации устройства, отметку времени активации и то, была ли проверена конфигурация устройства.

### <a name="client-data-synchronization"></a>Синхронизация данных клиента

Все изменения в клиенте POS за исключением изменений в статусе активации устройства необходимо синхронизировать с базой данных канала, чтобы они вступили в силу. Чтобы синхронизировать изменения с базой данных канала, перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения и выполните требуемый график распределения**. В случае изменений клиента необходимо выполнить графики распределения **Регистры** и **Конфигурация канала**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка и установка Retail Hardware Station](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
