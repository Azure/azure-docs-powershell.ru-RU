---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422452"
---
# <span data-ttu-id="6a6df-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6df-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="6a6df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a6df-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6df-103">Обновляет политику моментального снимка azure NetApp Files (ANF) с помощью необязательных модификаторов.</span><span class="sxs-lookup"><span data-stu-id="6a6df-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="6a6df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a6df-104">SYNTAX</span></span>

### <span data-ttu-id="6a6df-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a6df-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6df-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a6df-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6df-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a6df-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6df-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a6df-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a6df-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a6df-109">DESCRIPTION</span></span>
<span data-ttu-id="6a6df-110">Для **обновления-AzNetAppFilesSnapshotPolicy** будет модименовна политика моментального снимка ANF.</span><span class="sxs-lookup"><span data-stu-id="6a6df-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="6a6df-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a6df-111">EXAMPLES</span></span>

### <span data-ttu-id="6a6df-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a6df-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="6a6df-113">Эта команда изменяет политику резервного копирования ANF на "MySnapshotPolicy" на заданный почасовой план.</span><span class="sxs-lookup"><span data-stu-id="6a6df-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="6a6df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a6df-114">PARAMETERS</span></span>

### <span data-ttu-id="6a6df-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a6df-115">-AccountName</span></span>
<span data-ttu-id="6a6df-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6a6df-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6a6df-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6a6df-117">-AccountObject</span></span>
<span data-ttu-id="6a6df-118">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="6a6df-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="6a6df-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="6a6df-119">-DailySchedule</span></span>
<span data-ttu-id="6a6df-120">Массив, который представляет ежедневный календарный план</span><span class="sxs-lookup"><span data-stu-id="6a6df-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6df-121">-DefaultProfile</span></span>
<span data-ttu-id="6a6df-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a6df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6df-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6a6df-123">-Enabled</span></span>
<span data-ttu-id="6a6df-124">Свойство, для решаемого, что политика включена или не включена</span><span class="sxs-lookup"><span data-stu-id="6a6df-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="6a6df-125">-HourlySchedule</span></span>
<span data-ttu-id="6a6df-126">A hashtable array which represents the hourly Schedule</span><span class="sxs-lookup"><span data-stu-id="6a6df-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a6df-127">-InputObject</span></span>
<span data-ttu-id="6a6df-128">Снимок объекта, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="6a6df-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-129">-Location</span><span class="sxs-lookup"><span data-stu-id="6a6df-129">-Location</span></span>
<span data-ttu-id="6a6df-130">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="6a6df-130">The location of the resource</span></span>

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

### <span data-ttu-id="6a6df-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="6a6df-131">-MonthlySchedule</span></span>
<span data-ttu-id="6a6df-132">Измеримый массив, представляюща монтно-календарный план</span><span class="sxs-lookup"><span data-stu-id="6a6df-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6a6df-133">-Name</span></span>
<span data-ttu-id="6a6df-134">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6a6df-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6df-135">-ResourceGroupName</span></span>
<span data-ttu-id="6a6df-136">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6a6df-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6a6df-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a6df-137">-ResourceId</span></span>
<span data-ttu-id="6a6df-138">ИД ресурса политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6a6df-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a6df-139">-Tag</span></span>
<span data-ttu-id="6a6df-140">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="6a6df-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="6a6df-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="6a6df-141">-WeeklySchedule</span></span>
<span data-ttu-id="6a6df-142">Измеримый массив, представляюща монтно-календарный план</span><span class="sxs-lookup"><span data-stu-id="6a6df-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6df-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a6df-143">-Confirm</span></span>
<span data-ttu-id="6a6df-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a6df-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a6df-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a6df-145">-WhatIf</span></span>
<span data-ttu-id="6a6df-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a6df-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a6df-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a6df-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a6df-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6df-148">CommonParameters</span></span>
<span data-ttu-id="6a6df-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6df-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6df-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a6df-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6df-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a6df-151">INPUTS</span></span>

### <span data-ttu-id="6a6df-152">System.String</span><span class="sxs-lookup"><span data-stu-id="6a6df-152">System.String</span></span>

### <span data-ttu-id="6a6df-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6a6df-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6a6df-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6df-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="6a6df-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a6df-155">OUTPUTS</span></span>

### <span data-ttu-id="6a6df-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6df-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="6a6df-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a6df-157">NOTES</span></span>

## <span data-ttu-id="6a6df-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a6df-158">RELATED LINKS</span></span>
