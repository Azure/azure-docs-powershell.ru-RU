---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: eeb0db5c9dd180d8194d0bd506296f269c6c5386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964899"
---
# <span data-ttu-id="bb913-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bb913-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="bb913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb913-102">SYNOPSIS</span></span>
<span data-ttu-id="bb913-103">Запуск управляемой специализированной интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="bb913-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="bb913-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb913-104">SYNTAX</span></span>

### <span data-ttu-id="bb913-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb913-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb913-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb913-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb913-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bb913-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb913-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb913-108">DESCRIPTION</span></span>
<span data-ttu-id="bb913-109">Для запуска управляемой выделенной интеграции запускается **cmdlet Start-AzDataFactoryV2IntegrationRuntime.**</span><span class="sxs-lookup"><span data-stu-id="bb913-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="bb913-110">Ресурс будет подготовка, а после операции состояние "Запущено".</span><span class="sxs-lookup"><span data-stu-id="bb913-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="bb913-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb913-111">EXAMPLES</span></span>

### <span data-ttu-id="bb913-112">Пример 1. Запуск интеграции</span><span class="sxs-lookup"><span data-stu-id="bb913-112">Example 1: Start an integration runtime</span></span>
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
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="bb913-113">Этот cmdlet запускает управляемое интегрированное время интеграции с именем test-dedicated-ir.</span><span class="sxs-lookup"><span data-stu-id="bb913-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="bb913-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb913-114">PARAMETERS</span></span>

### <span data-ttu-id="bb913-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bb913-115">-DataFactoryName</span></span>
<span data-ttu-id="bb913-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="bb913-116">The data factory name.</span></span>

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

### <span data-ttu-id="bb913-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb913-117">-DefaultProfile</span></span>
<span data-ttu-id="bb913-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb913-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb913-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bb913-119">-Force</span></span>
<span data-ttu-id="bb913-120">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bb913-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="bb913-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb913-121">-InputObject</span></span>
<span data-ttu-id="bb913-122">Объект интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="bb913-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="bb913-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bb913-123">-Name</span></span>
<span data-ttu-id="bb913-124">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="bb913-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="bb913-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb913-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb913-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb913-126">The resource group name.</span></span>

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

### <span data-ttu-id="bb913-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb913-127">-ResourceId</span></span>
<span data-ttu-id="bb913-128">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="bb913-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bb913-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb913-129">-Confirm</span></span>
<span data-ttu-id="bb913-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bb913-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb913-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb913-131">-WhatIf</span></span>
<span data-ttu-id="bb913-132">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb913-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="bb913-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb913-133">CommonParameters</span></span>
<span data-ttu-id="bb913-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb913-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb913-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb913-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb913-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb913-136">INPUTS</span></span>

### <span data-ttu-id="bb913-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bb913-137">System.String</span></span>

### <span data-ttu-id="bb913-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bb913-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bb913-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb913-139">OUTPUTS</span></span>

### <span data-ttu-id="bb913-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="bb913-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="bb913-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb913-141">NOTES</span></span>

## <span data-ttu-id="bb913-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb913-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb913-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bb913-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
