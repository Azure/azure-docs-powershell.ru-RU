---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236695"
---
# <span data-ttu-id="267a8-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="267a8-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="267a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="267a8-102">SYNOPSIS</span></span>
<span data-ttu-id="267a8-103">Создает функциональный план служб приложений.</span><span class="sxs-lookup"><span data-stu-id="267a8-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="267a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="267a8-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="267a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="267a8-105">DESCRIPTION</span></span>
<span data-ttu-id="267a8-106">Создает функциональный план служб приложений.</span><span class="sxs-lookup"><span data-stu-id="267a8-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="267a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="267a8-107">EXAMPLES</span></span>

### <span data-ttu-id="267a8-108">Пример 1: создание плана приложений для Windows Premium в Западной Европы с возможностью разбивки на 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="267a8-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="267a8-109">Эта команда создает план приложений для Windows Premium в Западной Европе с возможностью разбивки до 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="267a8-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="267a8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="267a8-110">PARAMETERS</span></span>

### <span data-ttu-id="267a8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="267a8-111">-AsJob</span></span>
<span data-ttu-id="267a8-112">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="267a8-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="267a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267a8-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="267a8-114">-Location</span><span class="sxs-lookup"><span data-stu-id="267a8-114">-Location</span></span>
<span data-ttu-id="267a8-115">Место для плана потребления.</span><span class="sxs-lookup"><span data-stu-id="267a8-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="267a8-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="267a8-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="267a8-117">Максимальное количество рабочих процессов для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="267a8-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="267a8-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="267a8-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="267a8-119">Минимальное количество рабочих процессов для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="267a8-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="267a8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="267a8-120">-Name</span></span>
<span data-ttu-id="267a8-121">Имя плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="267a8-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="267a8-122">-Wait</span><span class="sxs-lookup"><span data-stu-id="267a8-122">-NoWait</span></span>
<span data-ttu-id="267a8-123">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="267a8-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="267a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="267a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="267a8-125">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="267a8-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="267a8-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="267a8-126">-Sku</span></span>
<span data-ttu-id="267a8-127">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="267a8-127">The plan sku.</span></span>
<span data-ttu-id="267a8-128">Допустимые входные значения: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="267a8-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="267a8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="267a8-129">-SubscriptionId</span></span>
<span data-ttu-id="267a8-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="267a8-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="267a8-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="267a8-131">-Tag</span></span>
<span data-ttu-id="267a8-132">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="267a8-132">Resource tags.</span></span>

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

### <span data-ttu-id="267a8-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="267a8-133">-WorkerType</span></span>
<span data-ttu-id="267a8-134">Тип работника для плана.</span><span class="sxs-lookup"><span data-stu-id="267a8-134">The worker type for the plan.</span></span>
<span data-ttu-id="267a8-135">Допустимые входные данные: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="267a8-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="267a8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="267a8-136">-Confirm</span></span>
<span data-ttu-id="267a8-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="267a8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="267a8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="267a8-138">-WhatIf</span></span>
<span data-ttu-id="267a8-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="267a8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="267a8-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="267a8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="267a8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267a8-141">CommonParameters</span></span>
<span data-ttu-id="267a8-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="267a8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267a8-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="267a8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267a8-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="267a8-144">INPUTS</span></span>

## <span data-ttu-id="267a8-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="267a8-145">OUTPUTS</span></span>

### <span data-ttu-id="267a8-146">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="267a8-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="267a8-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="267a8-147">NOTES</span></span>

<span data-ttu-id="267a8-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="267a8-148">ALIASES</span></span>

## <span data-ttu-id="267a8-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="267a8-149">RELATED LINKS</span></span>

