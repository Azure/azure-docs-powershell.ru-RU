---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 465c4b366990bb69d437fbdbe51fe2c5f4316758
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969027"
---
# <span data-ttu-id="d08ab-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="d08ab-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="d08ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d08ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d08ab-103">Создает план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="d08ab-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="d08ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d08ab-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d08ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d08ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d08ab-106">Создает план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="d08ab-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="d08ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d08ab-107">EXAMPLES</span></span>

### <span data-ttu-id="d08ab-108">Пример 1. Создайте план приложения Windows премиум в Западной Европе с возможностью вспышки в 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d08ab-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="d08ab-109">Эта команда создает план приложения Windows премиум в Западной Европе с возможностью вспышки до 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d08ab-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="d08ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d08ab-110">PARAMETERS</span></span>

### <span data-ttu-id="d08ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d08ab-111">-AsJob</span></span>
<span data-ttu-id="d08ab-112">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="d08ab-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="d08ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08ab-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ab-114">-Location</span><span class="sxs-lookup"><span data-stu-id="d08ab-114">-Location</span></span>
<span data-ttu-id="d08ab-115">Расположение плана потребления.</span><span class="sxs-lookup"><span data-stu-id="d08ab-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="d08ab-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="d08ab-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="d08ab-117">Максимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="d08ab-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ab-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="d08ab-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="d08ab-119">Минимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="d08ab-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d08ab-120">-Name</span></span>
<span data-ttu-id="d08ab-121">Имя плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d08ab-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="d08ab-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d08ab-122">-NoWait</span></span>
<span data-ttu-id="d08ab-123">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d08ab-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d08ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="d08ab-125">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d08ab-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="d08ab-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="d08ab-126">-Sku</span></span>
<span data-ttu-id="d08ab-127">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="d08ab-127">The plan sku.</span></span>
<span data-ttu-id="d08ab-128">Допустимые входные данные: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="d08ab-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="d08ab-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d08ab-129">-SubscriptionId</span></span>
<span data-ttu-id="d08ab-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d08ab-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ab-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d08ab-131">-Tag</span></span>
<span data-ttu-id="d08ab-132">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d08ab-132">Resource tags.</span></span>

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

### <span data-ttu-id="d08ab-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="d08ab-133">-WorkerType</span></span>
<span data-ttu-id="d08ab-134">Тип сотрудника для плана.</span><span class="sxs-lookup"><span data-stu-id="d08ab-134">The worker type for the plan.</span></span>
<span data-ttu-id="d08ab-135">Допустимые входные данные: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="d08ab-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="d08ab-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d08ab-136">-Confirm</span></span>
<span data-ttu-id="d08ab-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d08ab-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d08ab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d08ab-138">-WhatIf</span></span>
<span data-ttu-id="d08ab-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d08ab-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d08ab-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d08ab-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d08ab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08ab-141">CommonParameters</span></span>
<span data-ttu-id="d08ab-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08ab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08ab-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d08ab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08ab-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d08ab-144">INPUTS</span></span>

## <span data-ttu-id="d08ab-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d08ab-145">OUTPUTS</span></span>

### <span data-ttu-id="d08ab-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d08ab-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d08ab-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d08ab-147">NOTES</span></span>

<span data-ttu-id="d08ab-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d08ab-148">ALIASES</span></span>

## <span data-ttu-id="d08ab-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d08ab-149">RELATED LINKS</span></span>

