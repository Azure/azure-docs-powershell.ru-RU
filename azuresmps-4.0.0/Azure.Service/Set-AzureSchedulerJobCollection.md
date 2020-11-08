---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075443"
---
# <span data-ttu-id="bde2f-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bde2f-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="bde2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bde2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bde2f-103">Обновляет коллекцию заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="bde2f-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="bde2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bde2f-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bde2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bde2f-105">DESCRIPTION</span></span>
<span data-ttu-id="bde2f-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bde2f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bde2f-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bde2f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bde2f-108">Командлет **Set-AzureSchedulerJobCollection** обновляет коллекцию заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="bde2f-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="bde2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bde2f-109">EXAMPLES</span></span>

### <span data-ttu-id="bde2f-110">Пример 1: изменение максимального количества заданий для коллекции</span><span class="sxs-lookup"><span data-stu-id="bde2f-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="bde2f-111">Эта команда изменяет максимальное число заданий на 30 в существующей коллекции заданий планировщика с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="bde2f-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="bde2f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bde2f-112">PARAMETERS</span></span>

### <span data-ttu-id="bde2f-113">-Частота</span><span class="sxs-lookup"><span data-stu-id="bde2f-113">-Frequency</span></span>
<span data-ttu-id="bde2f-114">Указывает максимальную частоту, которая может быть указана для любого задания в этой коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="bde2f-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="bde2f-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bde2f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bde2f-116">До</span><span class="sxs-lookup"><span data-stu-id="bde2f-116">Minute</span></span>
- <span data-ttu-id="bde2f-117">Часовой</span><span class="sxs-lookup"><span data-stu-id="bde2f-117">Hour</span></span>
- <span data-ttu-id="bde2f-118">Дневных</span><span class="sxs-lookup"><span data-stu-id="bde2f-118">Day</span></span>
- <span data-ttu-id="bde2f-119">Недели</span><span class="sxs-lookup"><span data-stu-id="bde2f-119">Week</span></span>
- <span data-ttu-id="bde2f-120">Перехода</span><span class="sxs-lookup"><span data-stu-id="bde2f-120">Month</span></span>
- <span data-ttu-id="bde2f-121">Year</span><span class="sxs-lookup"><span data-stu-id="bde2f-121">Year</span></span>

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

### <span data-ttu-id="bde2f-122">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="bde2f-122">-Interval</span></span>
<span data-ttu-id="bde2f-123">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="bde2f-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="bde2f-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bde2f-124">-JobCollectionName</span></span>
<span data-ttu-id="bde2f-125">Указывает имя коллекции заданий планировщика для обновления.</span><span class="sxs-lookup"><span data-stu-id="bde2f-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="bde2f-126">-Location</span><span class="sxs-lookup"><span data-stu-id="bde2f-126">-Location</span></span>
<span data-ttu-id="bde2f-127">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="bde2f-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="bde2f-128">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="bde2f-128">Valid values are:</span></span> 

- <span data-ttu-id="bde2f-129">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="bde2f-129">Anywhere Asia</span></span>
- <span data-ttu-id="bde2f-130">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="bde2f-130">Anywhere Europe</span></span>
- <span data-ttu-id="bde2f-131">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="bde2f-131">Anywhere US</span></span>
- <span data-ttu-id="bde2f-132">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="bde2f-132">East Asia</span></span>
- <span data-ttu-id="bde2f-133">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="bde2f-133">East US</span></span>
- <span data-ttu-id="bde2f-134">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="bde2f-134">North Central US</span></span>
- <span data-ttu-id="bde2f-135">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="bde2f-135">North Europe</span></span>
- <span data-ttu-id="bde2f-136">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="bde2f-136">South Central US</span></span>
- <span data-ttu-id="bde2f-137">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="bde2f-137">Southeast Asia</span></span>
- <span data-ttu-id="bde2f-138">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="bde2f-138">West Europe</span></span>
- <span data-ttu-id="bde2f-139">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="bde2f-139">West US</span></span>

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

### <span data-ttu-id="bde2f-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="bde2f-140">-MaxJobCount</span></span>
<span data-ttu-id="bde2f-141">Указывает максимальное количество заданий, которые можно создать в коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="bde2f-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="bde2f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bde2f-142">-PassThru</span></span>
<span data-ttu-id="bde2f-143">Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.</span><span class="sxs-lookup"><span data-stu-id="bde2f-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="bde2f-144">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bde2f-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bde2f-145">-Планирование</span><span class="sxs-lookup"><span data-stu-id="bde2f-145">-Plan</span></span>
<span data-ttu-id="bde2f-146">Указывает план сбора заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="bde2f-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="bde2f-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="bde2f-147">-Profile</span></span>
<span data-ttu-id="bde2f-148">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bde2f-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bde2f-149">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bde2f-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bde2f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde2f-150">CommonParameters</span></span>
<span data-ttu-id="bde2f-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bde2f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde2f-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde2f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde2f-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bde2f-153">INPUTS</span></span>

## <span data-ttu-id="bde2f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bde2f-154">OUTPUTS</span></span>

## <span data-ttu-id="bde2f-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="bde2f-155">NOTES</span></span>

## <span data-ttu-id="bde2f-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bde2f-156">RELATED LINKS</span></span>

[<span data-ttu-id="bde2f-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bde2f-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="bde2f-158">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bde2f-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="bde2f-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bde2f-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


