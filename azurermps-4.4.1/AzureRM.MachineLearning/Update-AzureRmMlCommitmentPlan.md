---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733108"
---
# <span data-ttu-id="b96bd-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b96bd-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="b96bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b96bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b96bd-103">Обновляет свойства существующего ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="b96bd-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b96bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b96bd-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b96bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b96bd-106">Обновляет существующий ресурс плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="b96bd-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="b96bd-107">Обратите внимание, что большая часть свойств плана обязательства является постоянной и не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="b96bd-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="b96bd-108">Свойства, которые можно изменить, включают SKU (с помощью которого можно перенести план обязательства из одного SKU в другой) и на теги.</span><span class="sxs-lookup"><span data-stu-id="b96bd-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="b96bd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b96bd-109">EXAMPLES</span></span>

### <span data-ttu-id="b96bd-110">--------------------------Пример 1: Обновление плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="b96bd-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="b96bd-111">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b96bd-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="b96bd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b96bd-112">PARAMETERS</span></span>

### <span data-ttu-id="b96bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b96bd-113">-Force</span></span>
<span data-ttu-id="b96bd-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b96bd-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b96bd-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b96bd-115">-Name</span></span>
<span data-ttu-id="b96bd-116">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b96bd-116">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b96bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="b96bd-118">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b96bd-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b96bd-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b96bd-119">-SkuCapacity</span></span>
<span data-ttu-id="b96bd-120">Емкость SKU, используемая при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b96bd-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b96bd-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b96bd-121">-SkuName</span></span>
<span data-ttu-id="b96bd-122">Имя SKU, которое будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b96bd-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b96bd-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b96bd-123">-SkuTier</span></span>
<span data-ttu-id="b96bd-124">Уровень SKU, который будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b96bd-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b96bd-125">-Теги</span><span class="sxs-lookup"><span data-stu-id="b96bd-125">-Tags</span></span>
<span data-ttu-id="b96bd-126">Теги для ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="b96bd-126">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="b96bd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b96bd-127">-Confirm</span></span>
<span data-ttu-id="b96bd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b96bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b96bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96bd-129">-WhatIf</span></span>
<span data-ttu-id="b96bd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b96bd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b96bd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b96bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b96bd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96bd-132">-DefaultProfile</span></span>
<span data-ttu-id="b96bd-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b96bd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96bd-134">CommonParameters</span></span>
<span data-ttu-id="b96bd-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b96bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96bd-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b96bd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96bd-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b96bd-137">INPUTS</span></span>

## <span data-ttu-id="b96bd-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b96bd-138">OUTPUTS</span></span>

### <span data-ttu-id="b96bd-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b96bd-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b96bd-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b96bd-140">NOTES</span></span>
<span data-ttu-id="b96bd-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b96bd-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b96bd-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b96bd-142">RELATED LINKS</span></span>

