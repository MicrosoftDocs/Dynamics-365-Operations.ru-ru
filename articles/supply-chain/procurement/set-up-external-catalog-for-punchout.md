<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-external-catalog-for-punchout.md" target-language="ru-RU">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-external-catalog-for-punchout.474d96.39baa331120d765543c3cf662ce53d2bcfe404ab.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>39baa331120d765543c3cf662ce53d2bcfe404ab</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\procurement\set-up-external-catalog-for-punchout.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройка внешнего каталога для внешних eProcurement</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the use of an  external catalog or punchout catalog to collect quote information from a vendor and add it to a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом разделе описывается использование внешнего каталога или каталога PunchOut для сбора информации о ценовых предложениях от поставщика и добавления этой информации в заявку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройка внешнего каталога для внешних eProcurement</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>By using the external catalog, you can ensure that the product and price information that you subsequently process in Dynamics 365 for Finance and Operations July 2017 is accurate and up to date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Использование внешнего каталога позволяет гарантировать, что информация о продуктах и ценах, которую вы впоследствии обрабатываете в Dynamics 365 for Finance and Operations от июля 2017 г., будет точной и актуальной.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The requisition can then be approved and converted to a purchase order and an order can be placed at the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">После этого заявку можно будет утвердить и преобразовать в заказ на покупку, и разместить заказ у поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the external catalog is set up and an employee is preparing a requisition, there will be an option to redirect to an external site, the external catalog, and return the shopping basket that was created at the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если внешний каталог настроен, когда сотрудник составляет заявку, у него будет возможность перейти на внешний сайт, к внешнему каталогу, и вернуться в систему с корзиной для покупок, созданной на внешнем сайте.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This communication is based on the cXML protocol and it has to be set up between the systems of the buying and the selling organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Этот обмен данными основан на протоколе cXML, и его необходимо настроить между системами организации-покупателя и организации-продавца.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To set up the communication, your vendor has to provide pieces of information for you to use in the configuraiton of the external catalog such as Identity, domain of the buyers company, for example, "DUNS" and "DUNS number", credentials, and the URL to reach the vendors catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для настройки обмена данными поставщик должен предоставить вам информацию, которую вы будете использовать для конфигурирования внешнего каталога, такую как удостоверение, домен компании-покупателя, например, "DUNS" и "номер DUNS", учетные данные, а также URL-адрес для доступа к каталогу поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Setting up an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройка внешнего каталога</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The external catalog should enable an employee who enters a purchase requisition to be redirected to an external site to select products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Внешний каталог должен давать сотруднику, занимающемуся вводом заявки на покупку, возможность перейти на внешний сайт для выбора продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The products that the employee selects from the external catalog are returned to Dynamics 365 for Finance and Operations with up-to-date price information and from here, they can be added to the purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Продукты, которые сотрудник выбирает из внешнего каталога, возвращаются в Dynamics 365 for Finance and Operations с актуальной ценовой информацией, откуда их можно добавить в заявку на покупку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The intention is not to enable employees to place an order on the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Речь не идет о том, чтоб дать сотрудникам возможность размещать заказы на внешнем сайте.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>When setting up the external catalog, you need to make sure that the purpose of the site that can be accessed by the external catalog is to collect quote information and not to place a real order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">При настройке внешнего каталога, необходимо убедиться, что назначение сайта, доступ к которому осуществляется через внешний каталог, — это сбор ценовой информации, а не размещение реального заказа.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To set up an external vendor catalog, complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для настройки внешнего каталога поставщика выполните следующие задачи:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set up a procurement category hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройка иерархии категорий закупаемой продукции.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Set up policies for procurement category hierarchies<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Более подробные сведения см. в разделе <bpt id="p1">[</bpt>Настройка политик для иерархий категорий приобретаемой продукции<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Register the vendor in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Зарегистрируйте поставщика в Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Before you can set up configurations to access an external vendor’s catalog, you must set up the vendor and the vendor contact in Microsoft Dynamics 365.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Перед началом настройки доступа ко внешнему каталогу поставщика необходимо настроить поставщика и его контактное лицо в Microsoft Dynamics 365.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The external catalog’s vendor must also be added to the selected procurement category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Поставщика внешнего каталога также необходимо добавить в выбранную категорию закупаемой продукции.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For more information about registering vendors in Microsoft Dynamics 365, see <bpt id="p1">[</bpt>Manage vendor collaboration users<ept id="p1">](manage-vendor-collaboration-users.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные сведения о регистрации поставщиков в Microsoft Dynamics 365 см. в разделе <bpt id="p1">[</bpt>Управление пользователями совместной работы с поставщиками<ept id="p1">](manage-vendor-collaboration-users.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For information about how to assign vendors to a procurement category, see <bpt id="p1">[</bpt>Approve vendors for specific procurement categories<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">О том, как назначить поставщиков категории закупаемой продукции, см. в разделе <bpt id="p1">[</bpt>Утверждение поставщиков для определенных категорий закупаемой продукции<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the units of measure and the currency that the vendor uses are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Убедитесь, что настроены единицы измерения и валюта, которую использует поставщик.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For information about how to create a unit of measure, see <bpt id="p1">[</bpt>Manage units of measure<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">О том, как создать единицу измерения, см. в разделе <bpt id="p1">[</bpt>Управление единицами измерения<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Configure the external vendor catalog by using the requirements for your vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройте внешний каталог поставщика, используя требования к сайту внешнего каталога этого поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more details about this task, see <bpt id="p1">[</bpt>Configure the external vendor catalog<ept id="p1">](#configure-the-external-vendor-catalog)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные сведения об этой задаче см. в разделе <bpt id="p1">[</bpt>Настройка внешнего каталога поставщика<ept id="p1">](#configure-the-external-vendor-catalog)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Test the vendor’s external catalog configurations to verify that the settings are valid and that you can access the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Протестируйте конфигурацию внешнего каталога поставщика, чтобы убедиться в правильности настроек и возможности доступа к внешнему каталогу поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Use the <bpt id="p1">**</bpt>Validate settings<ept id="p1">**</ept> action to validate the request setup message that you’ve defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Используйте действие <bpt id="p1">**</bpt>Проверить параметры<ept id="p1">**</ept> для проверки определенного вами сообщения запроса настройки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This message should cause the vendors external catalog site to be opened in a browser window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это сообщение должно привести к открытию сайта внешнего каталога поставщика в окне браузера.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>During validation, you can’t order items and services from the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Во время проверки заказать номенклатуры и услуги у поставщика нельзя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>To order items and services, you must access the vendor’s catalog from a purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для заказа номенклатур и услуг необходимо осуществить доступ к каталога поставщика через заявку на покупку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Activate the external catalog by using the <bpt id="p1">**</bpt>Activate catalog<ept id="p1">**</ept> button on the <bpt id="p2">**</bpt>External catalogs<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Активируйте внешний каталог с помощью кнопки <bpt id="p1">**</bpt>Активировать каталог<ept id="p1">**</ept> на странице <bpt id="p2">**</bpt>Внешние каталоги<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The external catalog must be activated before employees can use it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Внешний каталог необходимо активировать, прежде чем сотрудники смогут им пользоваться.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can inactivate the external catalog at any time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вы можете в любой момент деактивировать внешний каталог.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Configure the external vendor catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройка внешнего каталога поставщика</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This section gives more details about task 4 in the preceding section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом разделе содержатся дополнительные сведения о задаче 4 из предыдущего раздела.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Enter a name and description for the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Введите название и описание для внешнего каталога поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The name that you enter will appear on the cart that represents the external catalog that is shown to employees who creates a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Введенное название будет отображаться на представляющей внешний каталог корзине, которую будут видеть сотрудники при создании заявки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Employees can click on the cart to open the catalog on the vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сотрудник может щелкнуть на корзине, чтобы открыть каталог на сайте внешнего каталога поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Add an image by using the<bpt id="p1"> **</bpt>External catalog image<ept id="p1">**</ept> action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Добавьте изображение с помощью действия<bpt id="p1"> **</bpt>Изображение внешнего каталога<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The image will appear on the cart that represents the external catalog that is shown to employees who create a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это изображение будет отображаться на представляющей внешний каталог корзине, которую будут видеть сотрудники при создании заявки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Note that the image’s width and height must be equal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обратите внимание, что ширина и высота изображения должны быть равны.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Otherwise the image won’t be displayed correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В противном случае изображение будет отображаться некорректно.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Select whether the vendor’s external catalog website should appear in the same browser window as the one where the employee has created the requisition, or if it should open in a new window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Выберите, должен ли веб-сайт внешнего каталога поставщика открываться в том же окне браузера, в котором сотрудник создал заявку, или в новом окне.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select the vendor for the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Выберите поставщика для каталога.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the <bpt id="p1">**</bpt>Legal entities<ept id="p1">**</ept> list, there is a row for each legal entity where the vendor is set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В списке <bpt id="p1">**</bpt>Юридические лица<ept id="p1">**</ept> имеется строка для каждого юридического лица, где настроен поставщик.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To allow users to request products directly from the vendor’s catalog in some legal entities but not others, you can use the <bpt id="p1">**</bpt>Prevent access<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Allow access<ept id="p2">**</ept> button for each legal entity where you want the catalog to be or not to be available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Чтобы разрешить пользователям запрашивать продукты непосредственно из каталога поставщика только в некоторых юридических лицах, можно использовать кнопку <bpt id="p1">**</bpt>Запретить доступ<ept id="p1">**</ept> или <bpt id="p2">**</bpt>Разрешить доступ<ept id="p2">**</ept> для каждого юридического лица, чтобы сделать каталог недоступным или доступным.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the <bpt id="p1">**</bpt>Default expiration (Days)<ept id="p1">**</ept> field, enter the number of days that a quotation received from the external catalog is valid and can be used to purchase from the external vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В поле <bpt id="p1">**</bpt>Истечение срока действия по умолчанию (дней)<ept id="p1">**</ept> введите количество дней, в течение которых ценовое предложение, полученное из внешнего каталога, будет действительным и может использоваться для приобретения продуктов у внешнего поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>When a quotation is created and retrieved from the vendor’s external catalog site, the quotation is valid as of the current system date and remains valid for the number of days that you enter in this field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">При создании и получении предложения с сайта внешнего каталога поставщика предложение действительно с момента текущей системной даты и остается действительным в течение количества дней, введенного в этом поле.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Click the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> button to start mapping the procurement categories to the external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Нажмите кнопку <bpt id="p1">**</bpt>Добавить<ept id="p1">**</ept>, чтобы начать сопоставление категорий закупаемой продукции с внешним каталогом.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source> Then, in the Category name list, select a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Затем в списке "Имя категории" выберите категорию.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The list of categories is a superset of procurement categories that the vendor has been mapped to in all the legal entities that are set up for the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Список категорий представляет собой надмножество категорий закупаемой продукции, которым поставщик сопоставлен во всех юридических лицах, настроенных для этого поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Procurement policies are used to allow or restrict access to categories for the buying legal entity or receiving operating unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Политики закупок используются для предоставления или ограничения доступа к категориям для юридического-лица покупателя или операционной единицы-получателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source> Punchout to an external catalog requires that access be allowed to at least one of the procurement categories that is mapped to the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Для перехода сотрудника к внешнему каталогу требуется, чтобы доступ был разрешен хотя бы к одной из категорий закупаемой продукции, сопоставленных каталогу.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Set up the cXML setup request message that will be sent to the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Настройте сообщение запроса настройки cXML, которое будет отправлено поставщику.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The automatically generated message format is the minimal template that is required in order to start a session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Автоматически сгенерированный формат сообщения — это минимальный шаблон, необходимый для запуска сеанса.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Fill in values for the tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Заполните значения для тегов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>At any time, you can reload the system-generated message template by clicking <bpt id="p1">**</bpt>Restore message format<ept id="p1">**</ept>.<ph id="ph1"> </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вы можете в любой момент перезагрузить созданный системой шаблон сообщения, щелкнув <bpt id="p1">**</bpt>Восстановить формат сообщения<ept id="p1">**</ept>.<ph id="ph1"> </ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Note that if you restore the message format, the current message will be replaced by the automatically generated message format, which has empty tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обратите внимание, что если восстановить формат сообщения, текущее сообщение будет заменено автоматически сгенерированным форматом сообщения с пустыми тегами.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>cXML setup message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сообщение настройки cXML</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Below you can find a description of the tags that are included in the template:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ниже приведено описание тегов, входящих в шаблон:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Поле</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">описание</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Домен компании-покупателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Удостоверение компании-покупателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The domain of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Домен компании-поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The identity of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Удостоверение компании-поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Домен компании-покупателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Удостоверение компании-покупателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The shared secret for the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Общий секрет для компании-покупателя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>&lt; Request deploymentMode=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Request deploymentMode=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The test or production deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Тестовая или рабочая среда.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The URL of the vendor’s punchout endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL-адрес конечной точки с каталогом поставщика.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Extrinsic elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Внешние элементы</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>An extrinsic element is additional information, such as a user name that is based on a user that punches out. The extrinsic element is set when the punchout occurs and it can be sent in the request setup message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Внешний элемент — это дополнительная информация, например имя пользователя, зависящее от пользователя, осуществляющего переход к каталогу. Внешний элемент задается в момент перехода и может быть отправлен в сообщении запроса настройки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Your vendor could have a requirement for receiving an extrinsic element in the setup request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">У поставщика может быть требование, состоящее в получении внешнего элемента в запросе настройки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In that case, you should add the extrinsic element to the list of extrinsic elements in the <bpt id="p1">**</bpt>Message format<ept id="p1">**</ept> section of the <bpt id="p2">**</bpt>External catalog<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом случае следует добавить внешний элемент в список внешних элементов в разделе <bpt id="p1">**</bpt>Формат сообщения<ept id="p1">**</ept> страницы <bpt id="p2">**</bpt>Внешний каталог<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Specify a name for the extrinsic element that the vendor can recognize and map it to a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Укажите имя для внешнего элемента, которое сможет распознать поставщик, и сопоставьте его значению.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The options for values are: User name, User email, or Random value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Возможные варианты значения — имя пользователя, адрес электронной почты пользователя или случайное значение.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For more information about the cXML protocol, see the <bpt id="p1">[</bpt>cXML.org website<ept id="p1">](http://cxml.org/)</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Дополнительные сведения о протоколе cXML см. на <bpt id="p1">[</bpt>веб-сайте cXML.org<ept id="p1">](http://cxml.org/)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Post back message</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Обратное сообщение</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The post back message is the message that is received from the vendor when the user checks out from the external site and returns to Finance and Operations.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Обратное сообщение — это сообщение, получаемое от поставщика, когда пользователь заканчивает работу на внешнем сайте и возвращается в Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Post back messages can’t be configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обратные сообщения не настраиваются.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The messages are based on the cXML protocol definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эти сообщения основаны на определении протокола cXML.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source> Here is the information that can be part of the post back message that is received on a requisition line:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Ниже приведена информация, которая может входить в состав обратного сообщения, полученного по строке заявки:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Message received from vendor</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сообщение, полученное от поставщика</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Copied to requisition line in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Копируется в строку заявки в Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>&lt; ItemIn quantity=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn quantity=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Количество</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>External item ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Внешний код номенклатуры</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Валютное</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Unit price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Цена за ед. изм.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Product name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Имя продукта</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Included in item description; Product name if ShortName is not specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Входит в описание номенклатуры; название продукта, если краткое название (ShortName) не указано.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ед. изм.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Входит в описание номенклатуры</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Входит в описание номенклатуры</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Delete an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Удаление внешнего каталога</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Delete an external catalog with the Delete action on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Удалить внешний каталог можно с помощью действия "Удалить" на странице.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If a product from the external vendor catalog has been requested, the external vendor catalog cannot be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если был запрошен какой-либо продукт из внешнего каталога поставщика, внешний каталог поставщика удалить нельзя.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Instead, the status of the external vendor catalog is set to inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вместо этого внешнему каталогу поставщика присваивается неактивный статус.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If you want to remove access to the external vendor’s catalog site, but not delete it, change the external catalog status to Inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если вы хотите прекратить доступ к сайту внешнего каталога поставщика, но не удалить его, измените статус внешнего каталога на "Неактивно".</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>