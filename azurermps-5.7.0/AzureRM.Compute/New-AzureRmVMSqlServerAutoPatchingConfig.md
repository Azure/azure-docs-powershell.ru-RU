---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563692"
---
# <span data-ttu-id="04b0f-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="04b0f-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="04b0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="04b0f-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="04b0f-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04b0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04b0f-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="04b0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="04b0f-106">Командлет **New-AzureVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="04b0f-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="04b0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="04b0f-108">Пример 1: создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="04b0f-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="04b0f-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="04b0f-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="04b0f-110">Команда задает день недели и определяет окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="04b0f-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="04b0f-111">Эта конфигурация включает исправление, использующее эти значения.</span><span class="sxs-lookup"><span data-stu-id="04b0f-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="04b0f-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="04b0f-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="04b0f-113">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="04b0f-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="04b0f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04b0f-114">PARAMETERS</span></span>

### <span data-ttu-id="04b0f-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="04b0f-115">-DayOfWeek</span></span>
<span data-ttu-id="04b0f-116">Указывает день недели, когда необходимо установить обновления.</span><span class="sxs-lookup"><span data-stu-id="04b0f-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="04b0f-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="04b0f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04b0f-118">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="04b0f-118">Sunday</span></span>
- <span data-ttu-id="04b0f-119">Вторник</span><span class="sxs-lookup"><span data-stu-id="04b0f-119">Monday</span></span>
- <span data-ttu-id="04b0f-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="04b0f-120">Tuesday</span></span>
- <span data-ttu-id="04b0f-121">Четверг</span><span class="sxs-lookup"><span data-stu-id="04b0f-121">Wednesday</span></span>
- <span data-ttu-id="04b0f-122">Вторник</span><span class="sxs-lookup"><span data-stu-id="04b0f-122">Thursday</span></span>
- <span data-ttu-id="04b0f-123">Пт</span><span class="sxs-lookup"><span data-stu-id="04b0f-123">Friday</span></span>
- <span data-ttu-id="04b0f-124">Субботам</span><span class="sxs-lookup"><span data-stu-id="04b0f-124">Saturday</span></span>
- <span data-ttu-id="04b0f-125">Жизни</span><span class="sxs-lookup"><span data-stu-id="04b0f-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b0f-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="04b0f-126">-Enable</span></span>
<span data-ttu-id="04b0f-127">Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.</span><span class="sxs-lookup"><span data-stu-id="04b0f-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="04b0f-128">Если вы включите автоматическое исправление, командлет поместит обновление Windows в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="04b0f-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="04b0f-129">Если отключить автоматическое исправление, параметры центра обновления Windows не изменяются.</span><span class="sxs-lookup"><span data-stu-id="04b0f-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b0f-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="04b0f-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="04b0f-131">Указывает продолжительность (в минутах) периода обслуживания.</span><span class="sxs-lookup"><span data-stu-id="04b0f-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="04b0f-132">Автоматическое исправление устраняет выполнение действия, которое может повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="04b0f-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="04b0f-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="04b0f-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b0f-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="04b0f-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="04b0f-135">Указывает час дня, когда запускается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="04b0f-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="04b0f-136">Это время определяет время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="04b0f-136">This time defines when updates start to install.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b0f-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="04b0f-137">-PatchCategory</span></span>
<span data-ttu-id="04b0f-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="04b0f-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b0f-139">CommonParameters</span></span>
<span data-ttu-id="04b0f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04b0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b0f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b0f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b0f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04b0f-142">INPUTS</span></span>

### <span data-ttu-id="04b0f-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="04b0f-143">None</span></span>
<span data-ttu-id="04b0f-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="04b0f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04b0f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b0f-145">OUTPUTS</span></span>

### <span data-ttu-id="04b0f-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="04b0f-146">AutoPatchingSettings</span></span>
<span data-ttu-id="04b0f-147">Этот командлет возвращает объект, содержащий параметры автоматического исправления.</span><span class="sxs-lookup"><span data-stu-id="04b0f-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="04b0f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="04b0f-148">NOTES</span></span>

## <span data-ttu-id="04b0f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04b0f-149">RELATED LINKS</span></span>

[<span data-ttu-id="04b0f-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="04b0f-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="04b0f-151">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="04b0f-151">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


