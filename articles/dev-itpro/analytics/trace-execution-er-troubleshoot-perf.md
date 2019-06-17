<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="ru-RU">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Трассировка выполнения формата электронной отчетности для устранения проблем с производительностью</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этой теме приводятся сведения об использовании функции трассировки производительности в электронной отчетности (ER) для устранения проблем с производительностью.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Трассировка выполнения форматов электронной отчетности для устранения проблем с производительностью</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В процессе разработки конфигураций электронной отчетности (ER) для создания электронных документов определяется метод, используемый для извлечения данных Microsoft Dynamics 365 for Finance and Operations и ввода их в создаваемые выводные данные.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Функция трассировки производительности электронной отчетности позволяет значительно сократить время и затраты, связанные со сбором сведений о выполнении формата ER, и использовать их для устранения неполадок, связанных с производительностью.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этом учебнике приводятся инструкции по выполнению трассировки производительности для выполняемых форматов электронной отчетности в Finance and Operations, а также по использованию сведений из этих трассировок для повышения производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Необходимые условия</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Чтобы завершить примеры из этого учебника, необходимы следующие возможности доступа:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Доступ к Finance and Operations для одной из следующих ролей:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Разработчик электронной отчетности</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Консультант по функциональным возможностям электронной отчетности</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Системный администратор</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Доступ к экземпляру служб Regulatory Configuration Service (RCS), который был настроен для того же клиента, что и Finance and Operations, для одной из следующих ролей:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Разработчик электронной отчетности</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Консультант по функциональным возможностям электронной отчетности</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Системный администратор</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Кроме того, необходимо загрузить следующие файлы и сохранить их локально.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Хранилище файлов</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Содержание</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Модель трассировки производительности.версия.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Пример конфигурации модели данных электронной отчетности<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Метаданные трассировки производительности.версия.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Пример конфигурации метаданных электронной отчетности<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Сопоставление трассировки производительности.версия.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Пример конфигурации сопоставления модели электронной отчетности<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Формат трассировки производительности.версия.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Пример конфигурации формата электронной отчетности<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Настройка параметров ER</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Каждая трассировка производительности электронной отчетности, созданная в Finance and Operations, сохраняется в виде вложения в записи журнала выполнения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Для управления этими вложениями используется структура управления документооборотом (DM) Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Необходимо заранее настроить параметры электронной отчетности, чтобы указать тип документа DM, который должен использоваться для вложения трассировок производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В Finance and Operations в рабочей области <bpt id="p1">**</bpt>Электронная отчетность<ept id="p1">**</ept> выберите <bpt id="p2">**</bpt>Параметры электронной отчетности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Затем на странице <bpt id="p1">**</bpt>Параметры электронной отчетности<ept id="p1">**</ept> на вкладке <bpt id="p2">**</bpt>Вложения<ept id="p2">**</ept> в поле <bpt id="p3">**</bpt>Прочие<ept id="p3">**</ept> выберите тип документа DM, который будет использоваться для трассировок производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Страница параметров электронной отчетности в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Чтобы тип документа DM был доступным в поле подстановки <bpt id="p1">**</bpt>Прочие<ept id="p1">**</ept>, он должен быть настроен следующим образом на странице <bpt id="p2">**</bpt>Типы документов<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Администрирование организации <ph id="ph1">\&gt;</ph> Управление документами <ph id="ph2">\&gt;</ph> Типы документов<ept id="p3">**</ept>):</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Класс:<ept id="p1">**</ept> Вложить файл</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Группа:<ept id="p1">**</ept> Файл</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Страница типов документов в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выбранный тип документа должен быть доступен в каждой компании в текущем экземпляре Finance and Operations, поскольку вложения DM являются специфическими для компании.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Настройка параметров RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Трассировки производительности электронной отчетности, создаваемые в Finance and Operations, будет импортированы в службу RCS для анализа с помощью конструктора форматов электронной отчетности и конструктора сопоставления электронной отчетности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Так как трассировки производительности электронной отчетности хранятся в виде вложений в запись журнала выполнения, которая относится к формату электронной отчетности, необходимо заранее настроить параметры службы RCS, чтобы указать тип документа DM, который должен использоваться для присоединения трассировок производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В экземпляре службы RCS, который был подготовлен для компании, в рабочей области <bpt id="p1">**</bpt>Электронная отчетность<ept id="p1">**</ept> выберите <bpt id="p2">**</bpt>Параметры электронной отчетности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Затем на странице <bpt id="p1">**</bpt>Параметры электронной отчетности<ept id="p1">**</ept> на вкладке <bpt id="p2">**</bpt>Вложения<ept id="p2">**</ept> в поле <bpt id="p3">**</bpt>Прочие<ept id="p3">**</ept> выберите тип документа DM, который будет использоваться для трассировок производительности.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Страница параметров электронной отчетности в службе RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Чтобы тип документа DM был доступным в поле подстановки <bpt id="p1">**</bpt>Прочие<ept id="p1">**</ept>, он должен быть настроен следующим образом на странице <bpt id="p2">**</bpt>Типы документов<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Администрирование организации <ph id="ph1">\&gt;</ph> Управление документами <ph id="ph2">\&gt;</ph> Типы документов<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Класс:<ept id="p1">**</ept> Вложить файл</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Группа:<ept id="p1">**</ept> Файл</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Разработка решения электронной отчетности</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Предположим, что вы приступили к разработке нового решения ER для создания нового отчета, представляющего проводки по поставщику.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В настоящее время на странице <bpt id="p1">**</bpt>Проводки по поставщику<ept id="p1">**</ept> можно найти проводки для выбранного поставщика (перейдите по пути <bpt id="p2">**</bpt>Расчеты с поставщиками <ph id="ph1">\&gt;</ph> Поставщики <ph id="ph2">\&gt;</ph> Все поставщики<ept id="p2">**</ept>, выберите поставщика, затем на панели операций на вкладке <bpt id="p3">**</bpt>Поставщик<ept id="p3">**</ept> в группе <bpt id="p4">**</bpt>Проводки<ept id="p4">**</ept> выберите <bpt id="p5">**</bpt>Проводки<ept id="p5">**</ept>).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Однако необходимо иметь одновременно все проводки поставщика в одном электронном документе в формате XML.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это решение будет состоять из нескольких конфигураций ER, которые содержат требуемую модель данных, метаданные, сопоставление моделей и компоненты формата.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните вход в экземпляр службы RCS, который был подготовлен для вашей компании.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">В этом учебнике вам предстоит создать и изменить конфигурации для демонстрационной компании <bpt id="p1">**</bpt>Litware, Inc<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поэтому убедитесь, что данный поставщик конфигурации был добавлен в RCS и выбран как активный.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Инструкции см. в процедуре <bpt id="p1">[</bpt>Создание поставщиков конфигураций и пометка их как активных<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">В рабочей области <bpt id="p1">**</bpt>Электронная отчетность<ept id="p1">**</ept> выберите плитку <bpt id="p2">**</bpt>Конфигурации отчетности<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> импортируйте конфигурации электронной отчетности, загруженные в качестве необходимого компонента в RCS, в следующем порядке: модель данных, метаданные, сопоставление моделей, формат.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Для каждой конфигурации выполните следующие действия.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">На панели действий выберите пункт <bpt id="p1">**</bpt>Обмен <ph id="ph1">\&gt;</ph> Загрузить из XML-файла<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выберите <bpt id="p1">**</bpt>Обзор<ept id="p1">**</ept>, чтобы выбрать соответствующий файл для требуемой конфигурации ER в формате XML.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>ОК<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Страница конфигураций в службе RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Запуск решения электронной отчетности для трассировки выполнения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Предположим, что вы завершили разработку первой версии решения ER.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Теперь необходимо проверить его в своем экземпляре Finance and Operations и проанализировать производительность выполнения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Импорт конфигурации ER из службы RCS в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Войдите в свой экземпляр Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этом учебнике будут импортированы конфигурации из экземпляра RCS (где вы разрабатываете компоненты электронной отчетности) в экземпляр Finance and Operations (где они проверяются и затем используются).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поэтому необходимо убедиться, что все необходимые артефакты подготовлены.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Инструкции см. в процедуре <bpt id="p1">[</bpt>Импорт конфигураций электронной отчетности из служб Regulatory Configuration Service (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните следующие действия, чтобы импортировать конфигурации из RCS в Finance and Operations:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В рабочей области <bpt id="p1">**</bpt>Электронная отчетность<ept id="p1">**</ept> на плитке поставщика конфигурации <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> выберите <bpt id="p3">**</bpt>Репозитории<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">На странице <bpt id="p1">**</bpt>Репозиторий конфигураций<ept id="p1">**</ept> выберите репозиторий типа <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept>, затем выберите <bpt id="p3">**</bpt>Открыть<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На экспресс-вкладке <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> выберите конфигурацию <bpt id="p2">**</bpt>Формат трассировки производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">На экспресс-вкладке <bpt id="p1">**</bpt>Версии<ept id="p1">**</ept> выберите версию <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> выбранной конфигурации, затем выберите <bpt id="p3">**</bpt>Импорт<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Страница репозитория конфигураций в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Соответствующие версии модели данных и конфигурации сопоставления моделей автоматически импортируются как необходимые условия для импортированной конфигурации формата ER.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Включение трассировки производительности электронной отчетности</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">В Finance and Operations перейдите к <bpt id="p1">**</bpt>Администрирование организации <ph id="ph1">\&gt;</ph> Электронная отчетность <ph id="ph2">\&gt;</ph> Конфигурации<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">На странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> в области действий на вкладке <bpt id="p2">**</bpt>Конфигурации<ept id="p2">**</ept> в группе <bpt id="p3">**</bpt>Дополнительные параметры<ept id="p3">**</ept> выберите <bpt id="p4">**</bpt>Параметры пользователя<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В диалоговом окне <bpt id="p1">**</bpt>Параметры пользователя<ept id="p1">**</ept> в разделе <bpt id="p2">**</bpt>Трассировка выполнения<ept id="p2">**</ept> выполните следующие действия:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В поле <bpt id="p1">**</bpt>Формат трассировки выполнения<ept id="p1">**</ept> выберите <bpt id="p2">**</bpt>Отладка формата трассировки<ept id="p2">**</ept>, чтобы начать сбор сведений о выполнении формата ER.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если выбрано это значение, трассировка производительности будет собирать сведения о времени, затраченном на выполнение следующих действий:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполнение каждого источника данных в сопоставлении модели, которое вызывается для извлечения данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обработка каждого элемента формата для ввода данных в создаваемые выходные данные</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поле <bpt id="p1">**</bpt>Формат трассировки выполнения<ept id="p1">**</ept> используется для указания формата созданного отслеживания производительности, в котором хранятся сведения о выполнении, для формата ER и элементов сопоставления.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выбрав <bpt id="p1">**</bpt>Отладка формата трассировки<ept id="p1">**</ept> в качестве значения, можно проанализировать содержимое трассировки в конструкторе операций электронной отчетности и просмотреть формат ER или элементы сопоставления, которые упоминаются в трассировке.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Задайте для следующих параметров значение <bpt id="p1">**</bpt>Да<ept id="p1">**</ept>, чтобы собрать определенные подробные сведения о выполнении сопоставления модели ER и компонентах формата ER:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Сбор статистики запросов<ept id="p1">**</ept> — когда этот параметр включен, трассировка производительности соберет следующую информацию:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Число вызовов базы данных, выполненных источниками данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Количество дублированных обращений к базе данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Подробные сведения об инструкциях SQL, которые использовались для выполнения вызовов базы данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Отслеживания доступа кэширования<ept id="p1">**</ept> — если этот параметр включен, трассировка производительности будет собирать сведения об использовании кэша сопоставлений модели ER.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Трассировка доступа к данным<ept id="p1">**</ept> — когда этот параметр включен, трассировка производительности будет собирать сведения о количестве обращений к базе данных для запущенных источников данных типа списка записей.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Перечисление списка трассировки<ept id="p1">**</ept> — когда этот параметр включен, трассировка производительности будет собирать сведения о количестве записей, запрошенных из источников данных типа списка записей.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Параметры в диалоговом окне <bpt id="p1">**</bpt>Параметры пользователя<ept id="p1">**</ept> относятся только к этому пользователю и текущей компании.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Диалоговое окно "Параметры пользователя" в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Выполнение формата электронной отчетности</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">В Finance and Operations выберите компанию <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Перейдите в раздел <bpt id="p1">**</bpt>Управление организацией <ph id="ph1">\&gt;</ph> Электронная отчетность <ph id="ph2">\&gt;</ph> Конфигурации<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">На странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> в дереве конфигураций выберите пункт <bpt id="p2">**</bpt>Формат трассировки производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">В области действий выберите <bpt id="p1">**</bpt>Выполнить<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что создаваемый файл содержит информацию о 265 транзакциях для шести поставщиков.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Просмотр трассировки выполнения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Экспорт созданной трассировки из Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Трассировки производительности не связаны с исходным форматом ER и могут быть сериализованы во внешний ZIP-файл.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">В Finance and Operations перейдите к пункту <bpt id="p1">**</bpt>Администрирование организации <ph id="ph1">\&gt;</ph> Электронная отчетность <ph id="ph2">\&gt;</ph> Журналы отладки конфигураций<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На странице <bpt id="p1">**</bpt>Журналы выполнения электронной отчетности<ept id="p1">**</ept> в левой области в поле <bpt id="p2">**</bpt>Имя конфигурации<ept id="p2">**</ept> выберите <bpt id="p3">**</bpt>Формат трассировки производительности<ept id="p3">**</ept> для поиска записей журнала, созданных при выполнении конфигурации <bpt id="p4">**</bpt>Формат трассировки производительности<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Выберите кнопку <bpt id="p1">**</bpt>Вложения<ept id="p1">**</ept> (символ скрепки) в верхнем правом углу страницы или нажмите <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Кнопка вложений на странице журналов выполнения электронной отчетности в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На странице <bpt id="p1">**</bpt>Вложения для журналов выполнения прикрепления электронной отчетности<ept id="p1">**</ept> на панели операций выберите <bpt id="p2">**</bpt>Открыть<ept id="p2">**</ept>, чтобы получить трассировку производительности в виде ZIP-файла и сохранить ее локально.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Вложения для страницы журналов выполнения электронной отчетности в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Создаваемая трассировка имеет ссылку на исходный отчет ER с помощью уникального идентификатора отчета только в формате <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Нумерация версий этого формата не учитывается.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что связь между трассировкой производительности, созданной для выполненного формата ER, и сопоставлением модели ER основана на используемом корневом дескрипторе и общей модели данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Нумерация версий этого формата и сопоставление модели не учитывается.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Настройка флага <bpt id="p1">**</bpt>По умолчанию для сопоставления модели<ept id="p1">**</ept> для сопоставления модели также не учитывается.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Импорт созданной трассировки в службу RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">В службе RCS в рабочей области <bpt id="p1">**</bpt>Электронная отчетность<ept id="p1">**</ept> выберите плитку <bpt id="p2">**</bpt>Конфигурации отчетности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> в дереве конфигураций разверните элемент <bpt id="p2">**</bpt>Модели трассировки производительности<ept id="p2">**</ept> и выберите пункт <bpt id="p3">**</bpt>Формат трассировки производительности<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">В области действий выберите <bpt id="p1">**</bpt>Конструктор<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">На странице <bpt id="p1">**</bpt>Конструктор форматов<ept id="p1">**</ept> в области действий выберите <bpt id="p2">**</bpt>Трассировка производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В диалоговом окне <bpt id="p1">**</bpt>Параметры результатов трассировки производительности<ept id="p1">**</ept> выберите <bpt id="p2">**</bpt>Импорт трассировки производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выберите <bpt id="p1">**</bpt>Обзор<ept id="p1">**</ept>, чтобы выбрать ZIP-файл, экспортированный из Finance and Operations ранее.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>ОК<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Диалоговое окно "Параметры результатов трассировки производительности" в RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Используйте трассировку производительности для анализа в RCS — выполнение формата</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В RCS на странице <bpt id="p1">**</bpt>Конструктор формата<ept id="p1">**</ept> выберите <bpt id="p2">**</bpt>Развернуть/свернуть<ept id="p2">**</ept>, чтобы развернуть содержимое всех элементов формата.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что для некоторых элементов текущего формата отображаются дополнительные сведения:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Фактическое время, потраченное на ввод данных в генерируемые выходные данные с использованием элемента формата</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">То же время, выраженное в процентах от общего времени, затраченного на формирование всех выходных данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Страница конструктора форматов в службе RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Закройте страницу <bpt id="p1">**</bpt>Конструктор форматов<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Используйте трассировку производительности для анализа в RCS — сопоставление модели</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">В службе RCS на странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> в дереве конфигураций выберите пункт <bpt id="p2">**</bpt>Сопоставление трассировки производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">В области действий выберите <bpt id="p1">**</bpt>Конструктор<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Выберите <bpt id="p1">**</bpt>Конструктор<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">На странице <bpt id="p1">**</bpt>Конструктор сопоставления модели<ept id="p1">**</ept> в области действий выберите <bpt id="p2">**</bpt>Трассировка производительности<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выберите ранее импортированную трассировку.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>ОК<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что новые сведения становятся доступны для некоторых элементов источника данных в текущем сопоставлении модели:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Фактическое время, потраченное на получение данных с использованием источника данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">То же время, выраженное в процентах от общего времени, затраченного на выполнение всего сопоставления модели</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что электронная отчетность информирует о том, что текущее сопоставление модели дублирует запросы к базе данных, когда выполняется источник данных VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Такое дублирование происходит из-за того, что список проводок поставщика вызывается два раза для каждой итерации записи поставщика:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Один вызов выполняется для ввода подробных сведений о каждой проводке в модели данных на основе настроенных привязок.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Один вызов создается для ввода рассчитанного количества проводок по поставщику в модели данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Сообщение о дубликатах запросов базы данных на странице конструктора сопоставления модели в RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> указывает на то, что таблица VendTrans была вызвана 530 раз, чтобы вернуть запись из этой таблицы в источник данных VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> указывает на то, что источник данных VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum был вызван 530 раз, чтобы вернуть запись из этого источника данных и ввести сведения из нее в модель данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Рекомендуется использовать кэширование для источника данных VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum, чтобы уменьшить число вызовов, которые были сделаны для получения сведений о 265 транзакциях и помочь улучшить производительность сопоставления модели.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Также может быть полезно уменьшить количество вызовов, выполненных в источнике данных LedgerTransTypeList.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот источник данных используется для связи каждого значения перечисления <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> с его меткой.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Используя этот источник данных, можно найти соответствующую метку и ввести ее в модель данных для каждой проводки поставщика.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Текущее число вызовов этого источника данных (9 027) довольно большое для 265 проводок.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Страница конструктора сопоставлений моделей в RCS, в которой показаны 9 027 вызовов в источнике данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Улучшите сопоставление модели на основе информации из трассировки выполнения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Изменение логики сопоставления модели</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните следующие действия, чтобы использовать кэширование, чтобы предотвратить повторные обращения к базе данных:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В службе RCS на странице <bpt id="p1">**</bpt>Конструктор сопоставления модели<ept id="p1">**</ept> в области <bpt id="p2">**</bpt>Источники данных<ept id="p2">**</ept> выберите элемент <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выберите <bpt id="p1">**</bpt>Кэш<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Разверните элемент <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept>, раскройте список отношений "один ко многим" для источника данных VendTable (элемент <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Отношения<ept id="p2">**</ept>) и выберите пункт <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Выберите <bpt id="p1">**</bpt>Кэш<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Настройка кэширования, помогающая предотвратить дублированные вызовы</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните следующие действия, чтобы перенести источник данных LedgerTransTypeList в область источника данных VendTable:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В области <bpt id="p1">**</bpt>Типы источников данных<ept id="p1">**</ept> раскройте элемент <bpt id="p2">**</bpt>Функции<ept id="p2">**</ept> и выберите элемент <bpt id="p3">**</bpt>Вычисляемое поле<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В области <bpt id="p1">**</bpt>Источники данных<ept id="p1">**</ept> выберите элемент <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Выберите <bpt id="p1">**</bpt>Добавить<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">В поле <bpt id="p1">**</bpt>Имя<ept id="p1">**</ept> введите <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Выберите <bpt id="p1">**</bpt>Изменить формулу<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">В поле <bpt id="p1">**</bpt>Формула<ept id="p1">**</ept> введите <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>Сохранить<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Закройте страницу <bpt id="p1">**</bpt>Редактор формул<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Щелкните <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните следующие действия, чтобы выполнить кэширование поля <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Выберите элемент <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Выберите <bpt id="p1">**</bpt>Кэш<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выберите элемент <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Выберите <bpt id="p1">**</bpt>Кэш<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Настройка кэширования для поля $TransType</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните следующие действия для изменения поля <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> таким образом, чтобы оно начинало использовать кэшированное поле <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept>:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На панели <bpt id="p1">**</bpt>Источники данных<ept id="p1">**</ept> разверните элемент <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>, разверните элемент <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Отношения<ept id="p3">**</ept>, разверните элемент <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> и выберите элемент <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Выберите <bpt id="p1">**</bpt>Правка<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Выберите <bpt id="p1">**</bpt>Изменить формулу<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В поле <bpt id="p1">**</bpt>Формула<ept id="p1">**</ept> найдите следующее выражение:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">В поле <bpt id="p1">**</bpt>Формула<ept id="p1">**</ept> введите следующее выражение:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>Сохранить<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Закройте страницу <bpt id="p1">**</bpt>Редактор формул<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>ОК<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Нажмите <bpt id="p1">**</bpt>Сохранить<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Закройте страницу <bpt id="p1">**</bpt>Конструктор сопоставления модели<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Закройте страницу <bpt id="p1">**</bpt>Сопоставления модели<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Выполните измененную версию сопоставления модели ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В RCS на странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> на экспресс-вкладке <bpt id="p2">**</bpt>Версии<ept id="p2">**</ept> выберите версию <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> конфигурации <bpt id="p4">**</bpt>Сопоставление трассировки производительности<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Выберите <bpt id="p1">**</bpt>Изменить статус<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Выберите <bpt id="p1">**</bpt>Завершено<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Импорт измененной конфигурации сопоставления модели ER из RCS в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Повторите шаги из раздела <bpt id="p1">[</bpt>Импорт конфигурации ER из службы RCS в Finance and Operations<ept id="p1">](#import-configuration)</ept> выше в этой теме, чтобы импортировать версию 1.2 конфигурации <bpt id="p2">**</bpt>Сопоставление трассировки производительности<ept id="p2">**</ept> в Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Запуск измененного решения электронной отчетности для трассировки выполнения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Выполнение формата электронной отчетности</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Повторите шаги в разделе <bpt id="p1">[</bpt>Выполнение формата электронной отчетности<ept id="p1">](#run-format)</ept> ранее в этой теме, чтобы создать новую трассировку производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Просмотр трассировки выполнения</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Экспорт созданной трассировки из Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Повторите шаги из раздела <bpt id="p1">[</bpt>Экспорт созданной трассировки из Finance and Operations<ept id="p1">](#export-trace)</ept> ранее в этой теме, чтобы сохранить новую трассировку производительности локально.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Импорт созданной трассировки в службу RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Повторите шаги из раздела <bpt id="p1">[</bpt>Импорт созданной трассировки в службу RCS<ept id="p1">](#import-trace)</ept> ранее в этой теме для импорта новой трассировки производительности в RCS.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Используйте трассировку производительности для анализа в RCS — сопоставление модели</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Повторите шаги из раздела <bpt id="p1">[</bpt>Используйте трассировку производительности для анализа в RCS — сопоставление модели<ept id="p1">](#use-trace)</ept>, приведенного ранее в этой теме, для анализа последней трассировки производительности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что изменения, внесенные в сопоставление модели, исключают повторяющиеся запросы к базе данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Также уменьшилось число обращений к таблицам базы данных и источникам данных для данного сопоставления модели.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поэтому производительность всего решения ER улучшилась.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Сведения отслеживания для источника данных VendTable на странице конструктора сопоставления модели в службе RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В данных трассировки значение <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> для источника данных VendTable указывает, что этот источник данных вызывался 12 раз.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> указывает, что шесть вызовов были преобразованы в вызовы таблицы VendTable базы данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> указывает, что записи, которые были извлечены из базы данных, были кэшированы, и шесть других вызовов были обработаны с использованием кэша.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что количество вызовов источника данных LedgerTransTypeList уменьшилось с 9 027 до 240.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Сведения отслеживания для источника данных LedgerTransTypeList на странице конструктора сопоставления модели в службе RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Просмотр трассировки выполнения в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В дополнение к RCS, некоторые версии Finance and Operations могут предоставлять возможности для конструктора структуры электронной отчетности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Эти версии Finance and Operations имеют параметр <bpt id="p1">**</bpt>Включить режим конструктора<ept id="p1">**</ept>, который может быть включен.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот параметр можно найти на вкладке <bpt id="p1">**</bpt>Общие<ept id="p1">**</ept> страницы <bpt id="p2">**</bpt>Параметры электронной отчетности<ept id="p2">**</ept>, которую можно открыть из рабочей области <bpt id="p3">**</bpt>Электронная отчетность<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Параметр "Включить режим конструктора" на странице "Параметры электронной отчетности" в Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">При использовании одной из этих версий Finance and Operations можно анализировать подробные сведения о созданных трассировках производительности непосредственно в Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Нет необходимости экспортировать их из Finance and Operations и импортировать в RCS.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Просмотр трассировки выполнения с помощью внешних средств</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Настройка параметров пользователя</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">В Finance and Operations перейдите к <bpt id="p1">**</bpt>Администрирование организации <ph id="ph1">\&gt;</ph> Электронная отчетность <ph id="ph2">\&gt;</ph> Конфигурации<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">На странице <bpt id="p1">**</bpt>Конфигурации<ept id="p1">**</ept> в области действий на вкладке <bpt id="p2">**</bpt>Конфигурации<ept id="p2">**</ept> в группе <bpt id="p3">**</bpt>Дополнительные параметры<ept id="p3">**</ept> выберите <bpt id="p4">**</bpt>Параметры пользователя<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В диалоговом окне <bpt id="p1">**</bpt>Параметры пользователя<ept id="p1">**</ept> в разделе <bpt id="p2">**</bpt>Трассировка выполнения<ept id="p2">**</ept> в поле <bpt id="p3">**</bpt>Формат трассировки выполнения<ept id="p3">**</ept> выберите <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Выполнение формата электронной отчетности</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Повторите шаги в разделе <bpt id="p1">[</bpt>Выполнение формата электронной отчетности<ept id="p1">](#run-format)</ept> ранее в этой теме, чтобы создать новую трассировку производительности.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что веб-браузер предлагает ZIP-файл для загрузки.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот файл содержит трассировку производительности в формате PerfView.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Затем можно воспользоваться средством анализа производительности PerfView, чтобы проанализировать сведения о выполнении формата электронной отчетности.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>