---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519571"
---
# <span data-ttu-id="6618e-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="6618e-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="6618e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6618e-102">SYNOPSIS</span></span>
<span data-ttu-id="6618e-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6618e-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="6618e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6618e-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="6618e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6618e-105">DESCRIPTION</span></span>
<span data-ttu-id="6618e-106">Для автоматического исправления на виртуальной машине создается объект конфигурации **new-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="6618e-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="6618e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6618e-107">EXAMPLES</span></span>

### <span data-ttu-id="6618e-108">Пример 1. Создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="6618e-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="6618e-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="6618e-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="6618e-110">Команда определяет день недели и окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6618e-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="6618e-111">Эта конфигурация позволяет исправления, использующие эти значения.</span><span class="sxs-lookup"><span data-stu-id="6618e-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="6618e-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="6618e-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="6618e-113">Вы можете указать этот элемент конфигурации для других Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="6618e-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="6618e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6618e-114">PARAMETERS</span></span>

### <span data-ttu-id="6618e-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="6618e-115">-DayOfWeek</span></span>
<span data-ttu-id="6618e-116">Определяет день недели, когда должны быть установлены обновления.</span><span class="sxs-lookup"><span data-stu-id="6618e-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="6618e-117">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="6618e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6618e-118">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="6618e-118">Sunday</span></span>
- <span data-ttu-id="6618e-119">Понедельник</span><span class="sxs-lookup"><span data-stu-id="6618e-119">Monday</span></span>
- <span data-ttu-id="6618e-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="6618e-120">Tuesday</span></span>
- <span data-ttu-id="6618e-121">Среда</span><span class="sxs-lookup"><span data-stu-id="6618e-121">Wednesday</span></span>
- <span data-ttu-id="6618e-122">Четверг</span><span class="sxs-lookup"><span data-stu-id="6618e-122">Thursday</span></span>
- <span data-ttu-id="6618e-123">Пятница</span><span class="sxs-lookup"><span data-stu-id="6618e-123">Friday</span></span>
- <span data-ttu-id="6618e-124">Суббота</span><span class="sxs-lookup"><span data-stu-id="6618e-124">Saturday</span></span>
- <span data-ttu-id="6618e-125">Каждый день</span><span class="sxs-lookup"><span data-stu-id="6618e-125">Everyday</span></span>

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

### <span data-ttu-id="6618e-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="6618e-126">-Enable</span></span>
<span data-ttu-id="6618e-127">Означает, что включено автоматическое исправление для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6618e-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="6618e-128">Если включить автоматическое исправление, с помощью cmdlet вы сможете переналить Windows Update в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="6618e-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="6618e-129">Если отключить автоматическое исправление, параметры Обновления Windows не изменятся.</span><span class="sxs-lookup"><span data-stu-id="6618e-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="6618e-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="6618e-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="6618e-131">Длительность (в минутах) окна обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6618e-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="6618e-132">Автоматическое исправление не позволяет выполнять действия, которые могут повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="6618e-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="6618e-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="6618e-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="6618e-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="6618e-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="6618e-135">Определяет час, в который день начинается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6618e-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="6618e-136">На этот раз определяется время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="6618e-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="6618e-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="6618e-137">-PatchCategory</span></span>
<span data-ttu-id="6618e-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="6618e-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="6618e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6618e-139">CommonParameters</span></span>
<span data-ttu-id="6618e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6618e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6618e-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6618e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6618e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6618e-142">INPUTS</span></span>

### <span data-ttu-id="6618e-143">Нет</span><span class="sxs-lookup"><span data-stu-id="6618e-143">None</span></span>

## <span data-ttu-id="6618e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6618e-144">OUTPUTS</span></span>

### <span data-ttu-id="6618e-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="6618e-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="6618e-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6618e-146">NOTES</span></span>

## <span data-ttu-id="6618e-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6618e-147">RELATED LINKS</span></span>

[<span data-ttu-id="6618e-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="6618e-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="6618e-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6618e-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


