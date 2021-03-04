---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 6bd60ced20e9c5b8ce9c3be01d419af55281aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956120"
---
# <span data-ttu-id="46109-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="46109-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="46109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46109-102">SYNOPSIS</span></span>
<span data-ttu-id="46109-103">Обновляет свойства существующего ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="46109-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="46109-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46109-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46109-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46109-105">DESCRIPTION</span></span>
<span data-ttu-id="46109-106">Обновляет существующий ресурс плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="46109-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="46109-107">Обратите внимание на то, что большинство свойств плана обязательств являются неанимабельными и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="46109-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="46109-108">К свойствам, которые можно изменить, относятся SKU (это позволяет перенести план обязательств из одного SKU в другой) и теги.</span><span class="sxs-lookup"><span data-stu-id="46109-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="46109-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46109-109">EXAMPLES</span></span>

### <span data-ttu-id="46109-110">Пример 1. Обновление плана обязательств</span><span class="sxs-lookup"><span data-stu-id="46109-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="46109-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46109-111">PARAMETERS</span></span>

### <span data-ttu-id="46109-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46109-112">-DefaultProfile</span></span>
<span data-ttu-id="46109-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="46109-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46109-114">-Force</span><span class="sxs-lookup"><span data-stu-id="46109-114">-Force</span></span>
<span data-ttu-id="46109-115">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="46109-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46109-116">-Name</span><span class="sxs-lookup"><span data-stu-id="46109-116">-Name</span></span>
<span data-ttu-id="46109-117">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="46109-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46109-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46109-118">-ResourceGroupName</span></span>
<span data-ttu-id="46109-119">Имя группы ресурсов для плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="46109-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46109-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="46109-120">-SkuCapacity</span></span>
<span data-ttu-id="46109-121">Емкость SKU, используемая при обновлении плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="46109-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46109-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="46109-122">-SkuName</span></span>
<span data-ttu-id="46109-123">Имя SKU, используемого при обновлении плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="46109-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46109-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="46109-124">-SkuTier</span></span>
<span data-ttu-id="46109-125">Уровень SKU, который используется при обновлении плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="46109-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46109-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="46109-126">-Tag</span></span>
<span data-ttu-id="46109-127">Теги для ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="46109-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46109-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46109-128">-Confirm</span></span>
<span data-ttu-id="46109-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="46109-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46109-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46109-130">-WhatIf</span></span>
<span data-ttu-id="46109-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46109-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46109-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46109-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46109-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46109-133">CommonParameters</span></span>
<span data-ttu-id="46109-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46109-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46109-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46109-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46109-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46109-136">INPUTS</span></span>

### <span data-ttu-id="46109-137">Нет</span><span class="sxs-lookup"><span data-stu-id="46109-137">None</span></span>

## <span data-ttu-id="46109-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46109-138">OUTPUTS</span></span>

### <span data-ttu-id="46109-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="46109-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="46109-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46109-140">NOTES</span></span>
<span data-ttu-id="46109-141">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="46109-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="46109-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46109-142">RELATED LINKS</span></span>
