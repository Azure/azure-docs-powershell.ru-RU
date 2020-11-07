---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721532"
---
# <span data-ttu-id="0d080-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0d080-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d080-102">SYNOPSIS</span></span>
<span data-ttu-id="0d080-103">Получение сведений о ресурсах среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0d080-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="0d080-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d080-104">SYNTAX</span></span>

### <span data-ttu-id="0d080-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d080-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d080-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d080-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d080-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0d080-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d080-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d080-108">DESCRIPTION</span></span>
<span data-ttu-id="0d080-109">Командлет Get-AzDataFactoryV2IntegrationRuntime получает сведения о средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0d080-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="0d080-110">Если вы задаете имя среды выполнения интеграции, этот командлет получает сведения о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0d080-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="0d080-111">Если имя не задано, этот командлет получает сведения обо всех средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0d080-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="0d080-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d080-112">EXAMPLES</span></span>

### <span data-ttu-id="0d080-113">Пример 1: список всех сред выполнения интеграции в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="0d080-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="0d080-114">Перечислите все среды выполнения интеграции в фабрике данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0d080-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0d080-115">Пример 2: получение управляемой выделенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="0d080-115">Example 2: Get managed dedicated integration runtime</span></span>
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
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="0d080-116">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0d080-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0d080-117">Пример 3: получение управляемой выделенной среды выполнения интеграции с подробным состоянием</span><span class="sxs-lookup"><span data-stu-id="0d080-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="0d080-118">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0d080-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0d080-119">Пример 4: получение самостоятельно размещенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="0d080-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="0d080-120">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0d080-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="0d080-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d080-121">PARAMETERS</span></span>

### <span data-ttu-id="0d080-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0d080-122">-DataFactoryName</span></span>
<span data-ttu-id="0d080-123">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0d080-123">The data factory name.</span></span>

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

### <span data-ttu-id="0d080-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d080-124">-DefaultProfile</span></span>
<span data-ttu-id="0d080-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d080-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d080-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d080-126">-InputObject</span></span>
<span data-ttu-id="0d080-127">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="0d080-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="0d080-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d080-128">-Name</span></span>
<span data-ttu-id="0d080-129">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0d080-129">The integration runtime name.</span></span>

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

### <span data-ttu-id="0d080-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d080-130">-ResourceGroupName</span></span>
<span data-ttu-id="0d080-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d080-131">The resource group name.</span></span>

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

### <span data-ttu-id="0d080-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d080-132">-ResourceId</span></span>
<span data-ttu-id="0d080-133">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0d080-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0d080-134">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="0d080-134">-Status</span></span>
<span data-ttu-id="0d080-135">Состояние сведений о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0d080-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="0d080-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d080-136">CommonParameters</span></span>
<span data-ttu-id="0d080-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d080-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d080-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d080-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d080-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d080-139">INPUTS</span></span>

### <span data-ttu-id="0d080-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d080-140">System.String</span></span>

### <span data-ttu-id="0d080-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0d080-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d080-142">OUTPUTS</span></span>

### <span data-ttu-id="0d080-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="0d080-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="0d080-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="0d080-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="0d080-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d080-147">NOTES</span></span>
<span data-ttu-id="0d080-148">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="0d080-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0d080-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d080-149">RELATED LINKS</span></span>

[<span data-ttu-id="0d080-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="0d080-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0d080-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
