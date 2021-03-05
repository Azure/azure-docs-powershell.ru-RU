---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: fa0b8ae9adaca5a187136f068dfd8797ed9e4b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960883"
---
# <span data-ttu-id="3f387-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="3f387-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="3f387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f387-102">SYNOPSIS</span></span>
<span data-ttu-id="3f387-103">Обновление бюджета в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f387-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3f387-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f387-104">SYNTAX</span></span>

### <span data-ttu-id="3f387-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f387-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f387-106">Уведомление</span><span class="sxs-lookup"><span data-stu-id="3f387-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f387-107">Piping</span><span class="sxs-lookup"><span data-stu-id="3f387-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f387-108">Piping and Notification</span><span class="sxs-lookup"><span data-stu-id="3f387-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f387-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f387-109">DESCRIPTION</span></span>
<span data-ttu-id="3f387-110">Новый Set-AzConsumptionBudget обновляет бюджет в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f387-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3f387-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f387-111">EXAMPLES</span></span>

### <span data-ttu-id="3f387-112">Пример 1. Обновление бюджета на новую сумму с названием бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="3f387-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="3f387-113">Пример 2. Обновление бюджета с помощью уведомления, когда затраты или использование достигает порогового значения в 90 процентов от суммы на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="3f387-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="3f387-114">Пример 3. Обновление бюджета на новую сумму с названием бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f387-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="3f387-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f387-115">PARAMETERS</span></span>

### <span data-ttu-id="3f387-116">-Amount</span><span class="sxs-lookup"><span data-stu-id="3f387-116">-Amount</span></span>
<span data-ttu-id="3f387-117">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="3f387-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-118">-Category</span><span class="sxs-lookup"><span data-stu-id="3f387-118">-Category</span></span>
<span data-ttu-id="3f387-119">Категория бюджета может быть затратами или использованием.</span><span class="sxs-lookup"><span data-stu-id="3f387-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="3f387-120">-ContactEmail</span></span>
<span data-ttu-id="3f387-121">Адреса электронной почты для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="3f387-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="3f387-122">-ContactGroup</span></span>
<span data-ttu-id="3f387-123">Группы действий для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="3f387-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="3f387-124">-ContactRole</span></span>
<span data-ttu-id="3f387-125">Роли контактов для отправки бюджетного уведомления о превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="3f387-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f387-126">-DefaultProfile</span></span>
<span data-ttu-id="3f387-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f387-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f387-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3f387-128">-EndDate</span></span>
<span data-ttu-id="3f387-129">Дата окончания (ММ-ММ-ММ в UTC) периода времени для бюджета.</span><span class="sxs-lookup"><span data-stu-id="3f387-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="3f387-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f387-130">-InputObject</span></span>
<span data-ttu-id="3f387-131">Объект «Бюджет».</span><span class="sxs-lookup"><span data-stu-id="3f387-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="3f387-132">-MeterFilter</span></span>
<span data-ttu-id="3f387-133">Разделенный запятой список метров для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3f387-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="3f387-134">Требуется, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="3f387-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="3f387-135">-Name</span><span class="sxs-lookup"><span data-stu-id="3f387-135">-Name</span></span>
<span data-ttu-id="3f387-136">Имя бюджета.</span><span class="sxs-lookup"><span data-stu-id="3f387-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="3f387-137">-NotificationEnabled</span></span>
<span data-ttu-id="3f387-138">Уведомление включено.</span><span class="sxs-lookup"><span data-stu-id="3f387-138">The notification is enabled.</span></span>
<span data-ttu-id="3f387-139">Если не указано, уведомление по умолчанию отключено.</span><span class="sxs-lookup"><span data-stu-id="3f387-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="3f387-140">-NotificationKey</span></span>
<span data-ttu-id="3f387-141">Ключ уведомления, связанного с бюджетом, необходимого для создания уведомления с переключателем с поддержкой уведомлений, порогового значения уведомления, сообщений контактов, групп контактов или ролей контактов.</span><span class="sxs-lookup"><span data-stu-id="3f387-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="3f387-142">-NotificationThreshold</span></span>
<span data-ttu-id="3f387-143">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="3f387-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="3f387-144">Уведомление отправляется, когда затраты или использование превышают пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="3f387-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="3f387-145">Оно всегда является процентом и должно быть вме же от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="3f387-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="3f387-146">-ResourceFilter</span></span>
<span data-ttu-id="3f387-147">Список экземпляров ресурсов, которые нужно отфильтровать, разделенный запятой.</span><span class="sxs-lookup"><span data-stu-id="3f387-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="3f387-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="3f387-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="3f387-149">Список групп ресурсов, разделенных запятой, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="3f387-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="3f387-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f387-150">-ResourceGroupName</span></span>
<span data-ttu-id="3f387-151">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="3f387-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3f387-152">-StartDate</span></span>
<span data-ttu-id="3f387-153">Дата начала (ВДНХ-ММ-ДД в UTC) периода времени для бюджета.</span><span class="sxs-lookup"><span data-stu-id="3f387-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="3f387-154">Не ранее текущего месяца для месячного зерна.</span><span class="sxs-lookup"><span data-stu-id="3f387-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="3f387-155">Не ранее трех месяцев для ежеквартала.</span><span class="sxs-lookup"><span data-stu-id="3f387-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="3f387-156">Не ранее 12 месяцев для ежегодного зерна.</span><span class="sxs-lookup"><span data-stu-id="3f387-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="3f387-157">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="3f387-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="3f387-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="3f387-158">-TimeGrain</span></span>
<span data-ttu-id="3f387-159">Часть бюджета может быть раз в месяц, квартал или ежегодно.</span><span class="sxs-lookup"><span data-stu-id="3f387-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f387-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f387-160">-Confirm</span></span>
<span data-ttu-id="3f387-161">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f387-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f387-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f387-162">-WhatIf</span></span>
<span data-ttu-id="3f387-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f387-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f387-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f387-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f387-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f387-165">CommonParameters</span></span>
<span data-ttu-id="3f387-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f387-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f387-167">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f387-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f387-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f387-168">INPUTS</span></span>

### <span data-ttu-id="3f387-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="3f387-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3f387-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f387-170">OUTPUTS</span></span>

### <span data-ttu-id="3f387-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="3f387-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3f387-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f387-172">NOTES</span></span>

## <span data-ttu-id="3f387-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f387-173">RELATED LINKS</span></span>
