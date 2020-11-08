---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075799"
---
# <span data-ttu-id="6776a-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6776a-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="6776a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6776a-102">SYNOPSIS</span></span>
<span data-ttu-id="6776a-103">Обновляет задание планировщика, которое имеет действие HTTP.</span><span class="sxs-lookup"><span data-stu-id="6776a-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="6776a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6776a-104">SYNTAX</span></span>

### <span data-ttu-id="6776a-105">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6776a-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6776a-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="6776a-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6776a-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="6776a-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6776a-108">Проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6776a-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6776a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6776a-109">DESCRIPTION</span></span>
<span data-ttu-id="6776a-110">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6776a-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6776a-111">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6776a-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6776a-112">Командлет **Set-AzureSchedulerHttpJob** обновляет задание планировщика, в котором есть действие HTTP.</span><span class="sxs-lookup"><span data-stu-id="6776a-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="6776a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6776a-113">EXAMPLES</span></span>

### <span data-ttu-id="6776a-114">Пример 1: изменение состояния задания на состояние "отключено"</span><span class="sxs-lookup"><span data-stu-id="6776a-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="6776a-115">Эта команда изменяет состояние задания с именем "Job01" на "отключено".</span><span class="sxs-lookup"><span data-stu-id="6776a-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="6776a-116">Это задание входит в коллекцию заданий с именем JobColleciton01 в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="6776a-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="6776a-117">Пример 2: обновление URI задания</span><span class="sxs-lookup"><span data-stu-id="6776a-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="6776a-118">Эта команда обновляет универсальный код ресурса (URI) задания с именем Job01 http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="6776a-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="6776a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6776a-119">PARAMETERS</span></span>

### <span data-ttu-id="6776a-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6776a-120">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="6776a-121">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6776a-122">-EndTime</span></span>
<span data-ttu-id="6776a-123">Задает время в качестве объекта **DateTime** для планировщика, чтобы остановить инициирование заданий.</span><span class="sxs-lookup"><span data-stu-id="6776a-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="6776a-124">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="6776a-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="6776a-125">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6776a-125">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="6776a-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="6776a-127">Определяет заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6776a-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="6776a-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="6776a-128">-ErrorActionMethod</span></span>
<span data-ttu-id="6776a-129">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6776a-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="6776a-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6776a-130">Valid values are:</span></span> 

- <span data-ttu-id="6776a-131">Получить</span><span class="sxs-lookup"><span data-stu-id="6776a-131">GET</span></span>
- <span data-ttu-id="6776a-132">Установка</span><span class="sxs-lookup"><span data-stu-id="6776a-132">PUT</span></span>
- <span data-ttu-id="6776a-133">Поместить</span><span class="sxs-lookup"><span data-stu-id="6776a-133">POST</span></span>
- <span data-ttu-id="6776a-134">Перейдите</span><span class="sxs-lookup"><span data-stu-id="6776a-134">HEAD</span></span>
- <span data-ttu-id="6776a-135">Удаление</span><span class="sxs-lookup"><span data-stu-id="6776a-135">DELETE</span></span>

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

### <span data-ttu-id="6776a-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="6776a-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="6776a-137">Указывает текст для действий задания хранения.</span><span class="sxs-lookup"><span data-stu-id="6776a-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="6776a-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="6776a-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="6776a-139">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="6776a-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="6776a-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="6776a-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="6776a-141">Указывает маркер общего доступа к подписи (SAS) для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6776a-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="6776a-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6776a-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="6776a-143">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6776a-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="6776a-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6776a-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="6776a-145">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="6776a-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="6776a-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="6776a-146">-ErrorActionURI</span></span>
<span data-ttu-id="6776a-147">Задает универсальный код ресурса (URI) для действия задания с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6776a-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="6776a-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="6776a-148">-ExecutionCount</span></span>
<span data-ttu-id="6776a-149">Указывает число вхождений запущенного задания.</span><span class="sxs-lookup"><span data-stu-id="6776a-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="6776a-150">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="6776a-150">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-151">-Частота</span><span class="sxs-lookup"><span data-stu-id="6776a-151">-Frequency</span></span>
<span data-ttu-id="6776a-152">Указывает максимальную частоту для этого задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="6776a-152">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-153">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="6776a-153">-Headers</span></span>
<span data-ttu-id="6776a-154">Задает заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6776a-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="6776a-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="6776a-155">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-156">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="6776a-156">-Interval</span></span>
<span data-ttu-id="6776a-157">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="6776a-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6776a-158">-JobCollectionName</span></span>
<span data-ttu-id="6776a-159">Указывает имя коллекции, содержащей задание планировщика, которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="6776a-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="6776a-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="6776a-160">-JobName</span></span>
<span data-ttu-id="6776a-161">Указывает имя задания планировщика, которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="6776a-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="6776a-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="6776a-162">-JobState</span></span>
<span data-ttu-id="6776a-163">Указывает состояние задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="6776a-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="6776a-164">-Location</span><span class="sxs-lookup"><span data-stu-id="6776a-164">-Location</span></span>
<span data-ttu-id="6776a-165">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="6776a-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="6776a-166">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6776a-166">Valid values are:</span></span> 

- <span data-ttu-id="6776a-167">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="6776a-167">Anywhere Asia</span></span>
- <span data-ttu-id="6776a-168">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="6776a-168">Anywhere Europe</span></span>
- <span data-ttu-id="6776a-169">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="6776a-169">Anywhere US</span></span>
- <span data-ttu-id="6776a-170">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6776a-170">East Asia</span></span>
- <span data-ttu-id="6776a-171">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="6776a-171">East US</span></span>
- <span data-ttu-id="6776a-172">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="6776a-172">North Central US</span></span>
- <span data-ttu-id="6776a-173">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="6776a-173">North Europe</span></span>
- <span data-ttu-id="6776a-174">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="6776a-174">South Central US</span></span>
- <span data-ttu-id="6776a-175">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6776a-175">Southeast Asia</span></span>
- <span data-ttu-id="6776a-176">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="6776a-176">West Europe</span></span>
- <span data-ttu-id="6776a-177">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="6776a-177">West US</span></span>

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

### <span data-ttu-id="6776a-178">-Method</span><span class="sxs-lookup"><span data-stu-id="6776a-178">-Method</span></span>
<span data-ttu-id="6776a-179">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6776a-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="6776a-180">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6776a-180">Valid values are:</span></span> 

- <span data-ttu-id="6776a-181">Получить</span><span class="sxs-lookup"><span data-stu-id="6776a-181">GET</span></span>
- <span data-ttu-id="6776a-182">Установка</span><span class="sxs-lookup"><span data-stu-id="6776a-182">PUT</span></span>
- <span data-ttu-id="6776a-183">Поместить</span><span class="sxs-lookup"><span data-stu-id="6776a-183">POST</span></span>
- <span data-ttu-id="6776a-184">Перейдите</span><span class="sxs-lookup"><span data-stu-id="6776a-184">HEAD</span></span>
- <span data-ttu-id="6776a-185">Удаление</span><span class="sxs-lookup"><span data-stu-id="6776a-185">DELETE</span></span>

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

### <span data-ttu-id="6776a-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6776a-186">-PassThru</span></span>
<span data-ttu-id="6776a-187">Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.</span><span class="sxs-lookup"><span data-stu-id="6776a-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="6776a-188">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6776a-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6776a-189">-Profile</span><span class="sxs-lookup"><span data-stu-id="6776a-189">-Profile</span></span>
<span data-ttu-id="6776a-190">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6776a-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6776a-191">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6776a-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6776a-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="6776a-192">-RequestBody</span></span>
<span data-ttu-id="6776a-193">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="6776a-193">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6776a-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6776a-194">-StartTime</span></span>
<span data-ttu-id="6776a-195">Задает время для начала задания (в виде объекта **DateTime** ).</span><span class="sxs-lookup"><span data-stu-id="6776a-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="6776a-196">-URI</span><span class="sxs-lookup"><span data-stu-id="6776a-196">-URI</span></span>
<span data-ttu-id="6776a-197">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="6776a-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="6776a-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6776a-198">CommonParameters</span></span>
<span data-ttu-id="6776a-199">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6776a-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6776a-200">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6776a-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6776a-201">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6776a-201">INPUTS</span></span>

## <span data-ttu-id="6776a-202">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6776a-202">OUTPUTS</span></span>

## <span data-ttu-id="6776a-203">Пуск</span><span class="sxs-lookup"><span data-stu-id="6776a-203">NOTES</span></span>

## <span data-ttu-id="6776a-204">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6776a-204">RELATED LINKS</span></span>

[<span data-ttu-id="6776a-205">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6776a-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


