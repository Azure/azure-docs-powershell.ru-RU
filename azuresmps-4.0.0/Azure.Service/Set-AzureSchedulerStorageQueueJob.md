---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076050"
---
# <span data-ttu-id="6e160-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6e160-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="6e160-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e160-102">SYNOPSIS</span></span>
<span data-ttu-id="6e160-103">Обновляет задание планировщика с действием хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="6e160-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e160-104">SYNTAX</span></span>

### <span data-ttu-id="6e160-105">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e160-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6e160-106">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="6e160-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e160-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e160-107">DESCRIPTION</span></span>
<span data-ttu-id="6e160-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e160-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e160-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6e160-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e160-110">Командлет **Set-AzureSchedulerStorageQueueJob** обновляет задание планировщика с действием хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e160-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="6e160-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e160-111">EXAMPLES</span></span>

### <span data-ttu-id="6e160-112">Пример 1: обновление сообщения очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="6e160-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="6e160-113">Эта команда обновляет сообщение очереди для задания хранения с именем Job12.</span><span class="sxs-lookup"><span data-stu-id="6e160-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="6e160-114">Команда задает имя и расположение коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="6e160-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="6e160-115">Пример 2: Включение задания очереди хранилища</span><span class="sxs-lookup"><span data-stu-id="6e160-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="6e160-116">Эта команда включает задание с именем Job16.</span><span class="sxs-lookup"><span data-stu-id="6e160-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="6e160-117">Команда изменяет состояние задания на Enabled, указывая это значение для параметра *JobState* .</span><span class="sxs-lookup"><span data-stu-id="6e160-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="6e160-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e160-118">PARAMETERS</span></span>

### <span data-ttu-id="6e160-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6e160-119">-EndTime</span></span>
<span data-ttu-id="6e160-120">Задает время в качестве объекта **DateTime** для планировщика, чтобы остановить инициирование задания.</span><span class="sxs-lookup"><span data-stu-id="6e160-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="6e160-121">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="6e160-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="6e160-122">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6e160-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="6e160-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="6e160-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="6e160-124">Определяет заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6e160-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="6e160-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="6e160-125">-ErrorActionMethod</span></span>
<span data-ttu-id="6e160-126">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6e160-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="6e160-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6e160-127">Valid values are:</span></span> 

- <span data-ttu-id="6e160-128">Получить</span><span class="sxs-lookup"><span data-stu-id="6e160-128">GET</span></span>
- <span data-ttu-id="6e160-129">Установка</span><span class="sxs-lookup"><span data-stu-id="6e160-129">PUT</span></span>
- <span data-ttu-id="6e160-130">Поместить</span><span class="sxs-lookup"><span data-stu-id="6e160-130">POST</span></span>
- <span data-ttu-id="6e160-131">Перейдите</span><span class="sxs-lookup"><span data-stu-id="6e160-131">HEAD</span></span>
- <span data-ttu-id="6e160-132">Удаление</span><span class="sxs-lookup"><span data-stu-id="6e160-132">DELETE</span></span>

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

### <span data-ttu-id="6e160-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="6e160-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="6e160-134">Указывает текст для действий задания хранения.</span><span class="sxs-lookup"><span data-stu-id="6e160-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="6e160-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="6e160-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="6e160-136">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="6e160-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="6e160-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="6e160-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="6e160-138">Указывает маркер общего доступа к подписи (SAS) для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="6e160-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e160-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="6e160-140">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6e160-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="6e160-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6e160-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="6e160-142">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="6e160-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="6e160-143">-ErrorActionURI</span></span>
<span data-ttu-id="6e160-144">Задает универсальный код ресурса (URI) для действия задания с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6e160-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="6e160-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="6e160-145">-ExecutionCount</span></span>
<span data-ttu-id="6e160-146">Указывает число вхождений запущенного задания.</span><span class="sxs-lookup"><span data-stu-id="6e160-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="6e160-147">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="6e160-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="6e160-148">-Частота</span><span class="sxs-lookup"><span data-stu-id="6e160-148">-Frequency</span></span>
<span data-ttu-id="6e160-149">Указывает максимальную частоту для этого задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="6e160-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="6e160-150">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="6e160-150">-Interval</span></span>
<span data-ttu-id="6e160-151">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="6e160-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="6e160-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6e160-152">-JobCollectionName</span></span>
<span data-ttu-id="6e160-153">Указывает имя коллекции, в которой должно содержаться задание планировщика.</span><span class="sxs-lookup"><span data-stu-id="6e160-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="6e160-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="6e160-154">-JobName</span></span>
<span data-ttu-id="6e160-155">Указывает имя задания планировщика, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="6e160-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="6e160-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="6e160-156">-JobState</span></span>
<span data-ttu-id="6e160-157">Указывает состояние задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="6e160-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="6e160-158">-Location</span><span class="sxs-lookup"><span data-stu-id="6e160-158">-Location</span></span>
<span data-ttu-id="6e160-159">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="6e160-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="6e160-160">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6e160-160">Valid values are:</span></span> 

- <span data-ttu-id="6e160-161">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="6e160-161">Anywhere Asia</span></span>
- <span data-ttu-id="6e160-162">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="6e160-162">Anywhere Europe</span></span>
- <span data-ttu-id="6e160-163">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="6e160-163">Anywhere US</span></span>
- <span data-ttu-id="6e160-164">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6e160-164">East Asia</span></span>
- <span data-ttu-id="6e160-165">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="6e160-165">East US</span></span>
- <span data-ttu-id="6e160-166">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="6e160-166">North Central US</span></span>
- <span data-ttu-id="6e160-167">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="6e160-167">North Europe</span></span>
- <span data-ttu-id="6e160-168">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="6e160-168">South Central US</span></span>
- <span data-ttu-id="6e160-169">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6e160-169">Southeast Asia</span></span>
- <span data-ttu-id="6e160-170">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="6e160-170">West Europe</span></span>
- <span data-ttu-id="6e160-171">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="6e160-171">West US</span></span>

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

### <span data-ttu-id="6e160-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e160-172">-PassThru</span></span>
<span data-ttu-id="6e160-173">Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.</span><span class="sxs-lookup"><span data-stu-id="6e160-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="6e160-174">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6e160-174">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e160-175">-Profile</span><span class="sxs-lookup"><span data-stu-id="6e160-175">-Profile</span></span>
<span data-ttu-id="6e160-176">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6e160-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e160-177">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e160-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e160-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="6e160-178">-SASToken</span></span>
<span data-ttu-id="6e160-179">Указывает маркер SAS для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="6e160-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e160-180">-StartTime</span></span>
<span data-ttu-id="6e160-181">Задает время для начала задания (в виде объекта **DateTime** ).</span><span class="sxs-lookup"><span data-stu-id="6e160-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="6e160-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="6e160-182">-StorageQueueAccount</span></span>
<span data-ttu-id="6e160-183">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6e160-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="6e160-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="6e160-184">-StorageQueueMessage</span></span>
<span data-ttu-id="6e160-185">Указывает сообщение очереди для задания хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="6e160-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="6e160-186">-StorageQueueName</span></span>
<span data-ttu-id="6e160-187">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6e160-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="6e160-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e160-188">CommonParameters</span></span>
<span data-ttu-id="6e160-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e160-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e160-190">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e160-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e160-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e160-191">INPUTS</span></span>

## <span data-ttu-id="6e160-192">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e160-192">OUTPUTS</span></span>

## <span data-ttu-id="6e160-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e160-193">NOTES</span></span>

## <span data-ttu-id="6e160-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e160-194">RELATED LINKS</span></span>

[<span data-ttu-id="6e160-195">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6e160-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


