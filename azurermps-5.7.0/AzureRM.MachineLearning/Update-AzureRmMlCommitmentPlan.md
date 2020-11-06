---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 0cda9ee6f6a93a43234835104130ea39782f36d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564851"
---
# <span data-ttu-id="9a505-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="9a505-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="9a505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a505-102">SYNOPSIS</span></span>
<span data-ttu-id="9a505-103">Обновляет свойства существующего ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="9a505-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a505-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a505-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a505-105">DESCRIPTION</span></span>
<span data-ttu-id="9a505-106">Обновляет существующий ресурс плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="9a505-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="9a505-107">Обратите внимание, что большая часть свойств плана обязательства является постоянной и не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="9a505-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="9a505-108">Свойства, которые можно изменить, включают SKU (с помощью которого можно перенести план обязательства из одного SKU в другой) и на теги.</span><span class="sxs-lookup"><span data-stu-id="9a505-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="9a505-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a505-109">EXAMPLES</span></span>

### <span data-ttu-id="9a505-110">Пример 1: Обновление плана обязательства</span><span class="sxs-lookup"><span data-stu-id="9a505-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="9a505-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a505-111">PARAMETERS</span></span>

### <span data-ttu-id="9a505-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a505-112">-DefaultProfile</span></span>
<span data-ttu-id="9a505-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9a505-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a505-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9a505-114">-Force</span></span>
<span data-ttu-id="9a505-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9a505-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9a505-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a505-116">-Name</span></span>
<span data-ttu-id="9a505-117">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9a505-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a505-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a505-119">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9a505-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9a505-120">-SkuCapacity</span></span>
<span data-ttu-id="9a505-121">Емкость SKU, используемая при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9a505-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9a505-122">-SkuName</span></span>
<span data-ttu-id="9a505-123">Имя SKU, которое будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9a505-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9a505-124">-SkuTier</span></span>
<span data-ttu-id="9a505-125">Уровень SKU, который будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="9a505-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="9a505-126">-Tag</span></span>
<span data-ttu-id="9a505-127">Теги для ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="9a505-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a505-128">-Confirm</span></span>
<span data-ttu-id="9a505-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a505-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a505-130">-WhatIf</span></span>
<span data-ttu-id="9a505-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a505-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a505-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a505-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a505-133">CommonParameters</span></span>
<span data-ttu-id="9a505-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a505-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a505-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a505-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a505-136">INPUTS</span></span>

### <span data-ttu-id="9a505-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="9a505-137">None</span></span>
<span data-ttu-id="9a505-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9a505-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a505-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a505-139">OUTPUTS</span></span>

### <span data-ttu-id="9a505-140">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="9a505-140">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="9a505-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a505-141">NOTES</span></span>
<span data-ttu-id="9a505-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="9a505-142">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9a505-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a505-143">RELATED LINKS</span></span>
