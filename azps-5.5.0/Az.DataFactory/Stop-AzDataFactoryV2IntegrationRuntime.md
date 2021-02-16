---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234660"
---
# <span data-ttu-id="1aada-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aada-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1aada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aada-102">SYNOPSIS</span></span>
<span data-ttu-id="1aada-103">Остановка управляемой специализированной интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="1aada-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="1aada-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1aada-104">SYNTAX</span></span>

### <span data-ttu-id="1aada-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1aada-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1aada-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1aada-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aada-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1aada-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aada-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aada-108">DESCRIPTION</span></span>
<span data-ttu-id="1aada-109">Командалет **Stop-AzDataFactoryV2IntegrationRuntime** останавливает управляемое время интеграции в состоянии "Начатая", которое было запущено Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="1aada-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="1aada-110">Ресурсы будут выпущены, а государственные переводы — в "Остановлено".</span><span class="sxs-lookup"><span data-stu-id="1aada-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="1aada-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1aada-111">EXAMPLES</span></span>

### <span data-ttu-id="1aada-112">Пример 1. Остановка управляемой интеграции с запущенным процессом в состоянии "Начало".</span><span class="sxs-lookup"><span data-stu-id="1aada-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="1aada-113">Для управляемой интеграции режим test-reserlved-ir находится в состоянии "Начало".</span><span class="sxs-lookup"><span data-stu-id="1aada-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="1aada-114">После запуска Stop-AzDataFactoryV2IntegrationRuntime ресурсы выпускаются, а штат передает их в "Остановлено".</span><span class="sxs-lookup"><span data-stu-id="1aada-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="1aada-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aada-115">PARAMETERS</span></span>

### <span data-ttu-id="1aada-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1aada-116">-DataFactoryName</span></span>
<span data-ttu-id="1aada-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1aada-117">The data factory name.</span></span>

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

### <span data-ttu-id="1aada-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aada-118">-DefaultProfile</span></span>
<span data-ttu-id="1aada-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1aada-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aada-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1aada-120">-Force</span></span>
<span data-ttu-id="1aada-121">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1aada-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1aada-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aada-122">-InputObject</span></span>
<span data-ttu-id="1aada-123">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="1aada-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="1aada-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1aada-124">-Name</span></span>
<span data-ttu-id="1aada-125">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="1aada-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="1aada-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aada-126">-ResourceGroupName</span></span>
<span data-ttu-id="1aada-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1aada-127">The resource group name.</span></span>

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

### <span data-ttu-id="1aada-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aada-128">-ResourceId</span></span>
<span data-ttu-id="1aada-129">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1aada-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1aada-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aada-130">-Confirm</span></span>
<span data-ttu-id="1aada-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1aada-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aada-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aada-132">-WhatIf</span></span>
<span data-ttu-id="1aada-133">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1aada-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1aada-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aada-134">CommonParameters</span></span>
<span data-ttu-id="1aada-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aada-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aada-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aada-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aada-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1aada-137">INPUTS</span></span>

### <span data-ttu-id="1aada-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1aada-138">System.String</span></span>

### <span data-ttu-id="1aada-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aada-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1aada-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1aada-140">OUTPUTS</span></span>

### <span data-ttu-id="1aada-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1aada-141">System.Void</span></span>

## <span data-ttu-id="1aada-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1aada-142">NOTES</span></span>
<span data-ttu-id="1aada-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="1aada-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1aada-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aada-144">RELATED LINKS</span></span>

[<span data-ttu-id="1aada-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aada-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
