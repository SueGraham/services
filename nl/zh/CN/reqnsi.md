---

copyright:
  years: 2016, 2017
lastupdated: "2017-05-16"

---


{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


#服务
{: #services}

在 {{site.data.keyword.Bluemix}} 控制台中，可以在**目录**的**服务**下找到可用的服务。
{:shortdesc}


{{site.data.keyword.Bluemix_notm}} 中提供针对移动应用程序的预定义服务。{{site.data.keyword.Bluemix_notm}} 为对移动应用程序实施、托管和扩展这些移动服务提供了便利。您可以关注应用程序逻辑和应用程序设计。

{{site.data.keyword.Bluemix_notm}} 托管并管理针对 Web 应用程序的中间件服务。应用程序开发者可以指定他们需要的中间件服务。然后，{{site.data.keyword.Bluemix_notm}} 会自动供应指定中间件服务的新实例，并将服务实例绑定到应用程序。

{{site.data.keyword.Bluemix_notm}} 以两种方式显示服务：按服务类别和按服务支持类型。



<dl>
<dt><strong>类别</strong></dt>
<dd>{{site.data.keyword.Bluemix_notm}} 服务按不同的类别进行组织。在每个服务类别中，IBM 创建的服务最先列出，然后是第三方服务，最后是社区服务。</dd>
<dt><strong>支持</strong></dt>
<dd>系统为 {{site.data.keyword.Bluemix_notm}} 服务提供了多个级别的支持。下表描述了 {{site.data.keyword.Bluemix_notm}} 服务的一般支持信息：</dd>
</dl>



|类型	|描述	|支持详细信息|
|:------|:--------------|:--------------|
|IBM	|IBM 提供且普遍可用的服务。	|如果问题确定为 IBM 提供且普遍可用的服务中的缺陷，那么将受支持。将基于您设置的严重性提供支持。有关凭单严重性的更多信息，请参阅[联系支持人员](/docs/support/index.html#contacting-bluemix-support)。|
|第三方	|非 IBM 公司提供的服务。	|对第三方服务的支持由服务提供者提供。如果 IBM 调查的某个问题确定为第三方服务中的缺陷，那么 IBM 没有义务提供修订。如果需要，IBM 将与第三方服务提供者共享分析。|
|社区	|开放式源代码社区提供的服务。	|对社区服务的支持由 {{site.data.keyword.Bluemix_notm}} 开发者社区提供。如果 IBM 调查的某个问题确定为社区服务中的缺陷，那么 IBM 没有义务提供修订。|
|Beta	|尚不可用于生产、目前处于开发试用阶段的服务。Beta 服务可帮助开发和市场营销团队先评估服务价值，再使服务普遍可用。	|如果问题确定为 IBM 提供的 beta 服务中的缺陷，那么将受支持，但 IBM 没有义务提供修订。此外，将在适当的情况下为问题凭单分配严重性 3 或 4。有关凭单严重性的信息，请参阅[联系支持人员](/docs/support/index.html#contacting-bluemix-support)。|
{: caption="表 1. Bluemix 服务支持信息" caption-side="top"}




{{site.data.keyword.Bluemix_notm}} 还包含可供您试用的试验性服务。要查看所有可用的试验性服务、样板和运行时，请登录到 {{site.data.keyword.Bluemix_notm}}，滚动到“目录”的底部，然后单击 **{{site.data.keyword.Bluemix_notm}} Lab Catalog**。

试验性服务可能不稳定，并且可能会发生变化而与较低版本不兼容。不建议在生产环境中使用这些服务。对试验性服务的支持由 {{site.data.keyword.Bluemix_notm}} 开发者社区提供。对于某个问题，如果经 IBM 调查后确定该问题是试验性服务中的缺陷，那么 IBM 没有义务提供修订。

要在 {{site.data.keyword.Bluemix_notm}} 控制台、cf 命令行界面、IBM {{site.data.keyword.Bluemix_notm}} DevOps Services 或任何支持的工具中使用服务，请执行以下步骤：

1. 创建服务的实例。在大多数情况下，都可以在创建应用程序时创建服务实例。

2. 识别使用新服务实例的应用程序。对于 Web 应用程序，您可以指定多个应用程序使用相同的服务实例，此设置通常用于数据共享。

3. 在应用程序中编写自己的代码用于与服务进行交互。

# 将服务添加到应用程序
{: #add_service}


{{site.data.keyword.Bluemix}} 具有服务列表并为开发者管理这些服务。要添加服务以供您的应用程序使用，必须请求此服务的实例，并将该应用程序配置为与此服务进行交互。

通过下列方式，您可以在 {{site.data.keyword.Bluemix_notm}} 中查看所有可用服务：

* 从 {{site.data.keyword.Bluemix_notm}} 用户界面。查看 {{site.data.keyword.Bluemix_notm}}“目录”。
* 从 cf 命令行界面。使用 **cf marketplace** 命令。
* 从您自己的应用程序。使用 [GET /v2/services Services API ![外部链接图标](../icons/launch-glyph.svg)](http://apidocs.cloudfoundry.org/197/services/list_all_services.html){: new_window}。

在开发应用程序时，您可以选择所需的服务。在您进行选择后，{{site.data.keyword.Bluemix_notm}} 将与该服务进行交互，并执行必要的步骤以供应服务的资源。对于不同类型的服务，供应过程可能会不同。例如，数据库服务会创建数据库，移动应用程序的推送通知服务会生成配置信息。

{{site.data.keyword.Bluemix_notm}} 通过使用服务实例来为您的应用程序提供服务的资源。可以跨 Web 应用程序共享服务实例。

您还可使用在其他区域中托管的服务（如果这些服务在这些区域中可用）。这些服务必须可从因特网访问并且具有 API 端点。必须按照与编码外部应用程序或第三方工具以使用 {{site.data.keyword.Bluemix_notm}} 服务相同的方式来手动编码应用程序以使用这些服务。有关更多信息，请参阅[允许外部应用程序和第三方工具使用 {{site.data.keyword.Bluemix_notm}} 服务](#accser_external)。



## 请求新的服务实例
{: #req_instance}

要请求新的服务实例，必须使用 {{site.data.keyword.Bluemix_notm}} 控制台或 cf 命令行界面。

**注：**指定服务名称时，请避免使用非字母或数字字符，因为结果可能难以预料。

如果使用 {{site.data.keyword.Bluemix_notm}} 控制台请求服务实例，请完成以下步骤：

1. 在 {{site.data.keyword.Bluemix_notm}} **目录**中，单击要添加的服务的磁贴。这将打开服务详细信息页面。

2. 在“添加服务”窗格中，从**应用程序**列表中选择要将此服务实例绑定到的应用程序。

3. 在**服务名称**字段中键入名称。系统提供了缺省服务名称。您可以更改该字段中的名称，也可以保留不变。

4. 完成其他字段或选择，然后单击**创建**。

如果使用 cf 命令行界面请求服务实例，请完成以下步骤：

1. 使用 **cf marketplace** 命令查找所需服务的名称和套餐。

2. 使用以下命令创建服务实例，其中 service_name 是服务的名称；service_plan 是服务的套餐；service_instance 是您希望用于此服务实例的名称。

    ```
cf create-service service_name service_plan service_instance
    ```

3. 使用以下命令将服务实例绑定到应用程序，其中 appname 是应用程序的名称；service_instance 是服务实例的名称。

    ```
    cf bind-service appname service_instance
    ```

只能将服务实例绑定到位于同一空间或组织中的应用程序实例。不过，也可以按照与外部应用程序相同的方式使用其他空间或组织中的服务实例。不要创建绑定，请改用凭证来直接配置应用程序实例。有关外部应用程序如何使用 {{site.data.keyword.Bluemix_notm}} 服务的更多信息，请参阅[允许外部应用程序使用 {{site.data.keyword.Bluemix_notm}} 服务](#accser_external)。


## 将应用程序配置为与服务进行交互
{: #config}

将服务实例绑定到应用程序后，必须将应用程序配置为与服务交互。

每个服务可能需要采用不同的机制与应用程序进行通信。在开发应用程序时，会记录这些机制作为服务定义的一部分以供您参阅。为了实现一致性，您的应用程序需要通过这些机制与服务进行交互。

* 要与数据库服务交互，请使用 {{site.data.keyword.Bluemix_notm}} 提供的信息，例如，用户标识、密码和应用程序的访问 URI。
* 要与移动后端服务交互，请使用 {{site.data.keyword.Bluemix_notm}} 提供的信息，例如，应用程序标识、特定于客户机的安全性信息以及应用程序的访问 URI。移动服务通常彼此配合工作，以便能够在一组服务之间共享上下文信息，例如，应用程序开发者名称和使用应用程序的用户。
* 要与 Web 应用程序或移动应用程序的服务器端云代码交互，请在应用程序的 *VCAP_SERVICES* 环境变量中使用 {{site.data.keyword.Bluemix_notm}} 提供的信息，例如，运行时凭证。*VCAP_SERVICES* 环境变量的值是序列化 JSON 对象。该变量包含与绑定应用程序的服务进行交互所需要的运行时数据。不同服务的数据格式不同。您可能需要阅读服务文档以了解预期的结果以及如何解读每条信息。

如果绑定到应用程序的服务崩溃，那么应用程序可能会停止运行或发生错误。{{site.data.keyword.Bluemix_notm}} 不会自动重新启动应用程序，以便从这些问题中进行恢复。在进行应用程序编码时，应考虑到识别中断、异常和连接失败以及进行恢复的问题。有关更多信息，请参阅[应用程序不会自动重新启动](/docs/troubleshoot/index.html#ts_topmenubar)故障诊断主题。

## 允许外部应用程序使用 {{site.data.keyword.Bluemix_notm}} 服务
{: #accser_external}

您可能会有在 {{site.data.keyword.Bluemix_notm}} 外部创建和运行的应用程序，或者，您可能会使用第三方工具。如果 {{site.data.keyword.Bluemix_notm}} 服务提供可从因特网访问的服务密钥，那么您可以通过本地应用程序或第三方工具来使用这些服务。

以下服务提供服务密钥供您在外部使用：

* {{site.data.keyword.amashort_old}} <!--Advanced Mobile Access-->
* {{site.data.keyword.alchemyapishort}} <!--AlchemyAPI-->
* {{site.data.keyword.alertnotificationshort}} <!--Alert Notification-->
* {{site.data.keyword.sparks}} <!--Analytics for Apache Spark-->
* {{site.data.keyword.appseccloudshort}} <!--Application Security on Cloud-->
* {{site.data.keyword.blockchain}} <!--Blockchain-->
* {{site.data.keyword.cloudant}} <!--Cloudant&reg; NoSQL DB-->
* {{site.data.keyword.iotmapinsights_short}} <!--Context Mapping-->
* {{site.data.keyword.conversationshort}} <!--Conversation-->
* {{site.data.keyword.dashdbshort}} <!--dashDB-->
* {{site.data.keyword.discoveryshort}} <!--Discovery-->
* {{site.data.keyword.documentconversionshort}} <!--Document Conversion-->
* {{site.data.keyword.iotdriverinsights_short}} <!--Driver Behavior-->
* {{site.data.keyword.geospatialshort_Geospatial}} <!--Geospatial Analytics-->
* {{site.data.keyword.GlobalizationPipeline_short}} <!--Globalization Pipeline-->
* {{site.data.keyword.appconserviceshort}} <!--IBM&reg; App Connect-->
* {{site.data.keyword.dataworks_short}} <!--IBM&reg; Data Connect-->
* {{site.data.keyword.graphshort}} <!--IBM&reg; Graph-->
* {{site.data.keyword.iotelectronics_full}} <!--IBM&reg; IoT for Electronics-->
* {{site.data.keyword.twittershort}} <!--Insights for Twitter-->
* {{site.data.keyword.iot4auto_short}} <!--IoT for Automotive-->
* {{site.data.keyword.iotinsurance_short}} <!--IoT for Insurance-->
* {{site.data.keyword.languagetranslatorshort}} <!--Language Translator-->
* {{site.data.keyword.dwl_short}} <!--Lift-->
* {{site.data.keyword.messagehub}} <!--Message Hub-->
* {{site.data.keyword.mobileanalytics_short}} <!--Mobile Analytics-->
* {{site.data.keyword.nlclassifiershort}} <!--Natural Language Classifier-->
* {{site.data.keyword.objectstorageshort}} <!--Object Storage-->
* {{site.data.keyword.personalityinsightsshort}} <!--Personality Insights-->
* {{site.data.keyword.HybridConnect_short}} <!--Product Insights-->
* {{site.data.keyword.mobilepush}} <!--Push-->
* {{site.data.keyword.retrieveandrankshort}} <!--Retrieve and Rank-->
* {{site.data.keyword.speechtotextshort}} <!-- Speech to Text-->
* {{site.data.keyword.streaminganalyticsshort}} <!--Streaming Analytics-->
* {{site.data.keyword.texttospeechshort}} <!--Text to Speech-->
* {{site.data.keyword.toneanalyzershort}} <!--Tone Analyzer-->
* {{site.data.keyword.tradeoffanalyticsshort}} <!--Tradeoff Analytics-->
* {{site.data.keyword.weather_short}} <!--Weather Company Data-->
* {{site.data.keyword.workloadscheduler}} <!--Workload Scheduler-->

要允许外部应用程序或第三方工具使用 {{site.data.keyword.Bluemix_notm}} 服务，请完成以下步骤：

1. 请求服务的实例。
    1. 在 {{site.data.keyword.Bluemix_notm}} 用户界面中的“仪表板”上，单击**使用服务或 API**。这将显示“目录”。
    2. 在“目录”中，通过单击服务磁贴来选择所需的服务。这将打开服务详细信息页面。
    3. 在“添加服务”窗口中，将**应用程序**列表选择保留为**保持未绑定**。此选择意味着该服务不会连接到 {{site.data.keyword.Bluemix_notm}} 应用程序。
    4. 根据需要进行任何其他选择。然后，单击**创建**。这将创建服务实例，并显示服务“仪表板”。
2. 在服务“仪表板”的导航窗格中，可以选择**服务凭证**来查看或添加 JSON 格式的凭证。使用显示的 API 密钥作为凭证来连接到服务实例。

在 {{site.data.keyword.Bluemix_notm}} 外部运行的应用程序现在可以访问 {{site.data.keyword.Bluemix_notm}} 服务。

**注：**如果想要删除服务实例或检查记帐信息，必须返回到用户界面中用于管理服务实例的“仪表板”。

## 创建用户提供的服务实例
{: #user_provide_services}

您可能有一些资源是在 {{site.data.keyword.Bluemix_notm}} 外部管理的。如果您拥有从因特网访问这些外部资源的凭证，那么可以创建用户提供的 {{site.data.keyword.Bluemix_notm}} 服务实例来代表外部资源并与这些资源进行通信。

要创建用户提供的服务实例并将其绑定到应用程序，请完成以下步骤：

1. 创建用户提供的服务实例，方法是使用 **cf create-user-provided-service** 或 **cf cups** 命令：
    * 要创建用户提供的一般服务实例，请使用 **-p** 选项，并用逗号分隔参数名称。随后，cf 命令行界面会依次提示您提供每个参数的值。例如：
        ```
cf cups testups1 -p "host, port, dbname, username, password"
        host> pubsub01.example.com
        port> 1234
        dbname> sampledb01
        username> pubsubuser
        password> p@$$w0rd
        正在以 user@sample.com 身份在组织 my-org/空间 dev 中创建用户提供的服务 testups1...
        成功
        ```

    * 要创建服务实例来将信息排出至第三方日志管理软件，请使用 **-l** 选项，然后指定第三方日志管理软件提供的目标。例如：

        ```
cf cups testups2 -l syslog://example.com
        正在以 user@sample.com 身份在组织 my-org/空间 dev 中创建用户提供的服务 testups2...
        成功
        ```

    如果想要更新用户提供的服务实例的一个或多个参数，请使用 **cf update-user-provided-service** 或 **cf uups** 命令。

    * 要更新一般用户提供的服务实例，请使用 **-p** 选项，并在 json 对象中指定参数键和值。例如：

        ```
cf uups testups1 -p "{\"username\":\"pubsubuser2\",\"password\":\"p@$$w0rd2\"}"
        正在以 user@sample.com 身份在组织 my-org/空间 dev 中更新用户提供的服务 testups1...
        成功
        ```

    * 要创建服务实例来将信息排出至第三方日志管理软件，请使用 -l 选项。例如：

        ```
cf uups testups2 -l syslog://example2.com
        正在以 user@sample.com 身份在组织 my-org/空间 dev 中更新用户提供的服务 testups2...
        成功
        ```

2. 使用 cf bind-service 命令将该服务实例绑定到您的应用程序。例如：

	```
	cf bind-service myapp testups1
	正在以 user@sample.com 身份在组织 my-org/空间 dev 中将服务 testups1 绑定到应用程序 myapp...
	成功
	```

现在，您可以将应用程序配置为使用外部资源。有关如何将应用程序配置为与服务进行交互的信息，请参阅[将应用程序配置为与服务进行交互](#config){: new_window}。

## 在其他区域使用服务
{: #cross_region_service}

如果您在一个区域创建了服务实例并将其绑定到应用程序，那么可以通过以下某种方法，在另外一个区域使用此服务实例：

  * 使用服务凭证来直接配置应用程序实例。有关详细信息，请参阅[允许外部应用程序使用 {{site.data.keyword.Bluemix_notm}} 服务](#accser_external)。
  * 创建用户提供的服务作为网桥。

	假定您是在要使用服务实例的区域开始操作。要使用另一个区域中存在的服务实例，请完成以下步骤：

      1. 切换到服务实例所在的区域。在 {{site.data.keyword.Bluemix_notm}} 菜单栏中，展开**区域**或单击**区域**图标，然后选择服务实例所在的区域。

      2. 在服务所在的区域中从服务实例的 VCAP_SERVICES 环境变量检索凭证和连接参数。请完成以下步骤：

	       1. 在 {{site.data.keyword.Bluemix_notm}}“仪表板”中，单击应用程序磁贴。这将显示“概述”页面。
	       2. 在导航窗格中，单击**环境变量**。这将显示 *VCAP_SERVICES* 环境变量详细信息。记录服务实例的 JSON 内容。

      3. 切换到您要在其中使用服务实例的区域。在 {{site.data.keyword.Bluemix_notm}} 菜单栏中，展开**区域**或单击**区域**图标，然后选择要在其中使用服务实例的区域。

      4. 通过使用从 *VCAP_SERVICES* 环境变量记录的凭证和连接参数，以创建用户提供的服务实例。有关如何创建用户提供的服务实例的信息，请参阅[创建用户提供的服务实例](#user_provide_services)。

      5. 通过使用以下命令，将用户创建的服务实例绑定到您的应用程序：

	     ```
	     cf bind-service myapp user-provided_service_instance
	```






## 在其他服务中使用服务
{: #s2s_binding}

通过服务访问授权，一个服务可以直接访问另一个服务。在 {{site.data.keyword.Bluemix_notm}}“仪表板”上，可以授权和配置某个服务实例对其他服务实例的访问权。

要从另一个服务使用某个服务实例，请完成以下步骤：

1. 在 {{site.data.keyword.Bluemix_notm}}“仪表板”上，单击要访问的服务的磁贴。这将显示该服务的仪表板。
2. 在导航窗格中，单击**管理**，通过使用该服务实例的控制台来授权其他服务实例绑定该服务实例。
3. 如果想要拒绝其他服务访问该服务实例，请单击导航窗格中的**服务访问授权**，然后使用**撤销**来除去服务绑定。

# rellinks
{: #rellinks}

## general
{: #general}

* [使用 {{site.data.keyword.Bluemix_notm}} 用户界面绑定服务](/docs/cfapps/ee.html#ee_bindui)
* [检索 VCAP_SERVICES](/docs/cli/vcapsvc.html#retrieving)
