---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: c7acda834cda53a86073692dc6c888ce2803d859
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568382"
---
# <span data-ttu-id="068fc-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="068fc-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="068fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="068fc-102">SYNOPSIS</span></span>
<span data-ttu-id="068fc-103">Передает локальный файл в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="068fc-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="068fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="068fc-104">SYNTAX</span></span>

### <span data-ttu-id="068fc-105">SendManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="068fc-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068fc-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="068fc-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068fc-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="068fc-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="068fc-108">DESCRIPTION</span></span>
<span data-ttu-id="068fc-109">Командлет **Set-AzureStorageBlobContent** отправляет локальный файл в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="068fc-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="068fc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="068fc-110">EXAMPLES</span></span>

### <span data-ttu-id="068fc-111">Пример 1: отправка именованного файла</span><span class="sxs-lookup"><span data-stu-id="068fc-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="068fc-112">Эта команда отправляет файл с именем PlanningData в большой двоичный объект с именем Planning2015.</span><span class="sxs-lookup"><span data-stu-id="068fc-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="068fc-113">Пример 2: отправка всех файлов в текущей папке</span><span class="sxs-lookup"><span data-stu-id="068fc-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="068fc-114">Эта команда использует основной командлет Windows PowerShell, Get-ChildItem для получения всех файлов в текущей папке и во вложенных папках, а затем передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="068fc-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="068fc-115">Командлет **Set-AzureStorageBlobContent** отправляет файлы в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="068fc-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="068fc-116">Пример 3: перезаписать существующий большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="068fc-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="068fc-117">Эта команда получает большой двоичный объект с именем Planning2015 в контейнере ContosoUploads с помощью командлета Get-AzureStorageBlob и передает этот BLOB-объект в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="068fc-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="068fc-118">Команда отправляет файл с именем ContosoPlanning как Planning2015.</span><span class="sxs-lookup"><span data-stu-id="068fc-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="068fc-119">Эта команда не задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="068fc-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="068fc-120">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="068fc-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="068fc-121">Если вы подтвердите команду, командлет перезапишет существующий большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="068fc-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="068fc-122">Пример 4: передача файла в контейнер с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="068fc-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="068fc-123">Эта команда получает контейнер, который начинается со строки ContosoUpload с помощью командлета **Get-AzureStorageContainer** , а затем передает этот BLOB-объект в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="068fc-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="068fc-124">Команда отправляет файл с именем ContosoPlanning как Planning2015.</span><span class="sxs-lookup"><span data-stu-id="068fc-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="068fc-125">Пример 5: Добавление файла в большой двоичный объект на страницу с помощью метаданных и PremiumPageBlobTier в качестве P10</span><span class="sxs-lookup"><span data-stu-id="068fc-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="068fc-126">В первой команде создается хэш-таблица, которая содержит метаданные для большого двоичного объекта, и эта хэш-таблица сохраняется в переменной $Metadata.</span><span class="sxs-lookup"><span data-stu-id="068fc-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="068fc-127">Вторая команда отправляет файл с именем ContosoPlanning в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="068fc-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="068fc-128">Большой двоичный объект включает метаданные, хранящиеся в $Metadata, и имеет PremiumPageBlobTier в качестве P10.</span><span class="sxs-lookup"><span data-stu-id="068fc-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

## <span data-ttu-id="068fc-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="068fc-129">PARAMETERS</span></span>

### <span data-ttu-id="068fc-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="068fc-130">-Blob</span></span>
<span data-ttu-id="068fc-131">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="068fc-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="068fc-132">Этот командлет отправляет файл в большой двоичный объект хранилища Azure, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="068fc-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="068fc-133">-BlobType</span></span>
<span data-ttu-id="068fc-134">Указывает тип большого двоичного объекта, отправляемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="068fc-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="068fc-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="068fc-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="068fc-136">Блокирован</span><span class="sxs-lookup"><span data-stu-id="068fc-136">Block</span></span>
- <span data-ttu-id="068fc-137">Страниц</span><span class="sxs-lookup"><span data-stu-id="068fc-137">Page</span></span>

<span data-ttu-id="068fc-138">Значение по умолчанию — Block.</span><span class="sxs-lookup"><span data-stu-id="068fc-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="068fc-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="068fc-140">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="068fc-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="068fc-141">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="068fc-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="068fc-142">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="068fc-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="068fc-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="068fc-143">-CloudBlob</span></span>
<span data-ttu-id="068fc-144">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="068fc-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="068fc-145">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="068fc-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="068fc-146">-CloudBlobContainer</span></span>
<span data-ttu-id="068fc-147">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="068fc-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="068fc-148">Этот командлет передает содержимое в большой двоичный объект в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="068fc-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="068fc-149">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="068fc-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="068fc-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="068fc-151">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="068fc-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="068fc-152">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="068fc-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="068fc-153">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="068fc-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="068fc-154">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="068fc-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="068fc-155">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="068fc-155">The default value is 10.</span></span>

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

### <span data-ttu-id="068fc-156">-Container</span><span class="sxs-lookup"><span data-stu-id="068fc-156">-Container</span></span>
<span data-ttu-id="068fc-157">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="068fc-157">Specifies the name of a container.</span></span>
<span data-ttu-id="068fc-158">Этот командлет отправляет файл в большой двоичный объект в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="068fc-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-159">-Context</span><span class="sxs-lookup"><span data-stu-id="068fc-159">-Context</span></span>
<span data-ttu-id="068fc-160">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="068fc-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="068fc-161">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="068fc-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-162">-Файл</span><span class="sxs-lookup"><span data-stu-id="068fc-162">-File</span></span>
<span data-ttu-id="068fc-163">Указывает путь к локальному файлу для файла, который нужно отправить как содержимое BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="068fc-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-164">-Force</span><span class="sxs-lookup"><span data-stu-id="068fc-164">-Force</span></span>
<span data-ttu-id="068fc-165">Указывает на то, что этот командлет перезапишет существующий BLOB-объект без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="068fc-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="068fc-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="068fc-166">-Metadata</span></span>
<span data-ttu-id="068fc-167">Задает метаданные для загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="068fc-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-168">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="068fc-168">-PremiumPageBlobTier</span></span>
<span data-ttu-id="068fc-169">Уровень больших двоичных объектов страницы</span><span class="sxs-lookup"><span data-stu-id="068fc-169">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-170">-Свойства</span><span class="sxs-lookup"><span data-stu-id="068fc-170">-Properties</span></span>
<span data-ttu-id="068fc-171">Задает свойства для загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="068fc-171">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-172">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="068fc-172">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="068fc-173">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="068fc-173">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="068fc-174">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="068fc-174">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="068fc-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="068fc-175">-Confirm</span></span>
<span data-ttu-id="068fc-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="068fc-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068fc-177">-WhatIf</span></span>
<span data-ttu-id="068fc-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="068fc-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="068fc-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="068fc-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068fc-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068fc-180">CommonParameters</span></span>
<span data-ttu-id="068fc-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="068fc-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068fc-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="068fc-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068fc-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="068fc-183">INPUTS</span></span>

### <span data-ttu-id="068fc-184">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="068fc-184">IStorageContext</span></span>

<span data-ttu-id="068fc-185">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="068fc-185">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="068fc-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="068fc-186">OUTPUTS</span></span>

### <span data-ttu-id="068fc-187">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="068fc-187">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="068fc-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="068fc-188">NOTES</span></span>

## <span data-ttu-id="068fc-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="068fc-189">RELATED LINKS</span></span>

[<span data-ttu-id="068fc-190">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="068fc-190">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="068fc-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="068fc-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="068fc-192">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="068fc-192">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
