---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075902"
---
# <span data-ttu-id="dde67-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="dde67-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="dde67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dde67-102">SYNOPSIS</span></span>
<span data-ttu-id="dde67-103">Создает задание планировщика с действием хранилища.</span><span class="sxs-lookup"><span data-stu-id="dde67-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="dde67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dde67-104">SYNTAX</span></span>

### <span data-ttu-id="dde67-105">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dde67-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dde67-106">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="dde67-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dde67-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde67-107">DESCRIPTION</span></span>
<span data-ttu-id="dde67-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dde67-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dde67-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dde67-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dde67-110">Командлет **New-AzureSchedulerStorageQueueJob** создает задание планировщика с действием хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dde67-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="dde67-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dde67-111">EXAMPLES</span></span>

### <span data-ttu-id="dde67-112">Пример 1: создание задания хранилища, которое выполняется один раз</span><span class="sxs-lookup"><span data-stu-id="dde67-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="dde67-113">Эта команда создает задание хранилища планировщика в составе коллекции с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="dde67-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="dde67-114">Команда задает учетную запись хранения, имя очереди и маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="dde67-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="dde67-115">Задание запускается один раз сразу.</span><span class="sxs-lookup"><span data-stu-id="dde67-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="dde67-116">Пример 2: создание задания хранилища, которое выполняется указанное количество появлений.</span><span class="sxs-lookup"><span data-stu-id="dde67-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="dde67-117">Эта команда создает задание хранилища планировщика в составе коллекции с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="dde67-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="dde67-118">Команда задает учетную запись хранения, имя очереди и маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="dde67-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="dde67-119">Задание выполняется 20 раз в общее время, дважды каждый час.</span><span class="sxs-lookup"><span data-stu-id="dde67-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="dde67-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dde67-120">PARAMETERS</span></span>

### <span data-ttu-id="dde67-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dde67-121">-EndTime</span></span>
<span data-ttu-id="dde67-122">Задает время в качестве объекта **DateTime** для планировщика, чтобы остановить инициирование задания.</span><span class="sxs-lookup"><span data-stu-id="dde67-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="dde67-123">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="dde67-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="dde67-124">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dde67-124">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="dde67-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="dde67-126">Определяет заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="dde67-126">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="dde67-127">-ErrorActionMethod</span></span>
<span data-ttu-id="dde67-128">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dde67-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="dde67-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="dde67-129">Valid values are:</span></span> 

- <span data-ttu-id="dde67-130">Получить</span><span class="sxs-lookup"><span data-stu-id="dde67-130">GET</span></span>
- <span data-ttu-id="dde67-131">Установка</span><span class="sxs-lookup"><span data-stu-id="dde67-131">PUT</span></span>
- <span data-ttu-id="dde67-132">Поместить</span><span class="sxs-lookup"><span data-stu-id="dde67-132">POST</span></span>
- <span data-ttu-id="dde67-133">Перейдите</span><span class="sxs-lookup"><span data-stu-id="dde67-133">HEAD</span></span>
- <span data-ttu-id="dde67-134">Удаление</span><span class="sxs-lookup"><span data-stu-id="dde67-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="dde67-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="dde67-136">Указывает текст для действий задания хранения.</span><span class="sxs-lookup"><span data-stu-id="dde67-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="dde67-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="dde67-138">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="dde67-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="dde67-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="dde67-140">Указывает маркер общего доступа к подписи (SAS) для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="dde67-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dde67-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="dde67-142">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dde67-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="dde67-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="dde67-144">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="dde67-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="dde67-145">-ErrorActionURI</span></span>
<span data-ttu-id="dde67-146">Задает универсальный код ресурса (URI) для действия задания с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dde67-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="dde67-147">-ExecutionCount</span></span>
<span data-ttu-id="dde67-148">Указывает число вхождений запущенного задания.</span><span class="sxs-lookup"><span data-stu-id="dde67-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="dde67-149">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="dde67-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="dde67-150">-Частота</span><span class="sxs-lookup"><span data-stu-id="dde67-150">-Frequency</span></span>
<span data-ttu-id="dde67-151">Указывает максимальную частоту для этого задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="dde67-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="dde67-152">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="dde67-152">-Interval</span></span>
<span data-ttu-id="dde67-153">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="dde67-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="dde67-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="dde67-154">-JobCollectionName</span></span>
<span data-ttu-id="dde67-155">Указывает имя коллекции, в которой должно содержаться задание планировщика.</span><span class="sxs-lookup"><span data-stu-id="dde67-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="dde67-156">-JobName</span></span>
<span data-ttu-id="dde67-157">Указывает имя задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="dde67-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="dde67-158">-JobState</span></span>
<span data-ttu-id="dde67-159">Указывает состояние задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="dde67-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="dde67-160">-Location</span><span class="sxs-lookup"><span data-stu-id="dde67-160">-Location</span></span>
<span data-ttu-id="dde67-161">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="dde67-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="dde67-162">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="dde67-162">Valid values are:</span></span> 

- <span data-ttu-id="dde67-163">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="dde67-163">Anywhere Asia</span></span>
- <span data-ttu-id="dde67-164">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="dde67-164">Anywhere Europe</span></span>
- <span data-ttu-id="dde67-165">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="dde67-165">Anywhere US</span></span>
- <span data-ttu-id="dde67-166">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="dde67-166">East Asia</span></span>
- <span data-ttu-id="dde67-167">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="dde67-167">East US</span></span>
- <span data-ttu-id="dde67-168">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="dde67-168">North Central US</span></span>
- <span data-ttu-id="dde67-169">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="dde67-169">North Europe</span></span>
- <span data-ttu-id="dde67-170">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="dde67-170">South Central US</span></span>
- <span data-ttu-id="dde67-171">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="dde67-171">Southeast Asia</span></span>
- <span data-ttu-id="dde67-172">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="dde67-172">West Europe</span></span>
- <span data-ttu-id="dde67-173">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="dde67-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-174">-Profile</span><span class="sxs-lookup"><span data-stu-id="dde67-174">-Profile</span></span>
<span data-ttu-id="dde67-175">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dde67-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dde67-176">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dde67-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dde67-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="dde67-177">-SASToken</span></span>
<span data-ttu-id="dde67-178">Указывает маркер SAS для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="dde67-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dde67-179">-StartTime</span></span>
<span data-ttu-id="dde67-180">Задает время для начала задания (в виде объекта **DateTime** ).</span><span class="sxs-lookup"><span data-stu-id="dde67-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="dde67-181">-StorageQueueAccount</span></span>
<span data-ttu-id="dde67-182">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dde67-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="dde67-183">-StorageQueueMessage</span></span>
<span data-ttu-id="dde67-184">Указывает сообщение очереди для задания хранения.</span><span class="sxs-lookup"><span data-stu-id="dde67-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="dde67-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="dde67-185">-StorageQueueName</span></span>
<span data-ttu-id="dde67-186">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="dde67-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde67-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde67-187">CommonParameters</span></span>
<span data-ttu-id="dde67-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dde67-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde67-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde67-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde67-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dde67-190">INPUTS</span></span>

## <span data-ttu-id="dde67-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde67-191">OUTPUTS</span></span>

## <span data-ttu-id="dde67-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="dde67-192">NOTES</span></span>

## <span data-ttu-id="dde67-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dde67-193">RELATED LINKS</span></span>

[<span data-ttu-id="dde67-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="dde67-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


