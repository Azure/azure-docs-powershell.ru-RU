---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 984e1f9d75a7c5a56e6a9bda71a07b193df5be15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734821"
---
# <span data-ttu-id="ca9c5-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ca9c5-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ca9c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9c5-103">Создание нового плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca9c5-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca9c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9c5-106">Создание плана фиксации машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="ca9c5-107">Если в группе ресурсов есть план обязательства с таким же именем, этот звонок действует как операция обновления, и существующий план обязательства перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="ca9c5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca9c5-108">EXAMPLES</span></span>

### <span data-ttu-id="ca9c5-109">--------------------------Пример 1: создание нового плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="ca9c5-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
<span data-ttu-id="ca9c5-110">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ca9c5-110">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="ca9c5-111">Создание нового плана фиксации машинного обучения Azure с именем "MyCommitmentPlanName" в группе "MyResourceGroup" и в Южной Центральной области США.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-111">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="ca9c5-112">В этом примере используется SKU DevTest/Standard, что означает, что ресурсы, предоставленные планом обязательства, будут definied на ограничения DevTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-112">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="ca9c5-113">SkuCapacity в этом примере — это 1, что означает, что стоимость плана будет изменяться стоимостью DevTest, а ресурсы, содержащиеся в плане, будут изменяться в расчете на 1x, на которых DevTest предоставляется.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-113">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="ca9c5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca9c5-114">PARAMETERS</span></span>

### <span data-ttu-id="ca9c5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca9c5-115">-Force</span></span>
<span data-ttu-id="ca9c5-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ca9c5-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ca9c5-117">-Location</span></span>
<span data-ttu-id="ca9c5-118">Расположение плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-118">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca9c5-119">-Name</span></span>
<span data-ttu-id="ca9c5-120">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-120">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca9c5-122">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-122">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ca9c5-123">-SkuCapacity</span></span>
<span data-ttu-id="ca9c5-124">Емкость SKU, используемая при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-124">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ca9c5-125">-SkuName</span></span>
<span data-ttu-id="ca9c5-126">Имя SKU, которое будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-126">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-127">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ca9c5-127">-SkuTier</span></span>
<span data-ttu-id="ca9c5-128">Уровень SKU, который будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-128">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ca9c5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca9c5-129">-Confirm</span></span>
<span data-ttu-id="ca9c5-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9c5-131">-WhatIf</span></span>
<span data-ttu-id="ca9c5-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9c5-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9c5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9c5-134">-DefaultProfile</span></span>
<span data-ttu-id="ca9c5-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca9c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9c5-136">CommonParameters</span></span>
<span data-ttu-id="ca9c5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9c5-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9c5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9c5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca9c5-139">INPUTS</span></span>

## <span data-ttu-id="ca9c5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca9c5-140">OUTPUTS</span></span>

### <span data-ttu-id="ca9c5-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ca9c5-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ca9c5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca9c5-142">NOTES</span></span>
<span data-ttu-id="ca9c5-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ca9c5-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ca9c5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca9c5-144">RELATED LINKS</span></span>

