---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915322"
---
# <span data-ttu-id="9b46b-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="9b46b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b46b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b46b-103">Создание параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b46b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b46b-104">SYNTAX</span></span>

### <span data-ttu-id="9b46b-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b46b-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b46b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b46b-107">DESCRIPTION</span></span>
<span data-ttu-id="9b46b-108">Командлет **Add-AzureRmAutoscaleSetting** создает параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="9b46b-109">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="9b46b-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9b46b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b46b-110">EXAMPLES</span></span>

### <span data-ttu-id="9b46b-111">Пример 1: Создание параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="9b46b-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="9b46b-112">Первые две команды используют New-AzureRmAutoscaleRule для создания двух правил автомасштабирования $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9b46b-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9b46b-113">Третья и четвертая команды используют New-AzureRmAutoscaleProfile для создания профилей автомасштабирования $Profile 1 и $Profile 2 с помощью $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9b46b-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9b46b-114">Последняя команда создает параметр автомасштабирования с помощью профилей в $Profile 1 и $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="9b46b-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="9b46b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b46b-115">PARAMETERS</span></span>

### <span data-ttu-id="9b46b-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9b46b-116">-AutoscaleProfile</span></span>
<span data-ttu-id="9b46b-117">Задает список профилей, которые нужно добавить к параметру автомасштабирования, или $Null, чтобы добавить профиль без профиля.</span><span class="sxs-lookup"><span data-stu-id="9b46b-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b46b-118">-DefaultProfile</span></span>
<span data-ttu-id="9b46b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9b46b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b46b-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-120">-DisableSetting</span></span>
<span data-ttu-id="9b46b-121">Отключение существующего параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b46b-122">-InputObject</span></span>
<span data-ttu-id="9b46b-123">Полный набор спецификаций AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="9b46b-124">-Location</span></span>
<span data-ttu-id="9b46b-125">Задает расположение параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b46b-126">-Name</span></span>
<span data-ttu-id="9b46b-127">Задает имя создаваемого параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-128">-Уведомление</span><span class="sxs-lookup"><span data-stu-id="9b46b-128">-Notification</span></span>
<span data-ttu-id="9b46b-129">Задает список уведомлений с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="9b46b-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b46b-130">-ResourceGroupName</span></span>
<span data-ttu-id="9b46b-131">Указывает имя группы ресурсов для ресурса, связанного с параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9b46b-132">-TargetResourceId</span></span>
<span data-ttu-id="9b46b-133">Указывает идентификатор ресурса для автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b46b-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b46b-134">-Confirm</span></span>
<span data-ttu-id="9b46b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b46b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b46b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b46b-136">-WhatIf</span></span>
<span data-ttu-id="9b46b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b46b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b46b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b46b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b46b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b46b-139">CommonParameters</span></span>
<span data-ttu-id="9b46b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b46b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b46b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b46b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b46b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b46b-142">INPUTS</span></span>

### <span data-ttu-id="9b46b-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="9b46b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9b46b-144">System.String</span></span>

### <span data-ttu-id="9b46b-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b46b-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9b46b-146">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. AutoscaleProfile, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9b46b-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9b46b-147">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. AutoscaleNotification, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9b46b-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9b46b-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b46b-148">OUTPUTS</span></span>

### <span data-ttu-id="9b46b-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9b46b-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="9b46b-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b46b-150">NOTES</span></span>

## <span data-ttu-id="9b46b-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b46b-151">RELATED LINKS</span></span>

[<span data-ttu-id="9b46b-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9b46b-153">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9b46b-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="9b46b-154">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9b46b-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="9b46b-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9b46b-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


