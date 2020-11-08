---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245728"
---
# <span data-ttu-id="4e236-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="4e236-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="4e236-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e236-102">SYNOPSIS</span></span>
<span data-ttu-id="4e236-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4e236-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="4e236-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e236-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="4e236-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e236-105">DESCRIPTION</span></span>
<span data-ttu-id="4e236-106">Командлет **New-AzVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4e236-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="4e236-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e236-107">EXAMPLES</span></span>

### <span data-ttu-id="4e236-108">Пример 1: создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="4e236-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="4e236-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="4e236-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="4e236-110">Команда задает день недели и определяет окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4e236-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="4e236-111">Эта конфигурация включает исправление, использующее эти значения.</span><span class="sxs-lookup"><span data-stu-id="4e236-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="4e236-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="4e236-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="4e236-113">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="4e236-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="4e236-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e236-114">PARAMETERS</span></span>

### <span data-ttu-id="4e236-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="4e236-115">-DayOfWeek</span></span>
<span data-ttu-id="4e236-116">Указывает день недели, когда необходимо установить обновления.</span><span class="sxs-lookup"><span data-stu-id="4e236-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="4e236-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4e236-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e236-118">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="4e236-118">Sunday</span></span>
- <span data-ttu-id="4e236-119">Вторник</span><span class="sxs-lookup"><span data-stu-id="4e236-119">Monday</span></span>
- <span data-ttu-id="4e236-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="4e236-120">Tuesday</span></span>
- <span data-ttu-id="4e236-121">Четверг</span><span class="sxs-lookup"><span data-stu-id="4e236-121">Wednesday</span></span>
- <span data-ttu-id="4e236-122">Вторник</span><span class="sxs-lookup"><span data-stu-id="4e236-122">Thursday</span></span>
- <span data-ttu-id="4e236-123">Пт</span><span class="sxs-lookup"><span data-stu-id="4e236-123">Friday</span></span>
- <span data-ttu-id="4e236-124">Субботам</span><span class="sxs-lookup"><span data-stu-id="4e236-124">Saturday</span></span>
- <span data-ttu-id="4e236-125">Жизни</span><span class="sxs-lookup"><span data-stu-id="4e236-125">Everyday</span></span>

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

### <span data-ttu-id="4e236-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="4e236-126">-Enable</span></span>
<span data-ttu-id="4e236-127">Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.</span><span class="sxs-lookup"><span data-stu-id="4e236-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="4e236-128">Если вы включите автоматическое исправление, командлет поместит обновление Windows в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="4e236-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="4e236-129">Если отключить автоматическое исправление, параметры центра обновления Windows не изменяются.</span><span class="sxs-lookup"><span data-stu-id="4e236-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="4e236-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="4e236-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="4e236-131">Указывает продолжительность (в минутах) периода обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4e236-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="4e236-132">Автоматическое исправление устраняет выполнение действия, которое может повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="4e236-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="4e236-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="4e236-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="4e236-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="4e236-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="4e236-135">Указывает час дня, когда запускается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4e236-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="4e236-136">Это время определяет время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="4e236-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="4e236-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="4e236-137">-PatchCategory</span></span>
<span data-ttu-id="4e236-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="4e236-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="4e236-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e236-139">CommonParameters</span></span>
<span data-ttu-id="4e236-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e236-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e236-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e236-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e236-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e236-142">INPUTS</span></span>

### <span data-ttu-id="4e236-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e236-143">None</span></span>

## <span data-ttu-id="4e236-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e236-144">OUTPUTS</span></span>

### <span data-ttu-id="4e236-145">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="4e236-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="4e236-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e236-146">NOTES</span></span>

## <span data-ttu-id="4e236-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e236-147">RELATED LINKS</span></span>

[<span data-ttu-id="4e236-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="4e236-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="4e236-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4e236-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


