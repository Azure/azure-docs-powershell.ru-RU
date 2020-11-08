---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236789"
---
# <span data-ttu-id="cbd17-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="cbd17-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="cbd17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbd17-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd17-103">Обновляет узел среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="cbd17-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="cbd17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbd17-104">SYNTAX</span></span>

### <span data-ttu-id="cbd17-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbd17-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd17-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd17-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd17-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cbd17-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbd17-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd17-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd17-109">Командлет **Update-AzDataFactoryV2IntegrationRuntimeNode** обновляет свойства узла среды выполнения интеграции с самостоятельным размещением в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="cbd17-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="cbd17-110">В настоящее время поддерживается только обновление "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="cbd17-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="cbd17-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbd17-111">EXAMPLES</span></span>

### <span data-ttu-id="cbd17-112">Пример 1: обновление узла среды выполнения интеграции с самостоятельным размещением</span><span class="sxs-lookup"><span data-stu-id="cbd17-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="cbd17-113">Командлет обновляет "ConcurrentJobsLimit" до 3 для узла "Node_1" в саморазмещенной среде выполнения Integration теста-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="cbd17-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cbd17-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbd17-114">PARAMETERS</span></span>

### <span data-ttu-id="cbd17-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="cbd17-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="cbd17-116">Количество одновременных заданий, разрешенных для выполнения на узле среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd17-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="cbd17-117">Значения в диапазоне от 1 до maxConcurrentJobs разрешены.</span><span class="sxs-lookup"><span data-stu-id="cbd17-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="cbd17-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cbd17-118">-DataFactoryName</span></span>
<span data-ttu-id="cbd17-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="cbd17-119">The data factory name.</span></span>

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

### <span data-ttu-id="cbd17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd17-120">-DefaultProfile</span></span>
<span data-ttu-id="cbd17-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd17-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd17-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd17-122">-InputObject</span></span>
<span data-ttu-id="cbd17-123">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="cbd17-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="cbd17-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="cbd17-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="cbd17-125">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd17-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="cbd17-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbd17-126">-Name</span></span>
<span data-ttu-id="cbd17-127">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd17-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="cbd17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd17-128">-ResourceGroupName</span></span>
<span data-ttu-id="cbd17-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbd17-129">The resource group name.</span></span>

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

### <span data-ttu-id="cbd17-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd17-130">-ResourceId</span></span>
<span data-ttu-id="cbd17-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd17-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cbd17-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbd17-132">-Confirm</span></span>
<span data-ttu-id="cbd17-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbd17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd17-134">-WhatIf</span></span>
<span data-ttu-id="cbd17-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbd17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd17-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbd17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd17-137">CommonParameters</span></span>
<span data-ttu-id="cbd17-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbd17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd17-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd17-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd17-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbd17-140">INPUTS</span></span>

### <span data-ttu-id="cbd17-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd17-141">System.String</span></span>

### <span data-ttu-id="cbd17-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cbd17-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cbd17-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd17-143">OUTPUTS</span></span>

### <span data-ttu-id="cbd17-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="cbd17-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="cbd17-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbd17-145">NOTES</span></span>
<span data-ttu-id="cbd17-146">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="cbd17-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="cbd17-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbd17-147">RELATED LINKS</span></span>

<span data-ttu-id="cbd17-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="cbd17-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
