---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912878"
---
# <span data-ttu-id="55e1f-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="55e1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="55e1f-103">Получение сведений о ресурсах среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="55e1f-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="55e1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55e1f-104">SYNTAX</span></span>

### <span data-ttu-id="55e1f-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55e1f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e1f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="55e1f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e1f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="55e1f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e1f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e1f-108">DESCRIPTION</span></span>
<span data-ttu-id="55e1f-109">Командлет Get-AzDataFactoryV2IntegrationRuntime получает сведения о средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="55e1f-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="55e1f-110">Если вы задаете имя среды выполнения интеграции, этот командлет получает сведения о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="55e1f-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="55e1f-111">Если имя не задано, этот командлет получает сведения обо всех средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="55e1f-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="55e1f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55e1f-112">EXAMPLES</span></span>

### <span data-ttu-id="55e1f-113">Пример 1: список всех сред выполнения интеграции в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="55e1f-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="55e1f-114">Перечислите все среды выполнения интеграции в фабрике данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="55e1f-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="55e1f-115">Пример 2: получение управляемой выделенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="55e1f-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="55e1f-116">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="55e1f-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="55e1f-117">Пример 3: получение управляемой выделенной среды выполнения интеграции с подробным состоянием</span><span class="sxs-lookup"><span data-stu-id="55e1f-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="55e1f-118">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="55e1f-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="55e1f-119">Пример 4: получение самостоятельно размещенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="55e1f-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="55e1f-120">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="55e1f-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="55e1f-121">Пример 5: получение самостоятельно размещенной среды выполнения интеграции с подробным состоянием</span><span class="sxs-lookup"><span data-stu-id="55e1f-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="55e1f-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55e1f-122">PARAMETERS</span></span>

### <span data-ttu-id="55e1f-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="55e1f-123">-DataFactoryName</span></span>
<span data-ttu-id="55e1f-124">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="55e1f-124">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e1f-125">-DefaultProfile</span></span>
<span data-ttu-id="55e1f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55e1f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55e1f-127">-InputObject</span></span>
<span data-ttu-id="55e1f-128">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="55e1f-128">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55e1f-129">-Name</span></span>
<span data-ttu-id="55e1f-130">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="55e1f-130">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e1f-131">-ResourceGroupName</span></span>
<span data-ttu-id="55e1f-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55e1f-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55e1f-133">-ResourceId</span></span>
<span data-ttu-id="55e1f-134">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="55e1f-134">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-135">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="55e1f-135">-Status</span></span>
<span data-ttu-id="55e1f-136">Состояние сведений о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="55e1f-136">The integration runtime detail status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e1f-137">CommonParameters</span></span>
<span data-ttu-id="55e1f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55e1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e1f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e1f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e1f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55e1f-140">INPUTS</span></span>

### <span data-ttu-id="55e1f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55e1f-141">System.String</span></span>

### <span data-ttu-id="55e1f-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="55e1f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e1f-143">OUTPUTS</span></span>

### <span data-ttu-id="55e1f-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="55e1f-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="55e1f-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="55e1f-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="55e1f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="55e1f-148">NOTES</span></span>
<span data-ttu-id="55e1f-149">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="55e1f-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="55e1f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55e1f-150">RELATED LINKS</span></span>

[<span data-ttu-id="55e1f-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="55e1f-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55e1f-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
