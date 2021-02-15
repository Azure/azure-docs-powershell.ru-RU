---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244232"
---
# <span data-ttu-id="4ced3-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="4ced3-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="4ced3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ced3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ced3-103">Создание бюджета в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ced3-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4ced3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ced3-104">SYNTAX</span></span>

### <span data-ttu-id="4ced3-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ced3-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ced3-106">Уведомление</span><span class="sxs-lookup"><span data-stu-id="4ced3-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ced3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ced3-107">DESCRIPTION</span></span>
<span data-ttu-id="4ced3-108">С New-AzConsumptionBudget или группы ресурсов создается бюджет для подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ced3-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4ced3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ced3-109">EXAMPLES</span></span>

### <span data-ttu-id="4ced3-110">Пример 1. Создание бюджета затрат с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="4ced3-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="4ced3-111">Пример 2. Создание бюджета затрат с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4ced3-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="4ced3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ced3-112">PARAMETERS</span></span>

### <span data-ttu-id="4ced3-113">-Amount</span><span class="sxs-lookup"><span data-stu-id="4ced3-113">-Amount</span></span>
<span data-ttu-id="4ced3-114">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="4ced3-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-115">-Category</span><span class="sxs-lookup"><span data-stu-id="4ced3-115">-Category</span></span>
<span data-ttu-id="4ced3-116">Категория бюджета может быть затратами или использованием.</span><span class="sxs-lookup"><span data-stu-id="4ced3-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="4ced3-117">-ContactEmail</span></span>
<span data-ttu-id="4ced3-118">Адреса электронной почты для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4ced3-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="4ced3-119">-ContactGroup</span></span>
<span data-ttu-id="4ced3-120">Группы действий для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4ced3-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="4ced3-121">-ContactRole</span></span>
<span data-ttu-id="4ced3-122">Роли контактов для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="4ced3-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ced3-123">-DefaultProfile</span></span>
<span data-ttu-id="4ced3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ced3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ced3-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4ced3-125">-EndDate</span></span>
<span data-ttu-id="4ced3-126">Дата окончания периода времени для бюджета (ММ-ММ-ММ в UTC).</span><span class="sxs-lookup"><span data-stu-id="4ced3-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="4ced3-127">-MeterFilter</span></span>
<span data-ttu-id="4ced3-128">Разделенный запятой список метров для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4ced3-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="4ced3-129">Требуется, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="4ced3-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4ced3-130">-Name</span></span>
<span data-ttu-id="4ced3-131">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="4ced3-131">Name of a budget.</span></span>

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

### <span data-ttu-id="4ced3-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="4ced3-132">-NotificationEnabled</span></span>
<span data-ttu-id="4ced3-133">Уведомление включено или не включено.</span><span class="sxs-lookup"><span data-stu-id="4ced3-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="4ced3-134">-NotificationKey</span></span>
<span data-ttu-id="4ced3-135">Ключ уведомления, связанного с бюджетом, необходимого для создания уведомления с переключателем с поддержкой уведомлений, порогового значения уведомления, сообщений контактов, групп контактов или ролей контактов.</span><span class="sxs-lookup"><span data-stu-id="4ced3-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="4ced3-136">-NotificationThreshold</span></span>
<span data-ttu-id="4ced3-137">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="4ced3-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="4ced3-138">Уведомление отправляется, когда затраты или использование превышают пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="4ced3-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="4ced3-139">Оно всегда является процентом и должно быть вме же от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="4ced3-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="4ced3-140">-ResourceFilter</span></span>
<span data-ttu-id="4ced3-141">Список экземпляров ресурсов, которые нужно отфильтровать, разделенный запятой.</span><span class="sxs-lookup"><span data-stu-id="4ced3-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="4ced3-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="4ced3-143">Список групп ресурсов, разделенных запятой, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="4ced3-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ced3-144">-ResourceGroupName</span></span>
<span data-ttu-id="4ced3-145">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="4ced3-145">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4ced3-146">-StartDate</span></span>
<span data-ttu-id="4ced3-147">Дата начала (ВДНХ-ММ-ДД в UTC) периода времени для бюджета.</span><span class="sxs-lookup"><span data-stu-id="4ced3-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="4ced3-148">Не ранее текущего месяца для месячного зерна.</span><span class="sxs-lookup"><span data-stu-id="4ced3-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="4ced3-149">Не ранее трех месяцев для ежеквартала.</span><span class="sxs-lookup"><span data-stu-id="4ced3-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="4ced3-150">Не ранее 12 месяцев для ежегодного зерна.</span><span class="sxs-lookup"><span data-stu-id="4ced3-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="4ced3-151">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="4ced3-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="4ced3-152">-TimeGrain</span></span>
<span data-ttu-id="4ced3-153">Часть бюджета может быть раз в месяц, квартал или ежегодно.</span><span class="sxs-lookup"><span data-stu-id="4ced3-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ced3-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ced3-154">-Confirm</span></span>
<span data-ttu-id="4ced3-155">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4ced3-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ced3-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ced3-156">-WhatIf</span></span>
<span data-ttu-id="4ced3-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ced3-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ced3-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ced3-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ced3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ced3-159">CommonParameters</span></span>
<span data-ttu-id="4ced3-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ced3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ced3-161">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ced3-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ced3-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ced3-162">INPUTS</span></span>

### <span data-ttu-id="4ced3-163">Нет</span><span class="sxs-lookup"><span data-stu-id="4ced3-163">None</span></span>

## <span data-ttu-id="4ced3-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ced3-164">OUTPUTS</span></span>

### <span data-ttu-id="4ced3-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="4ced3-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="4ced3-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ced3-166">NOTES</span></span>

## <span data-ttu-id="4ced3-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ced3-167">RELATED LINKS</span></span>
