---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226140"
---
# <span data-ttu-id="bf1a9-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="bf1a9-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="bf1a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1a9-103">Создает новую политику моментального снимка azure NetApp Files (ANF) для учетной записи ANF.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="bf1a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf1a9-104">SYNTAX</span></span>

### <span data-ttu-id="bf1a9-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf1a9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf1a9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf1a9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf1a9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf1a9-107">DESCRIPTION</span></span>
<span data-ttu-id="bf1a9-108">Для учетной записи ANF создается новая политика моментального снимка с новыми данными **AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="bf1a9-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="bf1a9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf1a9-109">EXAMPLES</span></span>

### <span data-ttu-id="bf1a9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf1a9-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="bf1a9-111">Эта команда создает новую политику моментального снимка ANF для учетной записи ANF с именем "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="bf1a9-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="bf1a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf1a9-112">PARAMETERS</span></span>

### <span data-ttu-id="bf1a9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf1a9-113">-AccountName</span></span>
<span data-ttu-id="bf1a9-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bf1a9-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="bf1a9-115">-AccountObject</span></span>
<span data-ttu-id="bf1a9-116">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="bf1a9-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="bf1a9-117">-DailySchedule</span></span>
<span data-ttu-id="bf1a9-118">Массив, который представляет ежедневный календарный план</span><span class="sxs-lookup"><span data-stu-id="bf1a9-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1a9-119">-DefaultProfile</span></span>
<span data-ttu-id="bf1a9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf1a9-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="bf1a9-121">-Enabled</span></span>
<span data-ttu-id="bf1a9-122">Свойство, для решаемого, что политика включена или не включена</span><span class="sxs-lookup"><span data-stu-id="bf1a9-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="bf1a9-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="bf1a9-123">-HourlySchedule</span></span>
<span data-ttu-id="bf1a9-124">A hashtable array which represents the hourly Schedule</span><span class="sxs-lookup"><span data-stu-id="bf1a9-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="bf1a9-125">-Location</span></span>
<span data-ttu-id="bf1a9-126">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="bf1a9-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="bf1a9-127">-MonthlySchedule</span></span>
<span data-ttu-id="bf1a9-128">Измеримый массив, представляюща монтно-календарный план</span><span class="sxs-lookup"><span data-stu-id="bf1a9-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bf1a9-129">-Name</span></span>
<span data-ttu-id="bf1a9-130">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="bf1a9-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf1a9-132">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bf1a9-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf1a9-133">-Tag</span></span>
<span data-ttu-id="bf1a9-134">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="bf1a9-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="bf1a9-135">-WeeklySchedule</span></span>
<span data-ttu-id="bf1a9-136">Измеримый массив, представляюща монтно-календарный план</span><span class="sxs-lookup"><span data-stu-id="bf1a9-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1a9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf1a9-137">-Confirm</span></span>
<span data-ttu-id="bf1a9-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1a9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1a9-139">-WhatIf</span></span>
<span data-ttu-id="bf1a9-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1a9-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1a9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1a9-142">CommonParameters</span></span>
<span data-ttu-id="bf1a9-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1a9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1a9-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf1a9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1a9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf1a9-145">INPUTS</span></span>

### <span data-ttu-id="bf1a9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bf1a9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bf1a9-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf1a9-147">OUTPUTS</span></span>

### <span data-ttu-id="bf1a9-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="bf1a9-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="bf1a9-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf1a9-149">NOTES</span></span>

## <span data-ttu-id="bf1a9-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf1a9-150">RELATED LINKS</span></span>
