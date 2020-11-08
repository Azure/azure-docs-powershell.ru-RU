---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076311"
---
# <span data-ttu-id="fa158-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="fa158-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="fa158-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa158-102">SYNOPSIS</span></span>
<span data-ttu-id="fa158-103">Возвращает список заданий планировщика или определенного задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="fa158-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="fa158-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa158-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa158-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa158-105">DESCRIPTION</span></span>
<span data-ttu-id="fa158-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa158-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fa158-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fa158-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fa158-108">Командлет **Get-AzureSchedulerJobCollection** возвращает список заданий планировщика или определенного задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="fa158-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="fa158-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa158-109">EXAMPLES</span></span>

### <span data-ttu-id="fa158-110">Пример 1: получение всех заданий в коллекции</span><span class="sxs-lookup"><span data-stu-id="fa158-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="fa158-111">Эта команда получает задания планировщика, являющиеся частью коллекции заданий с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="fa158-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="fa158-112">Пример 2: получение именованного задания</span><span class="sxs-lookup"><span data-stu-id="fa158-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="fa158-113">Эта команда получает задание с именем Job01 из коллекции с именем JobCollection01 в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="fa158-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="fa158-114">Пример 3: получение отключенных заданий в коллекции</span><span class="sxs-lookup"><span data-stu-id="fa158-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="fa158-115">Эта команда получает все отключенные задания планировщика, которые являются частью JobCollection01 в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="fa158-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="fa158-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa158-116">PARAMETERS</span></span>

### <span data-ttu-id="fa158-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fa158-117">-JobCollectionName</span></span>
<span data-ttu-id="fa158-118">Указывает имя коллекции, содержащей задание планировщика, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fa158-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="fa158-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="fa158-119">-JobName</span></span>
<span data-ttu-id="fa158-120">Указывает имя задания планировщика, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fa158-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="fa158-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="fa158-121">-JobState</span></span>
<span data-ttu-id="fa158-122">Указывает состояние заданий планировщика, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="fa158-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="fa158-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa158-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa158-124">Включаем</span><span class="sxs-lookup"><span data-stu-id="fa158-124">Enabled</span></span>
- <span data-ttu-id="fa158-125">Отключает</span><span class="sxs-lookup"><span data-stu-id="fa158-125">Disabled</span></span>
- <span data-ttu-id="fa158-126">Сбой</span><span class="sxs-lookup"><span data-stu-id="fa158-126">Faulted</span></span>
- <span data-ttu-id="fa158-127">Completed</span><span class="sxs-lookup"><span data-stu-id="fa158-127">Completed</span></span>

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

### <span data-ttu-id="fa158-128">-Location</span><span class="sxs-lookup"><span data-stu-id="fa158-128">-Location</span></span>
<span data-ttu-id="fa158-129">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="fa158-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="fa158-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa158-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa158-131">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="fa158-131">Anywhere Asia</span></span>
- <span data-ttu-id="fa158-132">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="fa158-132">Anywhere Europe</span></span>
- <span data-ttu-id="fa158-133">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="fa158-133">Anywhere US</span></span>
- <span data-ttu-id="fa158-134">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="fa158-134">East Asia</span></span>
- <span data-ttu-id="fa158-135">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="fa158-135">East US</span></span>
- <span data-ttu-id="fa158-136">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="fa158-136">North Central US</span></span>
- <span data-ttu-id="fa158-137">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="fa158-137">North Europe</span></span>
- <span data-ttu-id="fa158-138">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="fa158-138">South Central US</span></span>
- <span data-ttu-id="fa158-139">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="fa158-139">Southeast Asia</span></span>
- <span data-ttu-id="fa158-140">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="fa158-140">West Europe</span></span>
- <span data-ttu-id="fa158-141">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="fa158-141">West US</span></span>

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

### <span data-ttu-id="fa158-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="fa158-142">-Profile</span></span>
<span data-ttu-id="fa158-143">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fa158-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa158-144">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa158-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa158-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa158-145">CommonParameters</span></span>
<span data-ttu-id="fa158-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa158-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa158-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa158-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa158-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa158-148">INPUTS</span></span>

## <span data-ttu-id="fa158-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa158-149">OUTPUTS</span></span>

## <span data-ttu-id="fa158-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa158-150">NOTES</span></span>

## <span data-ttu-id="fa158-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa158-151">RELATED LINKS</span></span>

[<span data-ttu-id="fa158-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="fa158-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


