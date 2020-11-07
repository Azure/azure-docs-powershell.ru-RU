---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: c0932dcefe6d833e64c83eb8b034b812e7bf3430
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900906"
---
# <span data-ttu-id="ddd20-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ddd20-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ddd20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddd20-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd20-103">Запускает управляемую выделенную среду выполнения для интеграции.</span><span class="sxs-lookup"><span data-stu-id="ddd20-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="ddd20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddd20-104">SYNTAX</span></span>

### <span data-ttu-id="ddd20-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddd20-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddd20-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd20-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd20-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ddd20-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd20-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd20-108">DESCRIPTION</span></span>
<span data-ttu-id="ddd20-109">Командлет **Start-AzDataFactoryV2IntegrationRuntime** запускает управляемую выделенную среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ddd20-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="ddd20-110">Ресурс подготовлен к работе и после операции с состоянием "начато".</span><span class="sxs-lookup"><span data-stu-id="ddd20-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="ddd20-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddd20-111">EXAMPLES</span></span>

### <span data-ttu-id="ddd20-112">Пример 1: запуск среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="ddd20-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="ddd20-113">Этот командлет запускает управляемую выделенную среду выполнения для интеграции с именем "тест-выделенный"-"IR".</span><span class="sxs-lookup"><span data-stu-id="ddd20-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="ddd20-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd20-114">PARAMETERS</span></span>

### <span data-ttu-id="ddd20-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ddd20-115">-DataFactoryName</span></span>
<span data-ttu-id="ddd20-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ddd20-116">The data factory name.</span></span>

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

### <span data-ttu-id="ddd20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd20-117">-DefaultProfile</span></span>
<span data-ttu-id="ddd20-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd20-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd20-119">-Force</span></span>
<span data-ttu-id="ddd20-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ddd20-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ddd20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd20-121">-InputObject</span></span>
<span data-ttu-id="ddd20-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="ddd20-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="ddd20-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddd20-123">-Name</span></span>
<span data-ttu-id="ddd20-124">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ddd20-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd20-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddd20-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddd20-126">The resource group name.</span></span>

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

### <span data-ttu-id="ddd20-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd20-127">-ResourceId</span></span>
<span data-ttu-id="ddd20-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd20-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ddd20-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddd20-129">-Confirm</span></span>
<span data-ttu-id="ddd20-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddd20-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd20-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd20-131">-WhatIf</span></span>
<span data-ttu-id="ddd20-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="ddd20-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd20-133">CommonParameters</span></span>
<span data-ttu-id="ddd20-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddd20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd20-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd20-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd20-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddd20-136">INPUTS</span></span>

### <span data-ttu-id="ddd20-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd20-137">System.String</span></span>

### <span data-ttu-id="ddd20-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ddd20-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ddd20-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd20-139">OUTPUTS</span></span>

### <span data-ttu-id="ddd20-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="ddd20-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ddd20-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddd20-141">NOTES</span></span>

## <span data-ttu-id="ddd20-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd20-142">RELATED LINKS</span></span>

[<span data-ttu-id="ddd20-143">Остановить-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ddd20-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
