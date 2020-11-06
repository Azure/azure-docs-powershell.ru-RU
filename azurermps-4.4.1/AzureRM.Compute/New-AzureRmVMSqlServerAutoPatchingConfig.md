---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569627"
---
# <span data-ttu-id="27573-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="27573-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="27573-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27573-102">SYNOPSIS</span></span>
<span data-ttu-id="27573-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="27573-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27573-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27573-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="27573-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27573-105">DESCRIPTION</span></span>
<span data-ttu-id="27573-106">Командлет **New-AzureVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="27573-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="27573-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27573-107">EXAMPLES</span></span>

### <span data-ttu-id="27573-108">Пример 1: создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="27573-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="27573-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="27573-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="27573-110">Команда задает день недели и определяет окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="27573-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="27573-111">Эта конфигурация включает исправление, использующее эти значения.</span><span class="sxs-lookup"><span data-stu-id="27573-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="27573-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="27573-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="27573-113">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="27573-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="27573-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27573-114">PARAMETERS</span></span>

### <span data-ttu-id="27573-115">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="27573-115">-Enable</span></span>
<span data-ttu-id="27573-116">Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.</span><span class="sxs-lookup"><span data-stu-id="27573-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="27573-117">Если вы включите автоматическое исправление, командлет поместит обновление Windows в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="27573-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="27573-118">Если отключить автоматическое исправление, параметры центра обновления Windows не изменяются.</span><span class="sxs-lookup"><span data-stu-id="27573-118">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="27573-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="27573-119">-DayOfWeek</span></span>
<span data-ttu-id="27573-120">Указывает день недели, когда необходимо установить обновления.</span><span class="sxs-lookup"><span data-stu-id="27573-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="27573-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="27573-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27573-122">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="27573-122">Sunday</span></span>
- <span data-ttu-id="27573-123">Вторник</span><span class="sxs-lookup"><span data-stu-id="27573-123">Monday</span></span>
- <span data-ttu-id="27573-124">Вторник</span><span class="sxs-lookup"><span data-stu-id="27573-124">Tuesday</span></span>
- <span data-ttu-id="27573-125">Четверг</span><span class="sxs-lookup"><span data-stu-id="27573-125">Wednesday</span></span>
- <span data-ttu-id="27573-126">Вторник</span><span class="sxs-lookup"><span data-stu-id="27573-126">Thursday</span></span>
- <span data-ttu-id="27573-127">Пт</span><span class="sxs-lookup"><span data-stu-id="27573-127">Friday</span></span>
- <span data-ttu-id="27573-128">Субботам</span><span class="sxs-lookup"><span data-stu-id="27573-128">Saturday</span></span>
- <span data-ttu-id="27573-129">Жизни</span><span class="sxs-lookup"><span data-stu-id="27573-129">Everyday</span></span>

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

### <span data-ttu-id="27573-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="27573-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="27573-131">Указывает час дня, когда запускается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="27573-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="27573-132">Это время определяет время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="27573-132">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="27573-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="27573-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="27573-134">Указывает продолжительность (в минутах) периода обслуживания.</span><span class="sxs-lookup"><span data-stu-id="27573-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="27573-135">Автоматическое исправление устраняет выполнение действия, которое может повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="27573-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="27573-136">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="27573-136">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="27573-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="27573-137">-PatchCategory</span></span>
<span data-ttu-id="27573-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="27573-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="27573-139">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="27573-139">-InformationAction</span></span>
<span data-ttu-id="27573-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="27573-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27573-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="27573-141">-InformationVariable</span></span>
<span data-ttu-id="27573-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="27573-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27573-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27573-143">CommonParameters</span></span>
<span data-ttu-id="27573-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27573-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27573-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27573-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27573-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27573-146">INPUTS</span></span>

## <span data-ttu-id="27573-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27573-147">OUTPUTS</span></span>

### <span data-ttu-id="27573-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="27573-148">AutoPatchingSettings</span></span>
<span data-ttu-id="27573-149">Этот командлет возвращает объект, содержащий параметры автоматического исправления.</span><span class="sxs-lookup"><span data-stu-id="27573-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="27573-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="27573-150">NOTES</span></span>

## <span data-ttu-id="27573-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27573-151">RELATED LINKS</span></span>

[<span data-ttu-id="27573-152">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="27573-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="27573-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="27573-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


