---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224348"
---
# <span data-ttu-id="6b1c9-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b1c9-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="6b1c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1c9-103">Создание или обновление записи конфигурации</span><span class="sxs-lookup"><span data-stu-id="6b1c9-103">Create or Update configuration record</span></span>

## <span data-ttu-id="6b1c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b1c9-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b1c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b1c9-105">DESCRIPTION</span></span>
<span data-ttu-id="6b1c9-106">Создание или обновление записи конфигурации</span><span class="sxs-lookup"><span data-stu-id="6b1c9-106">Create or Update configuration record</span></span>

## <span data-ttu-id="6b1c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b1c9-107">EXAMPLES</span></span>

### <span data-ttu-id="6b1c9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b1c9-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="6b1c9-109">Создание конфигурации обслуживания с областью действия host</span><span class="sxs-lookup"><span data-stu-id="6b1c9-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="6b1c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b1c9-110">PARAMETERS</span></span>

### <span data-ttu-id="6b1c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b1c9-111">-AsJob</span></span>
<span data-ttu-id="6b1c9-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6b1c9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b1c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1c9-113">-DefaultProfile</span></span>
<span data-ttu-id="6b1c9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b1c9-115">-Duration</span><span class="sxs-lookup"><span data-stu-id="6b1c9-115">-Duration</span></span>
<span data-ttu-id="6b1c9-116">Длительность</span><span class="sxs-lookup"><span data-stu-id="6b1c9-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1c9-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="6b1c9-117">-ExpirationDateTime</span></span>
<span data-ttu-id="6b1c9-118">Время окончания срока действия расписания в формате ММ-ММ-ЧЧ:мм</span><span class="sxs-lookup"><span data-stu-id="6b1c9-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="6b1c9-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="6b1c9-119">-ExtensionProperty</span></span>
<span data-ttu-id="6b1c9-120">Свойства расширения для каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="6b1c9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="6b1c9-121">-Location</span></span>
<span data-ttu-id="6b1c9-122">Расположение конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-122">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1c9-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="6b1c9-123">-MaintenanceScope</span></span>
<span data-ttu-id="6b1c9-124">Область обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="6b1c9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6b1c9-125">-Name</span></span>
<span data-ttu-id="6b1c9-126">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-126">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1c9-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="6b1c9-127">-RecurEvery</span></span>
<span data-ttu-id="6b1c9-128">Повторение расписания</span><span class="sxs-lookup"><span data-stu-id="6b1c9-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="6b1c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="6b1c9-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-130">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1c9-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="6b1c9-131">-StartDateTime</span></span>
<span data-ttu-id="6b1c9-132">Время StartDateTime расписания в форматеГГ-ММ-ДД чч:мм</span><span class="sxs-lookup"><span data-stu-id="6b1c9-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="6b1c9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b1c9-133">-Tag</span></span>
<span data-ttu-id="6b1c9-134">Теги ARM.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="6b1c9-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="6b1c9-135">-Timezone</span></span>
<span data-ttu-id="6b1c9-136">Время в поясе</span><span class="sxs-lookup"><span data-stu-id="6b1c9-136">The timezone</span></span>

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

### <span data-ttu-id="6b1c9-137">-Видимость</span><span class="sxs-lookup"><span data-stu-id="6b1c9-137">-Visibility</span></span>
<span data-ttu-id="6b1c9-138">Видимость области</span><span class="sxs-lookup"><span data-stu-id="6b1c9-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="6b1c9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b1c9-139">-Confirm</span></span>
<span data-ttu-id="6b1c9-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1c9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1c9-141">-WhatIf</span></span>
<span data-ttu-id="6b1c9-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1c9-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1c9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1c9-144">CommonParameters</span></span>
<span data-ttu-id="6b1c9-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1c9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1c9-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b1c9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1c9-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b1c9-147">INPUTS</span></span>

### <span data-ttu-id="6b1c9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6b1c9-148">System.String</span></span>

## <span data-ttu-id="6b1c9-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b1c9-149">OUTPUTS</span></span>

### <span data-ttu-id="6b1c9-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b1c9-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="6b1c9-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b1c9-151">NOTES</span></span>

## <span data-ttu-id="6b1c9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b1c9-152">RELATED LINKS</span></span>
