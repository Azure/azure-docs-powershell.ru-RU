---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fd6e979b753bd5fea21af050492b194326122a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568606"
---
# <span data-ttu-id="5a46f-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a46f-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5a46f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a46f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a46f-103">Получение сведений о ресурсах среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5a46f-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a46f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a46f-104">SYNTAX</span></span>

### <span data-ttu-id="5a46f-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a46f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a46f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a46f-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a46f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5a46f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a46f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a46f-108">DESCRIPTION</span></span>
<span data-ttu-id="5a46f-109">Командлет Get-AzureRmDataFactoryV2IntegrationRuntime получает сведения о средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5a46f-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="5a46f-110">Если вы задаете имя среды выполнения интеграции, этот командлет получает сведения о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5a46f-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="5a46f-111">Если имя не задано, этот командлет получает сведения обо всех средах выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5a46f-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="5a46f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a46f-112">EXAMPLES</span></span>

### <span data-ttu-id="5a46f-113">Пример 1: список всех сред выполнения интеграции в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="5a46f-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="5a46f-114">Перечислите все среды выполнения интеграции в фабрике данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="5a46f-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="5a46f-115">Пример 2: получение управляемой выделенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="5a46f-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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

<span data-ttu-id="5a46f-116">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="5a46f-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="5a46f-117">Пример 3: получение управляемой выделенной среды выполнения интеграции с подробным состоянием</span><span class="sxs-lookup"><span data-stu-id="5a46f-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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

<span data-ttu-id="5a46f-118">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="5a46f-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="5a46f-119">Пример 4: получение самостоятельно размещенной среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="5a46f-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="5a46f-120">Эта команда отображает сведения об исполняющей среде интеграции с именем "тест-выделенный-" в подписке для группы ресурсов "RG-Test-dfv2" и фабрики данных с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="5a46f-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="5a46f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a46f-121">PARAMETERS</span></span>

### <span data-ttu-id="5a46f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a46f-122">-DataFactoryName</span></span>
<span data-ttu-id="5a46f-123">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5a46f-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a46f-124">-DefaultProfile</span></span>
<span data-ttu-id="5a46f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a46f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a46f-126">-InputObject</span></span>
<span data-ttu-id="5a46f-127">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="5a46f-127">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a46f-128">-Name</span></span>
<span data-ttu-id="5a46f-129">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5a46f-129">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a46f-130">-ResourceGroupName</span></span>
<span data-ttu-id="5a46f-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a46f-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a46f-132">-ResourceId</span></span>
<span data-ttu-id="5a46f-133">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="5a46f-133">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-134">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="5a46f-134">-Status</span></span>
<span data-ttu-id="5a46f-135">Состояние сведений о среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5a46f-135">The integration runtime detail status.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a46f-136">CommonParameters</span></span>
<span data-ttu-id="5a46f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a46f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a46f-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a46f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a46f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a46f-139">INPUTS</span></span>

### <span data-ttu-id="5a46f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a46f-140">System.String</span></span>
<span data-ttu-id="5a46f-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a46f-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5a46f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a46f-142">OUTPUTS</span></span>

### <span data-ttu-id="5a46f-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5a46f-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5a46f-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a46f-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

## <span data-ttu-id="5a46f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a46f-145">NOTES</span></span>
<span data-ttu-id="5a46f-146">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="5a46f-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5a46f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a46f-147">RELATED LINKS</span></span>

[<span data-ttu-id="5a46f-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a46f-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="5a46f-149">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a46f-149">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
