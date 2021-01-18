---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507382"
---
# <span data-ttu-id="28436-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="28436-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="28436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28436-102">SYNOPSIS</span></span>
<span data-ttu-id="28436-103">Создает план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="28436-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="28436-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28436-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28436-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28436-105">DESCRIPTION</span></span>
<span data-ttu-id="28436-106">Создает план обслуживания приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="28436-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="28436-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28436-107">EXAMPLES</span></span>

### <span data-ttu-id="28436-108">Пример 1. Создайте план приложения Windows премиум в Западной Европе с возможностью вспышки в 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="28436-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="28436-109">Эта команда создает план приложения Windows премиум в Западной Европе с возможностью вспышки до 10 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="28436-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="28436-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28436-110">PARAMETERS</span></span>

### <span data-ttu-id="28436-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28436-111">-AsJob</span></span>
<span data-ttu-id="28436-112">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="28436-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="28436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28436-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="28436-114">-Location</span><span class="sxs-lookup"><span data-stu-id="28436-114">-Location</span></span>
<span data-ttu-id="28436-115">Расположение плана потребления.</span><span class="sxs-lookup"><span data-stu-id="28436-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="28436-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="28436-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="28436-117">Максимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="28436-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="28436-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="28436-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="28436-119">Минимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="28436-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="28436-120">-Name</span><span class="sxs-lookup"><span data-stu-id="28436-120">-Name</span></span>
<span data-ttu-id="28436-121">Имя плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="28436-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="28436-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="28436-122">-NoWait</span></span>
<span data-ttu-id="28436-123">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="28436-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="28436-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28436-124">-ResourceGroupName</span></span>
<span data-ttu-id="28436-125">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="28436-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="28436-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="28436-126">-Sku</span></span>
<span data-ttu-id="28436-127">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="28436-127">The plan sku.</span></span>
<span data-ttu-id="28436-128">Допустимые входные данные: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="28436-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="28436-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28436-129">-SubscriptionId</span></span>
<span data-ttu-id="28436-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="28436-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="28436-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="28436-131">-Tag</span></span>
<span data-ttu-id="28436-132">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28436-132">Resource tags.</span></span>

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

### <span data-ttu-id="28436-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="28436-133">-WorkerType</span></span>
<span data-ttu-id="28436-134">Тип сотрудника для плана.</span><span class="sxs-lookup"><span data-stu-id="28436-134">The worker type for the plan.</span></span>
<span data-ttu-id="28436-135">Допустимые входные данные: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="28436-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="28436-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28436-136">-Confirm</span></span>
<span data-ttu-id="28436-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28436-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28436-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28436-138">-WhatIf</span></span>
<span data-ttu-id="28436-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28436-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28436-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="28436-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28436-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28436-141">CommonParameters</span></span>
<span data-ttu-id="28436-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28436-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28436-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28436-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28436-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28436-144">INPUTS</span></span>

## <span data-ttu-id="28436-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28436-145">OUTPUTS</span></span>

### <span data-ttu-id="28436-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="28436-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="28436-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28436-147">NOTES</span></span>

<span data-ttu-id="28436-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="28436-148">ALIASES</span></span>

## <span data-ttu-id="28436-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28436-149">RELATED LINKS</span></span>

