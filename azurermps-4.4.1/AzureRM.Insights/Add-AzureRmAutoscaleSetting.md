---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734833"
---
# <span data-ttu-id="a5b09-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a5b09-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="a5b09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b09-103">Создание параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5b09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5b09-104">SYNTAX</span></span>

### <span data-ttu-id="a5b09-105">Параметры для Add-AzureRmAutoscaleSetting командлета в семантике обновления</span><span class="sxs-lookup"><span data-stu-id="a5b09-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5b09-106">Параметры для Add-AzureRmAutoscaleSetting командлета в семантике создания</span><span class="sxs-lookup"><span data-stu-id="a5b09-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5b09-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b09-107">DESCRIPTION</span></span>
<span data-ttu-id="a5b09-108">Командлет **Add-AzureRmAutoscaleSetting** создает параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="a5b09-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b09-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b09-110">Пример 1: Создание параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="a5b09-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="a5b09-111">Первые две команды используют New-AzureRmAutoscaleRule для создания двух правил автомасштабирования $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="a5b09-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="a5b09-112">Третья и четвертая команды используют New-AzureRmAutoscaleProfile для создания профилей автомасштабирования $Profile 1 и $Profile 2 с помощью $Rule 1 и $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="a5b09-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="a5b09-113">Последняя команда создает параметр автомасштабирования с помощью профилей в $Profile 1 и $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="a5b09-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="a5b09-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b09-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b09-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="a5b09-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="a5b09-116">Задает список профилей, которые нужно добавить к параметру автомасштабирования, или $Null, чтобы добавить профиль без профиля.</span><span class="sxs-lookup"><span data-stu-id="a5b09-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="a5b09-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="a5b09-117">-DisableSetting</span></span>
<span data-ttu-id="a5b09-118">Отключение существующего параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="a5b09-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a5b09-119">-Location</span></span>
<span data-ttu-id="a5b09-120">Задает расположение параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b09-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5b09-121">-Name</span></span>
<span data-ttu-id="a5b09-122">Задает имя создаваемого параметра автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b09-123">-Уведомления</span><span class="sxs-lookup"><span data-stu-id="a5b09-123">-Notifications</span></span>
<span data-ttu-id="a5b09-124">Задает список уведомлений с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="a5b09-124">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="a5b09-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5b09-125">-ResourceGroup</span></span>
<span data-ttu-id="a5b09-126">Указывает имя группы ресурсов для ресурса, связанного с параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b09-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="a5b09-127">-SettingSpec</span></span>
<span data-ttu-id="a5b09-128">Указывает объект **AutoscaleSetting** .</span><span class="sxs-lookup"><span data-stu-id="a5b09-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="a5b09-129">Чтобы получить объект **AutoscaleSetting** , можно использовать командлет Get-AzureRmAutoscaleSetting или создать его в сценарии Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5b09-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b09-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b09-130">-TargetResourceId</span></span>
<span data-ttu-id="a5b09-131">Указывает идентификатор ресурса для автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="a5b09-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b09-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b09-132">-DefaultProfile</span></span>
<span data-ttu-id="a5b09-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b09-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5b09-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b09-134">CommonParameters</span></span>
<span data-ttu-id="a5b09-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5b09-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b09-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b09-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b09-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5b09-137">INPUTS</span></span>

## <span data-ttu-id="a5b09-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b09-138">OUTPUTS</span></span>

### <span data-ttu-id="a5b09-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a5b09-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="a5b09-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5b09-140">NOTES</span></span>

## <span data-ttu-id="a5b09-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b09-141">RELATED LINKS</span></span>

[<span data-ttu-id="a5b09-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a5b09-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="a5b09-143">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a5b09-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="a5b09-144">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="a5b09-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="a5b09-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a5b09-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


