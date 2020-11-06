---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554796"
---
# <span data-ttu-id="72fa1-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="72fa1-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="72fa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="72fa1-103">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="72fa1-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="72fa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72fa1-104">SYNTAX</span></span>

### <span data-ttu-id="72fa1-105">ContainerInstance (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72fa1-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="72fa1-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="72fa1-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="72fa1-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="72fa1-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="72fa1-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="72fa1-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="72fa1-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="72fa1-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="72fa1-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72fa1-110">DESCRIPTION</span></span>
<span data-ttu-id="72fa1-111">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="72fa1-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="72fa1-112">Ознакомьтесь с дополнительными сведениями об этой функции https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="72fa1-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="72fa1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72fa1-113">EXAMPLES</span></span>

### <span data-ttu-id="72fa1-114">Пример 1: запуск добавочной операции копирования по имени BLOB-объектов и времени создания моментального снимка</span><span class="sxs-lookup"><span data-stu-id="72fa1-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="72fa1-115">Эта команда запускает добавочную операцию копирования по имени BLOB-объектов и времени snapshot.</span><span class="sxs-lookup"><span data-stu-id="72fa1-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="72fa1-116">Пример 2: запуск операции добавочного копирования с помощью URI источника</span><span class="sxs-lookup"><span data-stu-id="72fa1-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="72fa1-117">Эта команда запускает операцию добавочного копирования с использованием исходного кода ресурса</span><span class="sxs-lookup"><span data-stu-id="72fa1-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="72fa1-118">Пример 3: запуск операции добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="72fa1-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="72fa1-119">Эта команда запускает операцию добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="72fa1-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="72fa1-120">Пример 4: запуск операции добавочного копирования из объекта CloudPageBlob в конечный BLOB-объект с именем BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="72fa1-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="72fa1-121">Эта команда запускает операцию добавочного копирования из объекта CloudPageBlob в конечный большой двоичный объект с именем BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="72fa1-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="72fa1-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72fa1-122">PARAMETERS</span></span>

### <span data-ttu-id="72fa1-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="72fa1-123">-AbsoluteUri</span></span>
<span data-ttu-id="72fa1-124">Абсолютный URI в источник.</span><span class="sxs-lookup"><span data-stu-id="72fa1-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="72fa1-125">Следует отметить, что учетные данные должны быть указаны в универсальном коде ресурса (URI), если их источник требуется.</span><span class="sxs-lookup"><span data-stu-id="72fa1-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72fa1-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72fa1-127">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="72fa1-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="72fa1-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-128">-CloudBlob</span></span>
<span data-ttu-id="72fa1-129">Объект CloudBlob из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="72fa1-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="72fa1-130">Вы можете создать его или воспользоваться командлетом Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="72fa1-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="72fa1-131">-CloudBlobContainer</span></span>
<span data-ttu-id="72fa1-132">Объект CloudBlobContainer из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="72fa1-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="72fa1-133">Вы можете создать его или воспользоваться командлетом Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="72fa1-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72fa1-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72fa1-135">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="72fa1-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="72fa1-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="72fa1-136">The default value is 10.</span></span>

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

### <span data-ttu-id="72fa1-137">-Context</span><span class="sxs-lookup"><span data-stu-id="72fa1-137">-Context</span></span>
<span data-ttu-id="72fa1-138">Контекст исходного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="72fa1-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="72fa1-139">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="72fa1-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-140">-DestBlob</span></span>
<span data-ttu-id="72fa1-141">Имя целевого BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="72fa1-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-142">-DestCloudBlob</span></span>
<span data-ttu-id="72fa1-143">Конечный объект CloudBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="72fa1-144">-DestContainer</span></span>
<span data-ttu-id="72fa1-145">Имя целевого контейнера</span><span class="sxs-lookup"><span data-stu-id="72fa1-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="72fa1-146">-DestContext</span></span>
<span data-ttu-id="72fa1-147">Контекст целевого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="72fa1-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="72fa1-148">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="72fa1-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72fa1-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72fa1-150">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="72fa1-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="72fa1-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-151">-SrcBlob</span></span>
<span data-ttu-id="72fa1-152">Имя большого двоичного объекта исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="72fa1-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="72fa1-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="72fa1-154">Время моментального снимка BLOB исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="72fa1-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="72fa1-155">-SrcContainer</span></span>
<span data-ttu-id="72fa1-156">Имя исходного контейнера</span><span class="sxs-lookup"><span data-stu-id="72fa1-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72fa1-157">-Confirm</span></span>
<span data-ttu-id="72fa1-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72fa1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fa1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fa1-159">-WhatIf</span></span>
<span data-ttu-id="72fa1-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72fa1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fa1-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72fa1-161">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="72fa1-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72fa1-162">INPUTS</span></span>

### <span data-ttu-id="72fa1-163">Microsoft. WindowsAzure. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="72fa1-164">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer System. String Microsoft. WindowsAzure. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="72fa1-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="72fa1-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72fa1-165">OUTPUTS</span></span>

### <span data-ttu-id="72fa1-166">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="72fa1-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="72fa1-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="72fa1-167">NOTES</span></span>

## <span data-ttu-id="72fa1-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72fa1-168">RELATED LINKS</span></span>

