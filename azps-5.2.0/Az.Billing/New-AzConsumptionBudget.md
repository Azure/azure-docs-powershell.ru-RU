---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400975"
---
# <span data-ttu-id="ff6b2-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="ff6b2-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="ff6b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6b2-103">Создание бюджета в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ff6b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff6b2-104">SYNTAX</span></span>

### <span data-ttu-id="ff6b2-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff6b2-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6b2-106">Уведомление</span><span class="sxs-lookup"><span data-stu-id="ff6b2-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6b2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff6b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ff6b2-108">С New-AzConsumptionBudget или группы ресурсов создается бюджет для подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ff6b2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff6b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ff6b2-110">Пример 1. Создание бюджета затрат с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="ff6b2-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="ff6b2-111">Пример 2. Создание бюджета затрат с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff6b2-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="ff6b2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff6b2-112">PARAMETERS</span></span>

### <span data-ttu-id="ff6b2-113">-Amount</span><span class="sxs-lookup"><span data-stu-id="ff6b2-113">-Amount</span></span>
<span data-ttu-id="ff6b2-114">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="ff6b2-115">-Category</span><span class="sxs-lookup"><span data-stu-id="ff6b2-115">-Category</span></span>
<span data-ttu-id="ff6b2-116">Категория бюджета может быть затратами или использованием.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="ff6b2-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="ff6b2-117">-ContactEmail</span></span>
<span data-ttu-id="ff6b2-118">Адреса электронной почты для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="ff6b2-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="ff6b2-119">-ContactGroup</span></span>
<span data-ttu-id="ff6b2-120">Группы действий для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="ff6b2-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="ff6b2-121">-ContactRole</span></span>
<span data-ttu-id="ff6b2-122">Роли контактов для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="ff6b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6b2-123">-DefaultProfile</span></span>
<span data-ttu-id="ff6b2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff6b2-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ff6b2-125">-EndDate</span></span>
<span data-ttu-id="ff6b2-126">Дата окончания (ММ-ММ-ММ в UTC) периода времени для бюджета.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="ff6b2-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="ff6b2-127">-MeterFilter</span></span>
<span data-ttu-id="ff6b2-128">Разделенный запятой список метров для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="ff6b2-129">Требуется, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="ff6b2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ff6b2-130">-Name</span></span>
<span data-ttu-id="ff6b2-131">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-131">Name of a budget.</span></span>

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

### <span data-ttu-id="ff6b2-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="ff6b2-132">-NotificationEnabled</span></span>
<span data-ttu-id="ff6b2-133">Уведомление включено или не включено.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="ff6b2-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="ff6b2-134">-NotificationKey</span></span>
<span data-ttu-id="ff6b2-135">Ключ уведомления, связанного с бюджетом, который необходим для создания уведомления с переключателем, порогом уведомления, контактными письмами, группами контактов или ролями контактов.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="ff6b2-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="ff6b2-136">-NotificationThreshold</span></span>
<span data-ttu-id="ff6b2-137">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="ff6b2-138">Уведомление отправляется, когда затраты или использование превышают пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="ff6b2-139">Оно всегда является процентом и должно быть вме же от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="ff6b2-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="ff6b2-140">-ResourceFilter</span></span>
<span data-ttu-id="ff6b2-141">Список экземпляров ресурсов, которые нужно отфильтровать, разделенный запятой.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="ff6b2-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="ff6b2-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="ff6b2-143">Список групп ресурсов, разделенных запятой, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="ff6b2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6b2-144">-ResourceGroupName</span></span>
<span data-ttu-id="ff6b2-145">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="ff6b2-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ff6b2-146">-StartDate</span></span>
<span data-ttu-id="ff6b2-147">Дата начала (ВДНХ-ММ-ДД в UTC) периода времени для бюджета.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="ff6b2-148">Не ранее текущего месяца для месячного зерна.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="ff6b2-149">Не ранее трех месяцев для ежеквартала.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="ff6b2-150">Не ранее 12 месяцев для ежегодного зерна.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="ff6b2-151">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="ff6b2-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ff6b2-152">-TimeGrain</span></span>
<span data-ttu-id="ff6b2-153">Часть бюджета может быть раз в месяц, квартал или ежегодно.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="ff6b2-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff6b2-154">-Confirm</span></span>
<span data-ttu-id="ff6b2-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6b2-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6b2-156">-WhatIf</span></span>
<span data-ttu-id="ff6b2-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6b2-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6b2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6b2-159">CommonParameters</span></span>
<span data-ttu-id="ff6b2-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6b2-161">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6b2-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6b2-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff6b2-162">INPUTS</span></span>

### <span data-ttu-id="ff6b2-163">Нет</span><span class="sxs-lookup"><span data-stu-id="ff6b2-163">None</span></span>

## <span data-ttu-id="ff6b2-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff6b2-164">OUTPUTS</span></span>

### <span data-ttu-id="ff6b2-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="ff6b2-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="ff6b2-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff6b2-166">NOTES</span></span>

## <span data-ttu-id="ff6b2-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff6b2-167">RELATED LINKS</span></span>
