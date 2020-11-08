---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075980"
---
# <span data-ttu-id="b004a-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b004a-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="b004a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b004a-102">SYNOPSIS</span></span>
<span data-ttu-id="b004a-103">Создание коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="b004a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b004a-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b004a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b004a-105">DESCRIPTION</span></span>
<span data-ttu-id="b004a-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b004a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b004a-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b004a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b004a-108">Командлет **New-AzureSchedulerJobCollection** создает коллекцию заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="b004a-109">Если для параметра *плана* не указано значение, командлет создаст стандартную коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="b004a-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="b004a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b004a-110">EXAMPLES</span></span>

### <span data-ttu-id="b004a-111">Пример 1: создание коллекции заданий планировщика, включающей значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b004a-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="b004a-112">Эта команда создает стандартную коллекцию заданий планировщика с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="b004a-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="b004a-113">Для новой коллекции задано количество заданий по умолчанию и максимальное значение повторения для стандартной коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="b004a-114">Пример 2: создание коллекции заданий планировщика с указанными значениями</span><span class="sxs-lookup"><span data-stu-id="b004a-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="b004a-115">Эта команда создает стандартную коллекцию заданий планировщика с именем JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="b004a-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="b004a-116">Для новой коллекции задано максимальное число заданий в 30 рублей и максимальное количество повторений 12 в час.</span><span class="sxs-lookup"><span data-stu-id="b004a-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="b004a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b004a-117">PARAMETERS</span></span>

### <span data-ttu-id="b004a-118">-Частота</span><span class="sxs-lookup"><span data-stu-id="b004a-118">-Frequency</span></span>
<span data-ttu-id="b004a-119">Указывает максимальную частоту, которая может быть указана для любого задания в этой коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

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

### <span data-ttu-id="b004a-120">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="b004a-120">-Interval</span></span>
<span data-ttu-id="b004a-121">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="b004a-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="b004a-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b004a-122">-JobCollectionName</span></span>
<span data-ttu-id="b004a-123">Задает имя для новой коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-123">Specifies the name for the new scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b004a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="b004a-124">-Location</span></span>
<span data-ttu-id="b004a-125">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="b004a-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="b004a-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b004a-126">Valid values are:</span></span> 

- <span data-ttu-id="b004a-127">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="b004a-127">Anywhere Asia</span></span>
- <span data-ttu-id="b004a-128">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="b004a-128">Anywhere Europe</span></span>
- <span data-ttu-id="b004a-129">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="b004a-129">Anywhere US</span></span>
- <span data-ttu-id="b004a-130">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="b004a-130">East Asia</span></span>
- <span data-ttu-id="b004a-131">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="b004a-131">East US</span></span>
- <span data-ttu-id="b004a-132">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="b004a-132">North Central US</span></span>
- <span data-ttu-id="b004a-133">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="b004a-133">North Europe</span></span>
- <span data-ttu-id="b004a-134">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="b004a-134">South Central US</span></span>
- <span data-ttu-id="b004a-135">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="b004a-135">Southeast Asia</span></span>
- <span data-ttu-id="b004a-136">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="b004a-136">West Europe</span></span>
- <span data-ttu-id="b004a-137">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="b004a-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b004a-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="b004a-138">-MaxJobCount</span></span>
<span data-ttu-id="b004a-139">Указывает максимальное количество заданий, которые можно создать в коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="b004a-140">-Планирование</span><span class="sxs-lookup"><span data-stu-id="b004a-140">-Plan</span></span>
<span data-ttu-id="b004a-141">Указывает план сбора заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="b004a-141">Specifies the scheduler job collection plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b004a-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="b004a-142">-Profile</span></span>
<span data-ttu-id="b004a-143">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b004a-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b004a-144">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b004a-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b004a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b004a-145">CommonParameters</span></span>
<span data-ttu-id="b004a-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b004a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b004a-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b004a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b004a-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b004a-148">INPUTS</span></span>

## <span data-ttu-id="b004a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b004a-149">OUTPUTS</span></span>

## <span data-ttu-id="b004a-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="b004a-150">NOTES</span></span>

## <span data-ttu-id="b004a-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b004a-151">RELATED LINKS</span></span>

[<span data-ttu-id="b004a-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b004a-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="b004a-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b004a-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="b004a-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b004a-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


