---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076310"
---
# <span data-ttu-id="c5e43-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="c5e43-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="c5e43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5e43-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e43-103">Получает историю для задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="c5e43-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="c5e43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5e43-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e43-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e43-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5e43-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5e43-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c5e43-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c5e43-108">Командлет **Get-AzureSchedulerJobHistory** получает журнал для задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="c5e43-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="c5e43-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5e43-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e43-110">Пример 1: получение журнала для задания с использованием его имени</span><span class="sxs-lookup"><span data-stu-id="c5e43-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="c5e43-111">Эта команда получает историю задания с именем Job01.</span><span class="sxs-lookup"><span data-stu-id="c5e43-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="c5e43-112">Это задание входит в коллекцию заданий с именем JobCollection01 в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="c5e43-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="c5e43-113">Пример 2: получение журнала для невыполненного задания с использованием его имени</span><span class="sxs-lookup"><span data-stu-id="c5e43-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="c5e43-114">Эта команда получает историю задания с именем Job12, которая имеет состояние Failed.</span><span class="sxs-lookup"><span data-stu-id="c5e43-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="c5e43-115">Это задание входит в коллекцию заданий с именем JobCollection01 в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="c5e43-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="c5e43-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5e43-116">PARAMETERS</span></span>

### <span data-ttu-id="c5e43-117">-First</span><span class="sxs-lookup"><span data-stu-id="c5e43-117">-First</span></span>
<span data-ttu-id="c5e43-118">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="c5e43-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="c5e43-119">Введите количество получаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="c5e43-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e43-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c5e43-120">-IncludeTotalCount</span></span>
<span data-ttu-id="c5e43-121">Показывает общее количество объектов в наборе данных (целое число), за которыми следуют выбранные объекты.</span><span class="sxs-lookup"><span data-stu-id="c5e43-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="c5e43-122">Если командлет не может определить общее количество, выводится сообщение "неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="c5e43-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="c5e43-123">Целочисленное значение имеет свойство точности, которое указывает на надежность общего значения Count.</span><span class="sxs-lookup"><span data-stu-id="c5e43-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="c5e43-124">Значение точности в диапазоне от 0,0 до 1,0, где 0,0 означает, что командлет не может подсчитать объекты, 1,0 означает, что счетчик является точным, а значение в диапазоне от 0,0 и 1,0 указывает на то, что все более надежная оценка.</span><span class="sxs-lookup"><span data-stu-id="c5e43-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e43-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c5e43-125">-JobCollectionName</span></span>
<span data-ttu-id="c5e43-126">Указывает имя коллекции заданий планировщика.</span><span class="sxs-lookup"><span data-stu-id="c5e43-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="c5e43-127">Этот командлет получает историю для задания, которое принадлежит к коллекции, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c5e43-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5e43-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="c5e43-128">-JobName</span></span>
<span data-ttu-id="c5e43-129">Указывает имя задания планировщика, для которого требуется получить историю.</span><span class="sxs-lookup"><span data-stu-id="c5e43-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="c5e43-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="c5e43-130">-JobStatus</span></span>
<span data-ttu-id="c5e43-131">Указывает состояние задания планировщика, для которого требуется получить историю.</span><span class="sxs-lookup"><span data-stu-id="c5e43-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="c5e43-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c5e43-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5e43-133">Completed</span><span class="sxs-lookup"><span data-stu-id="c5e43-133">Completed</span></span>
- <span data-ttu-id="c5e43-134">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="c5e43-134">Failed</span></span>

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

### <span data-ttu-id="c5e43-135">-Location</span><span class="sxs-lookup"><span data-stu-id="c5e43-135">-Location</span></span>
<span data-ttu-id="c5e43-136">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="c5e43-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c5e43-137">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="c5e43-137">Valid values are:</span></span> 

- <span data-ttu-id="c5e43-138">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="c5e43-138">Anywhere Asia</span></span>
- <span data-ttu-id="c5e43-139">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="c5e43-139">Anywhere Europe</span></span>
- <span data-ttu-id="c5e43-140">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="c5e43-140">Anywhere US</span></span>
- <span data-ttu-id="c5e43-141">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="c5e43-141">East Asia</span></span>
- <span data-ttu-id="c5e43-142">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="c5e43-142">East US</span></span>
- <span data-ttu-id="c5e43-143">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="c5e43-143">North Central US</span></span>
- <span data-ttu-id="c5e43-144">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="c5e43-144">North Europe</span></span>
- <span data-ttu-id="c5e43-145">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="c5e43-145">South Central US</span></span>
- <span data-ttu-id="c5e43-146">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="c5e43-146">Southeast Asia</span></span>
- <span data-ttu-id="c5e43-147">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="c5e43-147">West Europe</span></span>
- <span data-ttu-id="c5e43-148">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="c5e43-148">West US</span></span>

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

### <span data-ttu-id="c5e43-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="c5e43-149">-Profile</span></span>
<span data-ttu-id="c5e43-150">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c5e43-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5e43-151">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5e43-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5e43-152">-Skip</span><span class="sxs-lookup"><span data-stu-id="c5e43-152">-Skip</span></span>
<span data-ttu-id="c5e43-153">Пропускает указанное количество объектов и возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="c5e43-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="c5e43-154">Введите количество объектов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="c5e43-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e43-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e43-155">CommonParameters</span></span>
<span data-ttu-id="c5e43-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5e43-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e43-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e43-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e43-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5e43-158">INPUTS</span></span>

## <span data-ttu-id="c5e43-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e43-159">OUTPUTS</span></span>

## <span data-ttu-id="c5e43-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5e43-160">NOTES</span></span>

## <span data-ttu-id="c5e43-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5e43-161">RELATED LINKS</span></span>

[<span data-ttu-id="c5e43-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c5e43-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="c5e43-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c5e43-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


