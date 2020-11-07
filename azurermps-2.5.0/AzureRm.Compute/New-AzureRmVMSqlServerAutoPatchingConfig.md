---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
ms.openlocfilehash: 1204a8b14cdbb45f46edd2a1ca2e4c12c27845a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914594"
---
# <span data-ttu-id="eb8fb-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="eb8fb-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="eb8fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8fb-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb8fb-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb8fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8fb-106">Командлет **New-AzureRmVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="eb8fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb8fb-107">EXAMPLES</span></span>

### <span data-ttu-id="eb8fb-108">Пример 1: создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="eb8fb-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="eb8fb-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="eb8fb-110">Команда задает день недели и определяет окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="eb8fb-111">Эта конфигурация включает исправление, использующее эти значения.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="eb8fb-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="eb8fb-113">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="eb8fb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb8fb-114">PARAMETERS</span></span>

### <span data-ttu-id="eb8fb-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="eb8fb-115">-DayOfWeek</span></span>
<span data-ttu-id="eb8fb-116">Указывает день недели, когда необходимо установить обновления.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="eb8fb-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb8fb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb8fb-118">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="eb8fb-118">Sunday</span></span>
- <span data-ttu-id="eb8fb-119">Вторник</span><span class="sxs-lookup"><span data-stu-id="eb8fb-119">Monday</span></span>
- <span data-ttu-id="eb8fb-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="eb8fb-120">Tuesday</span></span>
- <span data-ttu-id="eb8fb-121">Четверг</span><span class="sxs-lookup"><span data-stu-id="eb8fb-121">Wednesday</span></span>
- <span data-ttu-id="eb8fb-122">Вторник</span><span class="sxs-lookup"><span data-stu-id="eb8fb-122">Thursday</span></span>
- <span data-ttu-id="eb8fb-123">Пт</span><span class="sxs-lookup"><span data-stu-id="eb8fb-123">Friday</span></span>
- <span data-ttu-id="eb8fb-124">Субботам</span><span class="sxs-lookup"><span data-stu-id="eb8fb-124">Saturday</span></span>
- <span data-ttu-id="eb8fb-125">Жизни</span><span class="sxs-lookup"><span data-stu-id="eb8fb-125">Everyday</span></span>

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

### <span data-ttu-id="eb8fb-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="eb8fb-126">-Enable</span></span>
<span data-ttu-id="eb8fb-127">Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="eb8fb-128">Если вы включите автоматическое исправление, командлет поместит обновление Windows в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="eb8fb-129">Если отключить автоматическое исправление, параметры центра обновления Windows не изменяются.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="eb8fb-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="eb8fb-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="eb8fb-131">Указывает продолжительность (в минутах) периода обслуживания.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="eb8fb-132">Автоматическое исправление устраняет выполнение действия, которое может повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="eb8fb-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="eb8fb-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="eb8fb-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="eb8fb-135">Указывает час дня, когда запускается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="eb8fb-136">Это время определяет время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="eb8fb-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="eb8fb-137">-PatchCategory</span></span>
<span data-ttu-id="eb8fb-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="eb8fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8fb-139">CommonParameters</span></span>
<span data-ttu-id="eb8fb-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8fb-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8fb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8fb-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb8fb-142">INPUTS</span></span>

### <span data-ttu-id="eb8fb-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb8fb-143">None</span></span>
<span data-ttu-id="eb8fb-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb8fb-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8fb-145">OUTPUTS</span></span>

### <span data-ttu-id="eb8fb-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="eb8fb-146">AutoPatchingSettings</span></span>
<span data-ttu-id="eb8fb-147">Этот командлет возвращает объект, содержащий параметры автоматического исправления.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="eb8fb-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb8fb-148">NOTES</span></span>

## <span data-ttu-id="eb8fb-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb8fb-149">RELATED LINKS</span></span>



[<span data-ttu-id="eb8fb-150">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eb8fb-150">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


