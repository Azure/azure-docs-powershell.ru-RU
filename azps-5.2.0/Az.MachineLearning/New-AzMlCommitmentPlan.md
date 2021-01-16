---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400823"
---
# <span data-ttu-id="f60e3-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f60e3-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f60e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f60e3-103">Создается новый план обязательств.</span><span class="sxs-lookup"><span data-stu-id="f60e3-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="f60e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f60e3-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60e3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f60e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f60e3-106">Создает план обязательств по машинным обучению Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f60e3-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="f60e3-107">Если в группе ресурсов существует план обязательств с таким же именем, вызов будет выступать в качестве операции обновления, а существующий план обязательств будет перезаписан.</span><span class="sxs-lookup"><span data-stu-id="f60e3-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="f60e3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f60e3-108">EXAMPLES</span></span>

### <span data-ttu-id="f60e3-109">Пример 1. Создание нового плана обязательств</span><span class="sxs-lookup"><span data-stu-id="f60e3-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="f60e3-110">Создание нового плана обязательств по машинным обучению Azure с именем MyCommitmentPlanName в группе MyResourceGroup и регионом Южный Центр США.</span><span class="sxs-lookup"><span data-stu-id="f60e3-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="f60e3-111">В этом примере используется SKU DevTest/Standard, то есть ресурсы, предоставляемые планом обязательств, определяются ограничениями devTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="f60e3-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="f60e3-112">В этом примере SkuCapacity имеет значение 1, то есть стоимость плана будет на 1x стоить devTest, а ресурсы, которые содержит план, будут в 1x больше затрат, чем devTest.</span><span class="sxs-lookup"><span data-stu-id="f60e3-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="f60e3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60e3-113">PARAMETERS</span></span>

### <span data-ttu-id="f60e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60e3-114">-DefaultProfile</span></span>
<span data-ttu-id="f60e3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f60e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f60e3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f60e3-116">-Force</span></span>
<span data-ttu-id="f60e3-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f60e3-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f60e3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="f60e3-118">-Location</span></span>
<span data-ttu-id="f60e3-119">Расположение плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f60e3-120">-Name</span></span>
<span data-ttu-id="f60e3-121">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="f60e3-123">Имя группы ресурсов для плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f60e3-124">-SkuCapacity</span></span>
<span data-ttu-id="f60e3-125">Емкость SKU, используемая при планировании плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f60e3-126">-SkuName</span></span>
<span data-ttu-id="f60e3-127">Имя SKU, используемого при планировании плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f60e3-128">-SkuTier</span></span>
<span data-ttu-id="f60e3-129">Уровень SKU, который используется при планировании плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f60e3-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f60e3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f60e3-130">-Confirm</span></span>
<span data-ttu-id="f60e3-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60e3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60e3-132">-WhatIf</span></span>
<span data-ttu-id="f60e3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60e3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60e3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f60e3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60e3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60e3-135">CommonParameters</span></span>
<span data-ttu-id="f60e3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60e3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60e3-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60e3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60e3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f60e3-138">INPUTS</span></span>

### <span data-ttu-id="f60e3-139">Нет</span><span class="sxs-lookup"><span data-stu-id="f60e3-139">None</span></span>

## <span data-ttu-id="f60e3-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f60e3-140">OUTPUTS</span></span>

### <span data-ttu-id="f60e3-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f60e3-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f60e3-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f60e3-142">NOTES</span></span>
<span data-ttu-id="f60e3-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f60e3-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f60e3-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f60e3-144">RELATED LINKS</span></span>