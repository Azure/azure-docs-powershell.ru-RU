---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: ca0f14bf6940c9d81933c4a42703d828efdc5e51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998416"
---
# <span data-ttu-id="6e35c-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6e35c-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="6e35c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e35c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e35c-103">Обновления узла runtime для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="6e35c-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="6e35c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e35c-104">SYNTAX</span></span>

### <span data-ttu-id="6e35c-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e35c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e35c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e35c-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e35c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6e35c-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e35c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e35c-108">DESCRIPTION</span></span>
<span data-ttu-id="6e35c-109">Для узла runtime самостоятельной интеграции в фабрике данных свойства узла **update-AzDataFactoryV2IntegrationRuntimeNode** обновляются.</span><span class="sxs-lookup"><span data-stu-id="6e35c-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="6e35c-110">В настоящее время поддерживается только обновление "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="6e35c-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="6e35c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e35c-111">EXAMPLES</span></span>

### <span data-ttu-id="6e35c-112">Пример 1. Обновления узла runtime для самостоятельной интеграции</span><span class="sxs-lookup"><span data-stu-id="6e35c-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="6e35c-113">Для узла "Node_1" в режиме самостоятельной интеграции "test-selfhost-ir" для 3-го узла обновляется "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="6e35c-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6e35c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e35c-114">PARAMETERS</span></span>

### <span data-ttu-id="6e35c-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="6e35c-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="6e35c-116">Количество заданий одновременного запуска, разрешенных для узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="6e35c-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="6e35c-117">Допустимы значения от 1 до maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="6e35c-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e35c-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6e35c-118">-DataFactoryName</span></span>
<span data-ttu-id="6e35c-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6e35c-119">The data factory name.</span></span>

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

### <span data-ttu-id="6e35c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e35c-120">-DefaultProfile</span></span>
<span data-ttu-id="6e35c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e35c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e35c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e35c-122">-InputObject</span></span>
<span data-ttu-id="6e35c-123">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="6e35c-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="6e35c-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6e35c-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6e35c-125">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="6e35c-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e35c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6e35c-126">-Name</span></span>
<span data-ttu-id="6e35c-127">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="6e35c-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e35c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e35c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e35c-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e35c-129">The resource group name.</span></span>

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

### <span data-ttu-id="6e35c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e35c-130">-ResourceId</span></span>
<span data-ttu-id="6e35c-131">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6e35c-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6e35c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e35c-132">-Confirm</span></span>
<span data-ttu-id="6e35c-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6e35c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e35c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e35c-134">-WhatIf</span></span>
<span data-ttu-id="6e35c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e35c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e35c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e35c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e35c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e35c-137">CommonParameters</span></span>
<span data-ttu-id="6e35c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e35c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e35c-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e35c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e35c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e35c-140">INPUTS</span></span>

### <span data-ttu-id="6e35c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6e35c-141">System.String</span></span>

### <span data-ttu-id="6e35c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6e35c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6e35c-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e35c-143">OUTPUTS</span></span>

### <span data-ttu-id="6e35c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6e35c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6e35c-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e35c-145">NOTES</span></span>
<span data-ttu-id="6e35c-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="6e35c-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="6e35c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e35c-147">RELATED LINKS</span></span>

<span data-ttu-id="6e35c-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="6e35c-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

