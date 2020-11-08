---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076191"
---
# <span data-ttu-id="76763-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="76763-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="76763-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76763-102">SYNOPSIS</span></span>
<span data-ttu-id="76763-103">Создает объект конфигурации для автоматического исправления виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="76763-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="76763-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76763-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76763-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76763-105">DESCRIPTION</span></span>
<span data-ttu-id="76763-106">Командлет **New-AzureVMSqlServerAutoPatchingConfig** создает объект конфигурации для автоматического исправления виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="76763-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="76763-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76763-107">EXAMPLES</span></span>

### <span data-ttu-id="76763-108">Пример 1: создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="76763-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="76763-109">Эта команда создает объект конфигурации, который можно использовать для настройки автоматического исправления с помощью Set-AzureVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="76763-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="76763-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76763-110">PARAMETERS</span></span>

### <span data-ttu-id="76763-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="76763-111">-DayOfWeek</span></span>
<span data-ttu-id="76763-112">Указывает день недели, когда необходимо установить обновления.</span><span class="sxs-lookup"><span data-stu-id="76763-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="76763-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="76763-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76763-114">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="76763-114">Sunday</span></span>
- <span data-ttu-id="76763-115">Вторник</span><span class="sxs-lookup"><span data-stu-id="76763-115">Monday</span></span>
- <span data-ttu-id="76763-116">Вторник</span><span class="sxs-lookup"><span data-stu-id="76763-116">Tuesday</span></span>
- <span data-ttu-id="76763-117">Четверг</span><span class="sxs-lookup"><span data-stu-id="76763-117">Wednesday</span></span>
- <span data-ttu-id="76763-118">Вторник</span><span class="sxs-lookup"><span data-stu-id="76763-118">Thursday</span></span>
- <span data-ttu-id="76763-119">Пт</span><span class="sxs-lookup"><span data-stu-id="76763-119">Friday</span></span>
- <span data-ttu-id="76763-120">Субботам</span><span class="sxs-lookup"><span data-stu-id="76763-120">Saturday</span></span>
- <span data-ttu-id="76763-121">Жизни</span><span class="sxs-lookup"><span data-stu-id="76763-121">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76763-122">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="76763-122">-Enable</span></span>
<span data-ttu-id="76763-123">Указывает на то, что автоматическая установка исправлений для виртуальной машины включена.</span><span class="sxs-lookup"><span data-stu-id="76763-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="76763-124">Если вы включите автоматическое исправление, командлет перейдет в интерактивный режим центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="76763-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="76763-125">Если отключить автоматическое исправление, параметры центра обновления Windows не изменятся.</span><span class="sxs-lookup"><span data-stu-id="76763-125">If you disable automated patching, Windows Update settings will not change.</span></span>

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

### <span data-ttu-id="76763-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76763-126">-InformationAction</span></span>
<span data-ttu-id="76763-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="76763-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76763-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="76763-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76763-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="76763-129">Continue</span></span>
- <span data-ttu-id="76763-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="76763-130">Ignore</span></span>
- <span data-ttu-id="76763-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="76763-131">Inquire</span></span>
- <span data-ttu-id="76763-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76763-132">SilentlyContinue</span></span>
- <span data-ttu-id="76763-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="76763-133">Stop</span></span>
- <span data-ttu-id="76763-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="76763-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76763-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76763-135">-InformationVariable</span></span>
<span data-ttu-id="76763-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="76763-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76763-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="76763-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="76763-138">Указывает длительность периода обслуживания.</span><span class="sxs-lookup"><span data-stu-id="76763-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="76763-139">Автоматическое исправление не позволит выполнить какое-либо действие, которое может повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="76763-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="76763-140">Допускаются только 30 минут.</span><span class="sxs-lookup"><span data-stu-id="76763-140">Only 30 minutes increments are allowed.</span></span>

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

### <span data-ttu-id="76763-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="76763-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="76763-142">Указывает час дня, когда запускается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="76763-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="76763-143">Это время определяет, когда обновления начнут устанавливаться и округляются до часа.</span><span class="sxs-lookup"><span data-stu-id="76763-143">This time defines when updates start installing and is rounded to the hour.</span></span>

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

### <span data-ttu-id="76763-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="76763-144">-PatchCategory</span></span>
<span data-ttu-id="76763-145">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="76763-145">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76763-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76763-146">CommonParameters</span></span>
<span data-ttu-id="76763-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76763-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76763-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76763-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76763-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76763-149">INPUTS</span></span>

## <span data-ttu-id="76763-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76763-150">OUTPUTS</span></span>

### <span data-ttu-id="76763-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="76763-151">AutoPatchingSettings</span></span>
<span data-ttu-id="76763-152">Этот командлет возвращает объект, содержащий параметры автоматического исправления.</span><span class="sxs-lookup"><span data-stu-id="76763-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="76763-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="76763-153">NOTES</span></span>

## <span data-ttu-id="76763-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76763-154">RELATED LINKS</span></span>

[<span data-ttu-id="76763-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="76763-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="76763-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="76763-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="76763-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="76763-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


