---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001736"
---
# <span data-ttu-id="84d33-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="84d33-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="84d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84d33-102">SYNOPSIS</span></span>
<span data-ttu-id="84d33-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="84d33-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="84d33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84d33-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="84d33-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84d33-105">DESCRIPTION</span></span>
<span data-ttu-id="84d33-106">Для автоматического исправления на виртуальной машине создается объект конфигурации **new-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="84d33-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="84d33-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84d33-107">EXAMPLES</span></span>

### <span data-ttu-id="84d33-108">Пример 1. Создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="84d33-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="84d33-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="84d33-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="84d33-110">Команда определяет день недели и окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="84d33-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="84d33-111">Эта конфигурация позволяет исправления, использующие эти значения.</span><span class="sxs-lookup"><span data-stu-id="84d33-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="84d33-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="84d33-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="84d33-113">Вы можете указать этот элемент конфигурации для других Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="84d33-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="84d33-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84d33-114">PARAMETERS</span></span>

### <span data-ttu-id="84d33-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="84d33-115">-DayOfWeek</span></span>
<span data-ttu-id="84d33-116">Определяет день недели, когда должны быть установлены обновления.</span><span class="sxs-lookup"><span data-stu-id="84d33-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="84d33-117">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="84d33-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84d33-118">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="84d33-118">Sunday</span></span>
- <span data-ttu-id="84d33-119">Понедельник</span><span class="sxs-lookup"><span data-stu-id="84d33-119">Monday</span></span>
- <span data-ttu-id="84d33-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="84d33-120">Tuesday</span></span>
- <span data-ttu-id="84d33-121">Среда</span><span class="sxs-lookup"><span data-stu-id="84d33-121">Wednesday</span></span>
- <span data-ttu-id="84d33-122">Четверг</span><span class="sxs-lookup"><span data-stu-id="84d33-122">Thursday</span></span>
- <span data-ttu-id="84d33-123">Пятница</span><span class="sxs-lookup"><span data-stu-id="84d33-123">Friday</span></span>
- <span data-ttu-id="84d33-124">Суббота</span><span class="sxs-lookup"><span data-stu-id="84d33-124">Saturday</span></span>
- <span data-ttu-id="84d33-125">Каждый день</span><span class="sxs-lookup"><span data-stu-id="84d33-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d33-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="84d33-126">-Enable</span></span>
<span data-ttu-id="84d33-127">Означает, что включено автоматическое исправление для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="84d33-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="84d33-128">Если включить автоматическое исправление, с помощью cmdlet вы сможете переналиться в интерактивный режим Windows.</span><span class="sxs-lookup"><span data-stu-id="84d33-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="84d33-129">Если отключить автоматическое исправление, параметры Обновления Windows не изменятся.</span><span class="sxs-lookup"><span data-stu-id="84d33-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="84d33-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="84d33-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="84d33-131">Длительность (в минутах) окна обслуживания.</span><span class="sxs-lookup"><span data-stu-id="84d33-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="84d33-132">Автоматическое исправление позволяет избежать выполнения действий, которые могут повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="84d33-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="84d33-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="84d33-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d33-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="84d33-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="84d33-135">Определяет час, в который день начинается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="84d33-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="84d33-136">Это время определяет, когда начнется установка обновлений.</span><span class="sxs-lookup"><span data-stu-id="84d33-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d33-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="84d33-137">-PatchCategory</span></span>
<span data-ttu-id="84d33-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="84d33-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d33-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d33-139">CommonParameters</span></span>
<span data-ttu-id="84d33-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d33-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d33-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84d33-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d33-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84d33-142">INPUTS</span></span>

### <span data-ttu-id="84d33-143">Нет</span><span class="sxs-lookup"><span data-stu-id="84d33-143">None</span></span>

## <span data-ttu-id="84d33-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84d33-144">OUTPUTS</span></span>

### <span data-ttu-id="84d33-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="84d33-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="84d33-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84d33-146">NOTES</span></span>

## <span data-ttu-id="84d33-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84d33-147">RELATED LINKS</span></span>

[<span data-ttu-id="84d33-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="84d33-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="84d33-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="84d33-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


