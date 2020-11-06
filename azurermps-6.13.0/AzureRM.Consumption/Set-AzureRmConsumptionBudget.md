---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/set-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
ms.openlocfilehash: f416a6cef4888e51dfabbc9f34b4afad9dbd7370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568210"
---
# <span data-ttu-id="a1509-101">Set-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="a1509-101">Set-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="a1509-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1509-102">SYNOPSIS</span></span>
<span data-ttu-id="a1509-103">Обновление бюджета либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1509-103">Update a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1509-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1509-104">SYNTAX</span></span>

### <span data-ttu-id="a1509-105">Подписка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1509-105">Subscription (Default)</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1509-106">Извещен</span><span class="sxs-lookup"><span data-stu-id="a1509-106">Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1509-107">Трубодержателей</span><span class="sxs-lookup"><span data-stu-id="a1509-107">Piping</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1509-108">Трубопроводов и уведомления</span><span class="sxs-lookup"><span data-stu-id="a1509-108">Piping and Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1509-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1509-109">DESCRIPTION</span></span>
<span data-ttu-id="a1509-110">Командлет Set-AzureRmConsumptionBudget обновляет бюджет либо в подписке, либо в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1509-110">The Set-AzureRmConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a1509-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1509-111">EXAMPLES</span></span>

### <span data-ttu-id="a1509-112">Пример 1: Обновление бюджета на новую сумму с учетом названия бюджета на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="a1509-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -Amount 75
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

### <span data-ttu-id="a1509-113">Пример 2: Обновление бюджета с уведомлением о том, что стоимость или использование достигает порогового значения 90% от суммы на уровне подписки</span><span class="sxs-lookup"><span data-stu-id="a1509-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
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

### <span data-ttu-id="a1509-114">Пример 3: Обновление бюджета на новую сумму с использованием названия бюджета на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a1509-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
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

## <span data-ttu-id="a1509-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1509-115">PARAMETERS</span></span>

### <span data-ttu-id="a1509-116">-Сумма</span><span class="sxs-lookup"><span data-stu-id="a1509-116">-Amount</span></span>
<span data-ttu-id="a1509-117">Сумма бюджета.</span><span class="sxs-lookup"><span data-stu-id="a1509-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="a1509-118">-Категория</span><span class="sxs-lookup"><span data-stu-id="a1509-118">-Category</span></span>
<span data-ttu-id="a1509-119">Категория бюджета может представлять собой стоимость или использование.</span><span class="sxs-lookup"><span data-stu-id="a1509-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="a1509-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="a1509-120">-ContactEmail</span></span>
<span data-ttu-id="a1509-121">Адреса электронной почты, на которые нужно отправить уведомление о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="a1509-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a1509-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="a1509-122">-ContactGroup</span></span>
<span data-ttu-id="a1509-123">Группы действий для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="a1509-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a1509-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="a1509-124">-ContactRole</span></span>
<span data-ttu-id="a1509-125">Роли контактных лиц для отправки уведомления о бюджете при превышении порогового значения.</span><span class="sxs-lookup"><span data-stu-id="a1509-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a1509-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1509-126">-DefaultProfile</span></span>
<span data-ttu-id="a1509-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1509-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1509-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a1509-128">-EndDate</span></span>
<span data-ttu-id="a1509-129">Дата окончания срока действия бюджета (гггг-мм-дд в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="a1509-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="a1509-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1509-130">-InputObject</span></span>
<span data-ttu-id="a1509-131">Объект бюджета.</span><span class="sxs-lookup"><span data-stu-id="a1509-131">Budget object.</span></span>

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

### <span data-ttu-id="a1509-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="a1509-132">-MeterFilter</span></span>
<span data-ttu-id="a1509-133">Разделенный запятыми список измерительных приборов для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a1509-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="a1509-134">Обязательно, если категория является использованием.</span><span class="sxs-lookup"><span data-stu-id="a1509-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="a1509-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1509-135">-Name</span></span>
<span data-ttu-id="a1509-136">Название бюджета.</span><span class="sxs-lookup"><span data-stu-id="a1509-136">Name of a budget.</span></span>

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

### <span data-ttu-id="a1509-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="a1509-137">-NotificationEnabled</span></span>
<span data-ttu-id="a1509-138">Уведомление включено.</span><span class="sxs-lookup"><span data-stu-id="a1509-138">The notification is enabled.</span></span>
<span data-ttu-id="a1509-139">Если не указано, уведомление отключается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1509-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="a1509-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="a1509-140">-NotificationKey</span></span>
<span data-ttu-id="a1509-141">Ключ уведомления, связанного с бюджетом, необходимый для создания уведомления с параметром включения уведомлений, порога уведомлений, контактами электронной почты, группами контактов и контактными ролями.</span><span class="sxs-lookup"><span data-stu-id="a1509-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="a1509-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="a1509-142">-NotificationThreshold</span></span>
<span data-ttu-id="a1509-143">Пороговое значение, связанное с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="a1509-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="a1509-144">Уведомление отправляется, когда стоимость или использование превысило пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="a1509-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="a1509-145">Он всегда равен проценту и должен находиться в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="a1509-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="a1509-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="a1509-146">-ResourceFilter</span></span>
<span data-ttu-id="a1509-147">Список экземпляров ресурсов, разделенных запятыми, по которым нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="a1509-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="a1509-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="a1509-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="a1509-149">Список групп ресурсов с разделителями-запятыми, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="a1509-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="a1509-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1509-150">-ResourceGroupName</span></span>
<span data-ttu-id="a1509-151">Группа ресурсов бюджета.</span><span class="sxs-lookup"><span data-stu-id="a1509-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="a1509-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a1509-152">-StartDate</span></span>
<span data-ttu-id="a1509-153">Дата начала (гггг-мм-дд в формате UTC) периода бюджета.</span><span class="sxs-lookup"><span data-stu-id="a1509-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="a1509-154">Не до текущего месяца для ежемесячного прокадрового времени.</span><span class="sxs-lookup"><span data-stu-id="a1509-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="a1509-155">Не более чем за три месяца для квартального интервала времени.</span><span class="sxs-lookup"><span data-stu-id="a1509-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="a1509-156">Не более двенадцати месяцев для ежегодных граней.</span><span class="sxs-lookup"><span data-stu-id="a1509-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="a1509-157">Дата начала в будущем не более трех месяцев.</span><span class="sxs-lookup"><span data-stu-id="a1509-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="a1509-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="a1509-158">-TimeGrain</span></span>
<span data-ttu-id="a1509-159">Временные Гранки бюджета могут быть ежемесячными, ежеквартальными и ежегодно.</span><span class="sxs-lookup"><span data-stu-id="a1509-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="a1509-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1509-160">-Confirm</span></span>
<span data-ttu-id="a1509-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1509-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1509-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1509-162">-WhatIf</span></span>
<span data-ttu-id="a1509-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1509-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1509-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1509-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1509-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1509-165">CommonParameters</span></span>
<span data-ttu-id="a1509-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1509-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1509-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1509-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1509-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1509-168">INPUTS</span></span>

### <span data-ttu-id="a1509-169">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="a1509-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="a1509-170">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1509-170">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a1509-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1509-171">OUTPUTS</span></span>

### <span data-ttu-id="a1509-172">Microsoft. Azure. Commands. потребление. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="a1509-172">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="a1509-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1509-173">NOTES</span></span>

## <span data-ttu-id="a1509-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1509-174">RELATED LINKS</span></span>
