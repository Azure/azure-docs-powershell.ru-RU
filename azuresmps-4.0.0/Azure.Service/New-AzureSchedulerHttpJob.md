---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075904"
---
# <span data-ttu-id="4bbce-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4bbce-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="4bbce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bbce-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbce-103">Создает задание планировщика с действием HTTP.</span><span class="sxs-lookup"><span data-stu-id="4bbce-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="4bbce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bbce-104">SYNTAX</span></span>

### <span data-ttu-id="4bbce-105">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4bbce-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bbce-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="4bbce-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4bbce-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="4bbce-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4bbce-108">Проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="4bbce-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4bbce-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bbce-109">DESCRIPTION</span></span>
<span data-ttu-id="4bbce-110">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4bbce-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4bbce-111">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4bbce-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4bbce-112">Командлет **New-AzureSchedulerHttpJob** создает задание планировщика с действием HTTP.</span><span class="sxs-lookup"><span data-stu-id="4bbce-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="4bbce-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bbce-113">EXAMPLES</span></span>

### <span data-ttu-id="4bbce-114">Пример 1: Создание HTTP-задания</span><span class="sxs-lookup"><span data-stu-id="4bbce-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="4bbce-115">Эта команда создает HTTP-задание планировщика в коллекции заданий с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="4bbce-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="4bbce-116">Команда задает URI и указывает метод GET в качестве метода.</span><span class="sxs-lookup"><span data-stu-id="4bbce-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="4bbce-117">Пример 2: Создание HTTP-задания для определенного количества запусков</span><span class="sxs-lookup"><span data-stu-id="4bbce-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="4bbce-118">Эта команда создает HTTP-задание планировщика в коллекции заданий с именем JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="4bbce-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="4bbce-119">Команда задает URI и указывает метод GET в качестве метода.</span><span class="sxs-lookup"><span data-stu-id="4bbce-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="4bbce-120">Эта команда запускает задание в течение 20 операций.</span><span class="sxs-lookup"><span data-stu-id="4bbce-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="4bbce-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bbce-121">PARAMETERS</span></span>

### <span data-ttu-id="4bbce-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4bbce-122">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="4bbce-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="4bbce-123">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="4bbce-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4bbce-124">-EndTime</span></span>
<span data-ttu-id="4bbce-125">Задает время в качестве объекта **DateTime** для планировщика, чтобы остановить инициирование заданий.</span><span class="sxs-lookup"><span data-stu-id="4bbce-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="4bbce-126">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="4bbce-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="4bbce-127">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4bbce-127">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="4bbce-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="4bbce-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="4bbce-129">Определяет заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4bbce-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="4bbce-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="4bbce-130">-ErrorActionMethod</span></span>
<span data-ttu-id="4bbce-131">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4bbce-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="4bbce-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4bbce-132">Valid values are:</span></span> 

- <span data-ttu-id="4bbce-133">Получить</span><span class="sxs-lookup"><span data-stu-id="4bbce-133">GET</span></span>
- <span data-ttu-id="4bbce-134">Установка</span><span class="sxs-lookup"><span data-stu-id="4bbce-134">PUT</span></span>
- <span data-ttu-id="4bbce-135">Поместить</span><span class="sxs-lookup"><span data-stu-id="4bbce-135">POST</span></span>
- <span data-ttu-id="4bbce-136">Перейдите</span><span class="sxs-lookup"><span data-stu-id="4bbce-136">HEAD</span></span>
- <span data-ttu-id="4bbce-137">Удаление</span><span class="sxs-lookup"><span data-stu-id="4bbce-137">DELETE</span></span>

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

### <span data-ttu-id="4bbce-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="4bbce-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="4bbce-139">Указывает текст для действий задания хранения.</span><span class="sxs-lookup"><span data-stu-id="4bbce-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="4bbce-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="4bbce-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="4bbce-141">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="4bbce-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="4bbce-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="4bbce-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="4bbce-143">Указывает маркер общего доступа к подписи (SAS) для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="4bbce-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="4bbce-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bbce-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="4bbce-145">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4bbce-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="4bbce-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4bbce-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="4bbce-147">Указывает имя очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="4bbce-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="4bbce-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="4bbce-148">-ErrorActionURI</span></span>
<span data-ttu-id="4bbce-149">Задает универсальный код ресурса (URI) для действия задания с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4bbce-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="4bbce-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4bbce-150">-ExecutionCount</span></span>
<span data-ttu-id="4bbce-151">Указывает число вхождений запущенного задания.</span><span class="sxs-lookup"><span data-stu-id="4bbce-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="4bbce-152">По умолчанию задание повторяется неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="4bbce-152">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4bbce-153">-Частота</span><span class="sxs-lookup"><span data-stu-id="4bbce-153">-Frequency</span></span>
<span data-ttu-id="4bbce-154">Указывает максимальную частоту для этого задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="4bbce-154">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="4bbce-155">-Заголовки</span><span class="sxs-lookup"><span data-stu-id="4bbce-155">-Headers</span></span>
<span data-ttu-id="4bbce-156">Задает заголовки как хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4bbce-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="4bbce-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4bbce-157">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="4bbce-158">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="4bbce-158">-Interval</span></span>
<span data-ttu-id="4bbce-159">Задает интервал повторения с частотой, указанной с помощью параметра *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="4bbce-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="4bbce-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4bbce-160">-JobCollectionName</span></span>
<span data-ttu-id="4bbce-161">Указывает имя коллекции, в которой должно содержаться задание планировщика.</span><span class="sxs-lookup"><span data-stu-id="4bbce-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="4bbce-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="4bbce-162">-JobName</span></span>
<span data-ttu-id="4bbce-163">Указывает имя задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="4bbce-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="4bbce-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="4bbce-164">-JobState</span></span>
<span data-ttu-id="4bbce-165">Указывает состояние задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="4bbce-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="4bbce-166">-Location</span><span class="sxs-lookup"><span data-stu-id="4bbce-166">-Location</span></span>
<span data-ttu-id="4bbce-167">Указывает имя расположения, на котором размещается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="4bbce-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="4bbce-168">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4bbce-168">Valid values are:</span></span> 

- <span data-ttu-id="4bbce-169">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="4bbce-169">Anywhere Asia</span></span>
- <span data-ttu-id="4bbce-170">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="4bbce-170">Anywhere Europe</span></span>
- <span data-ttu-id="4bbce-171">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="4bbce-171">Anywhere US</span></span>
- <span data-ttu-id="4bbce-172">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="4bbce-172">East Asia</span></span>
- <span data-ttu-id="4bbce-173">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="4bbce-173">East US</span></span>
- <span data-ttu-id="4bbce-174">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="4bbce-174">North Central US</span></span>
- <span data-ttu-id="4bbce-175">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="4bbce-175">North Europe</span></span>
- <span data-ttu-id="4bbce-176">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="4bbce-176">South Central US</span></span>
- <span data-ttu-id="4bbce-177">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="4bbce-177">Southeast Asia</span></span>
- <span data-ttu-id="4bbce-178">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="4bbce-178">West Europe</span></span>
- <span data-ttu-id="4bbce-179">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="4bbce-179">West US</span></span>

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

### <span data-ttu-id="4bbce-180">-Method</span><span class="sxs-lookup"><span data-stu-id="4bbce-180">-Method</span></span>
<span data-ttu-id="4bbce-181">Указывает метод для типов действий HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4bbce-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="4bbce-182">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4bbce-182">Valid values are:</span></span> 

- <span data-ttu-id="4bbce-183">Получить</span><span class="sxs-lookup"><span data-stu-id="4bbce-183">GET</span></span>
- <span data-ttu-id="4bbce-184">Установка</span><span class="sxs-lookup"><span data-stu-id="4bbce-184">PUT</span></span>
- <span data-ttu-id="4bbce-185">Поместить</span><span class="sxs-lookup"><span data-stu-id="4bbce-185">POST</span></span>
- <span data-ttu-id="4bbce-186">Перейдите</span><span class="sxs-lookup"><span data-stu-id="4bbce-186">HEAD</span></span>
- <span data-ttu-id="4bbce-187">Удаление</span><span class="sxs-lookup"><span data-stu-id="4bbce-187">DELETE</span></span>

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

### <span data-ttu-id="4bbce-188">-Profile</span><span class="sxs-lookup"><span data-stu-id="4bbce-188">-Profile</span></span>
<span data-ttu-id="4bbce-189">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4bbce-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bbce-190">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bbce-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bbce-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="4bbce-191">-RequestBody</span></span>
<span data-ttu-id="4bbce-192">Задает тело для операций помещения и публикации.</span><span class="sxs-lookup"><span data-stu-id="4bbce-192">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="4bbce-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4bbce-193">-StartTime</span></span>
<span data-ttu-id="4bbce-194">Задает время для начала задания (в виде объекта **DateTime** ).</span><span class="sxs-lookup"><span data-stu-id="4bbce-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="4bbce-195">-URI</span><span class="sxs-lookup"><span data-stu-id="4bbce-195">-URI</span></span>
<span data-ttu-id="4bbce-196">Задает универсальный код ресурса (URI) для действия задания.</span><span class="sxs-lookup"><span data-stu-id="4bbce-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbce-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbce-197">CommonParameters</span></span>
<span data-ttu-id="4bbce-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bbce-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbce-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbce-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbce-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bbce-200">INPUTS</span></span>

## <span data-ttu-id="4bbce-201">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bbce-201">OUTPUTS</span></span>

## <span data-ttu-id="4bbce-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bbce-202">NOTES</span></span>

## <span data-ttu-id="4bbce-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bbce-203">RELATED LINKS</span></span>

[<span data-ttu-id="4bbce-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4bbce-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


