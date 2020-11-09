---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313730"
---
# <span data-ttu-id="5929a-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5929a-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5929a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5929a-102">SYNOPSIS</span></span>
<span data-ttu-id="5929a-103">Запускает управляемую выделенную среду выполнения для интеграции.</span><span class="sxs-lookup"><span data-stu-id="5929a-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="5929a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5929a-104">SYNTAX</span></span>

### <span data-ttu-id="5929a-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5929a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5929a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5929a-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5929a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5929a-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5929a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5929a-108">DESCRIPTION</span></span>
<span data-ttu-id="5929a-109">Командлет **Start-AzDataFactoryV2IntegrationRuntime** запускает управляемую выделенную среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5929a-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="5929a-110">Ресурс подготовлен к работе и после операции с состоянием "начато".</span><span class="sxs-lookup"><span data-stu-id="5929a-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="5929a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5929a-111">EXAMPLES</span></span>

### <span data-ttu-id="5929a-112">Пример 1: запуск среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="5929a-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="5929a-113">Этот командлет запускает управляемую выделенную среду выполнения для интеграции с именем "тест-выделенный"-"IR".</span><span class="sxs-lookup"><span data-stu-id="5929a-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="5929a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5929a-114">PARAMETERS</span></span>

### <span data-ttu-id="5929a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5929a-115">-DataFactoryName</span></span>
<span data-ttu-id="5929a-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5929a-116">The data factory name.</span></span>

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

### <span data-ttu-id="5929a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5929a-117">-DefaultProfile</span></span>
<span data-ttu-id="5929a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5929a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5929a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5929a-119">-Force</span></span>
<span data-ttu-id="5929a-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5929a-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5929a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5929a-121">-InputObject</span></span>
<span data-ttu-id="5929a-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="5929a-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="5929a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5929a-123">-Name</span></span>
<span data-ttu-id="5929a-124">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5929a-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="5929a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5929a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5929a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5929a-126">The resource group name.</span></span>

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

### <span data-ttu-id="5929a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5929a-127">-ResourceId</span></span>
<span data-ttu-id="5929a-128">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="5929a-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5929a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5929a-129">-Confirm</span></span>
<span data-ttu-id="5929a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5929a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5929a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5929a-131">-WhatIf</span></span>
<span data-ttu-id="5929a-132">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="5929a-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5929a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5929a-133">CommonParameters</span></span>
<span data-ttu-id="5929a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5929a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5929a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5929a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5929a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5929a-136">INPUTS</span></span>

### <span data-ttu-id="5929a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5929a-137">System.String</span></span>

### <span data-ttu-id="5929a-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5929a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5929a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5929a-139">OUTPUTS</span></span>

### <span data-ttu-id="5929a-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="5929a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="5929a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5929a-141">NOTES</span></span>

## <span data-ttu-id="5929a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5929a-142">RELATED LINKS</span></span>

[<span data-ttu-id="5929a-143">Остановить-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5929a-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
