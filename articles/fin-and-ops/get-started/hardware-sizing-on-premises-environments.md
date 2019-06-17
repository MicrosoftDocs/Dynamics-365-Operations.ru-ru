<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="hardware-sizing-on-premises-environments.md" target-language="ru-RU">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>hardware-sizing-on-premises-environments.e242d0.4832a056a99e0f7521e022982b7db7b16d7064a3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4832a056a99e0f7521e022982b7db7b16d7064a3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\fin-and-ops\get-started\hardware-sizing-on-premises-environments.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Требования к определению параметров оборудования для локальных сред</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic lists the hardware sizing requirements for an on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Требования к определению параметров оборудования для локальных сред</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Требования к определению параметров оборудования для локальных сред</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the <bpt id="p1">[</bpt>System requirements<ept id="p1">](system-requirements.md)</ept> and <bpt id="p2">[</bpt>Setup and deployment instructions<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept> to gain a solid understanding off the underlying infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Прежде чем начать процесс определения параметров оборудования и инфраструктуры для локальной среды, ознакомьтесь с разделами <bpt id="p1">[</bpt>Требования к системе<ept id="p1">](system-requirements.md)</ept> и <bpt id="p2">[</bpt>Инструкции по настройке и развертыванию<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept>, чтобы получить четкое представление о базовой инфраструктуре.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Pay close attention to the system setup best practices for optimum performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обратите особое внимание на рекомендации по настройке системы для достижения оптимальной производительности.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">После просмотра документации можно начать процесс оценки объема проводок и одновременных пользователей и определения параметров среды на основании средней пропускной способности ядра.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Factors that affect sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Факторы, влияющие на определение параметров</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>All the factors shown in the following illustration contribute to sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Все факторы, которые показаны на следующем рисунке, влияют на определение параметров.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The more detailed information that is collected, the more precisely you can determine sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Чем более подробны собранные сведения, тем можно более точно определить параметры.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Hardware sizing, without supporting data, is likely to be inaccurate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определение параметров оборудования без вспомогательных данных, скорее всего, будет неточным.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The absolute minimum requirement for necessary data is the peak transaction line load per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Абсолютное минимальное требование к необходимым данным является максимальная нагрузка строки проводки в час.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Hardware sizing for on-premises environments<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Определение параметров оборудования для локальных сред<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если смотреть слева направо, первым и важнейшим фактором, необходимым для точного определения параметров, является профиль проводки или характеристика проводки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It's important to always find the peak transactional volume per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Важно всегда находить пиковый объем проводок в час.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If there are multiple peak periods, then these periods need to be accurately defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">При наличии нескольких пиковых периодов эти периоды необходимо точно определить.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">После того, как вы будете иметь представление о нагрузке, которая влияет на инфраструктуру, вам необходимо также разобраться со следующими факторами:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Transactions<ept id="p1">**</ept> – Typically transactions have certain peaks throughout the day/week.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Проводки<ept id="p1">**</ept> — обычно проводки имеют определенные пики в течение дня или недели.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This mostly depends on the transaction type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это главным образом зависит от типа проводки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Записи времени и расходов обычно отображают пики один раз в неделю, в то время как записи заказа на продаже часто поступают в пакетном режиме путем интеграции или отправки в течение дня.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Number of concurrent users<ept id="p1">**</ept> – The number of concurrent users is the second most important sizing factor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Число одновременных пользователей<ept id="p1">**</ept> — число одновременных пользователей является вторым самым важным фактором определения параметров.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вы не можете надежно получить оценки определения паромеров на основе числа одновременных пользователей, если это единственные доступные данные. Выполните оценку приблизительного числа, а затем вернитесь в ним при наличии дополнительных данных.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>An accurate concurrent user definition means that:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Точное определение одновременных пользователей означает, что:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Named users are not concurrent users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Именованные пользователи не являются одновременными пользователями.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Concurrent users are always a subset of named users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Одновременные пользователи всегда представляют собой подмножество именованных пользователей.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Peak workload defines the maximum concurrency for sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пиковая рабочая нагрузка определяет максимальный параллелизм для определения параметров.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Criteria for concurrent users is that the user meets all the following criteria:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Критерии для одновременных пользователей — пользователь отвечает следующим критериям:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Logged on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Выполнил вход в систему.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Working transactions/inquiries at the time of counting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Работает с проводками/запросами во время расчета.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Not an idle session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сеанс не в режиме ожидания.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Data composition<ept id="p1">**</ept> – This is mostly about how your system will be set up and configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Состав данных<ept id="p1">**</ept> — это, главным образом, способ настройки и конфигурации системы.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Например, количество имеющихся юридических лиц, количество номенклатур, количество уровней спецификации и уровень сложности параметров безопасности.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Каждый из этих факторов может иметь незначительное влияние на производительность, поэтому эти факторы можно нейтрализовать, делая правильный выбор в отношении инфраструктуры.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Extensions<ept id="p1">**</ept> – Customizations can be simple or complex.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Расширения<ept id="p1">**</ept> — настройки могут быть простыми или сложными.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Количество настроек и характер сложности и использования оказывают различное влияние на размер инфраструктуры.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В случае сложных настроек рекомендуется провести оценку производительности, чтобы убедиться, что они не только проверены на эффективность, но и помогают понять требования инфраструктуры.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This is even more critical when the extensions are not coded according to best practices for performance and scalability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это еще более важно, когда расширения не кодируются согласно рекомендациям по производительности и масштабируемости.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Reporting and analytics<ept id="p1">**</ept> – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Отчеты и аналитика<ept id="p1">**</ept> — обычно эти факторы включают выполнение больших запросов к различным базам данных в системах баз данных Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Понимание и уменьшение частоты выполнения ресурсоемких отчетов поможет понять их влияние.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Third-party solutions<ept id="p1">**</ept> – These solutions, like ISVs, have the same implications and recommendations as extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Решения третьих сторон<ept id="p1">**</ept> — эти решения, такие как поставщики программного обеспечения, имеют тот же смысл и рекомендации, что и расширения.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Sizing your Finance and Operations environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определение параметров среды Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для понимания требований к параметрам необходимо знать пиковый объем проводок, которые необходимо обработать.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Большинство вспомогательных систем, например Management Reporter или SSRS, являются менее критически важными.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>As a result, this document focuses mostly on AOS and SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В результате этот документ посвящен, главным образом, AOS и SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В общем, случае уровни подсчета расширяются и должны быть настроены в формате N+1, т.е. если вы оцениваете, что нужно три сервера AOS, добавьте четвертый сервер AOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The database tier should be set up in an Always On highly-available setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">На уровне баз данных следует выполнить настройку высокой доступности Always On.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>SQL Server (OLTP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server (OLTP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определение параметров</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>3K to 15K transaction lines per hour per core on DB server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 000–15 000 строк проводок в час на ядро на сервере базы данных.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Стандартный коэффициент ядра AOS-к-SQL 3:1 для основного сервера SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Additional cores are required based on the chosen high availability configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные ядра требуются на основании выбранной конфигурации высокой доступности.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Processing database-heavy operations may regress this to 2:1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обработка ресурсоемких операций базы данных может понизить это до 2:1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The following factors influence variations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Следующие факторы влияют на варианты:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Parameter settings in use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Используемые настройки параметров.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Levels of extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Уровни расширений.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Usage of additional functionality, such as database log and alerts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Использование дополнительных функций, таких как журнал базы данных и оповещения.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Extreme database logging will further reduce throughput per hour per core below 3K lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Чрезмерная регистрация в журнале базы данных дополнительно снизит пропускную способность в час на ядро менее чем до 3 000 строк.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сложность состава данных — простой план счетов и детализированные подробного планы счетов влияют на пропускную способность (в качестве примера).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Характеристики проводок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>2 GB to 16 GB memory for each core.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2–16 ГБ памяти на каждое ядро.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Auxiliary databases on DB server such as Management reporter and SSRS databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вспомогательные базы данных на сервере базы данных, например базы данных Management Reporter и SSRS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Temp DB = 15% of DB size, with as many files as physical processors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Временная база данных = 15 % от размера базы данных с тем же количеством файлов, что и физические процессоры.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>SAN size and throughput based on total concurrent transaction volume/usage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Размер и пропускная способность SAN на основе всего объема/использования одновременных проводок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Высокая доступность</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>We recommend always utilizing SQL Server in either a cluster or mirroring setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Рекомендуется всегда использовать SQL Server при настройке кластера или зеркального отображения.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The second SQL node should have the same number of cores as the primary node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Второй узел SQL должен иметь то же количество ядер, что и основной узел.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Active Directory Federation Services (AD FS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Службы федерации Active Directory (AD FS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For AD FS sizing, see the <bpt id="p1">[</bpt>AD FS Server Capacity documentation<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Сведения об определении параметров AD FS см. в <bpt id="p1">[</bpt>документации по планированию мощности AD FS сервера<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A <bpt id="p1">[</bpt>sizing spreadsheet<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept> is available for planning the number of instances in your deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Электронная таблица определения параметров<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept> доступна для планирования числа экземпляров в развертывании.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>AOS (Online and batch)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS (Online и пакет)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определение параметров</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Sizing by transaction volume/usage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определение параметров по объему проводок/использованию</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>2K to 6K lines per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2000–6000 строк на ядро</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>16 GB per instance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">16 ГБ на экземпляр</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Standard box – 4 to 24 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Коробка — от 4 до 24 ядер</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>10 to 15 Enterprise users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10–15 пользователей Enterprise на ядро</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>15 to 25 Activity users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">15–25 пользователей Activity на ядро</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>25 to 50 Team members per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">25–50 участников групп на ядро</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Batch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пакет</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>1 to 4 batch threads per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1–4 потока в пакетном задании на ядро</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Size based on batch window characterization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Размер на основании характеристик окна пакета</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Обратите внимание, что AOS, управление данными и пакет принадлежат к одной и той же роли в Service Fabric.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Необходимо определить размер этих трех рабочих нагрузок вместе, а не разделять их как в Microsoft Dynamics AX 2012.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The same variability factors for SQL Server apply here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Здесь применяются те же факторы изменчивости для SQL Server.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Высокая доступность</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Ensure that you have at least 1 to 2 more AOS available than you estimate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Убедитесь, что у вас есть хотя бы 1–2 доступных AOS при оценке.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Ensure that you have at least 3 to 4 virtual hosts available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Убедитесь, что доступно по крайней мере 3–4 виртуальных узла.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Management reporter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В большинстве случаев, если отсутствует чрезмерная нагрузка, рекомендуемых минимальных требований использовать два узла должно быть достаточно.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Only in cases where there is heavy use will you need more than two nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Только при высокой нагрузке необходимо более двух узлов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Please scale as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Выполните масштабирование при необходимости.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>SQL Server Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Службы SQL Server Reporting Services</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>For the general availability release, only one SSRS node can be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В общедоступном выпуске можно развернуть только один узел SSRS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Отслеживайте узел SSRS при тестировании и увеличьте число ядер, доступных для SSRS, при необходимости.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Убедитесь, что имеется предварительно настроенный дополнительный узел, доступный в виртуальном узле, отличном от виртуальной машины SSRS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это важно при наличии проблемы с виртуальной машиной, на которой размещены службы SSRS, или виртуальным узлом.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If this the case, they would need to be replaced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом случае их необходимо заменить.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Environment Orchestrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Orchestrator среды</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The Orchestrator service is the service that manages your deployment and the related communication with LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Orchestrator — это служба, управляющая развертыванием и связанным обменом данными с LCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>This service is deployed as the primary Service Fabric service and requires at least three VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эта служба развертывается как основная служба Service Fabric и требует по крайней мере трех виртуальных машин.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This service is co-located with the Service Fabric orchestration services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эта служба размещается совместно со службами оркестрации Service Fabric.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This and should be sized to the peak load of the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ее параметры должны определять согласно пиковой нагрузке кластера.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>For more information, see <bpt id="p1">[</bpt>Service Fabric cluster capacity planning considerations<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные сведения см. в разделе <bpt id="p1">[</bpt>Рекомендации по планированию загрузки кластера Service Fabric<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Virtualization and oversubscription</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Виртуализация и превышение лимита</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Критически важные службы, такие как AOS, должны размещаться на виртуальных узлах с выделенными ресурсами: ядрами, памятью и диском.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>