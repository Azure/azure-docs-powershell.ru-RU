---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318317"
---
# <span data-ttu-id="75032-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="75032-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="75032-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75032-102">SYNOPSIS</span></span>
<span data-ttu-id="75032-103">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="75032-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="75032-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75032-104">SYNTAX</span></span>

### <span data-ttu-id="75032-105">ContainerInstance (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75032-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75032-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="75032-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75032-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="75032-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75032-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="75032-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75032-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="75032-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75032-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75032-110">DESCRIPTION</span></span>
<span data-ttu-id="75032-111">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="75032-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="75032-112">Ознакомьтесь с дополнительными сведениями об этой функции https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="75032-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="75032-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75032-113">EXAMPLES</span></span>

### <span data-ttu-id="75032-114">Пример 1: запуск добавочной операции копирования по имени BLOB-объектов и времени создания моментального снимка</span><span class="sxs-lookup"><span data-stu-id="75032-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="75032-115">Эта команда запускает добавочную операцию копирования по имени BLOB-объектов и времени snapshot.</span><span class="sxs-lookup"><span data-stu-id="75032-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="75032-116">Пример 2: запуск операции добавочного копирования с помощью URI источника</span><span class="sxs-lookup"><span data-stu-id="75032-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="75032-117">Эта команда запускает операцию добавочного копирования с использованием исходного кода ресурса</span><span class="sxs-lookup"><span data-stu-id="75032-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="75032-118">Пример 3: запуск операции добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="75032-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="75032-119">Эта команда запускает операцию добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="75032-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="75032-120">Пример 4: запуск операции добавочного копирования из объекта CloudPageBlob в конечный BLOB-объект с именем BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="75032-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="75032-121">Эта команда запускает операцию добавочного копирования из объекта CloudPageBlob в конечный большой двоичный объект с именем BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="75032-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="75032-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75032-122">PARAMETERS</span></span>

### <span data-ttu-id="75032-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="75032-123">-AbsoluteUri</span></span>
<span data-ttu-id="75032-124">Абсолютный URI в источник.</span><span class="sxs-lookup"><span data-stu-id="75032-124">Absolute Uri to the source.</span></span> <span data-ttu-id="75032-125">Следует отметить, что учетные данные должны быть указаны в универсальном коде ресурса (URI), если их источник требуется.</span><span class="sxs-lookup"><span data-stu-id="75032-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75032-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75032-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="75032-127">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="75032-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="75032-128">-CloudBlob</span></span>
<span data-ttu-id="75032-129">Объект CloudBlob из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75032-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="75032-130">Вы можете создать его или воспользоваться командлетом Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="75032-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75032-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="75032-131">-CloudBlobContainer</span></span>
<span data-ttu-id="75032-132">Объект CloudBlobContainer из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75032-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="75032-133">Вы можете создать его или воспользоваться командлетом Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="75032-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75032-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="75032-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="75032-135">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="75032-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="75032-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="75032-136">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-137">-Context</span><span class="sxs-lookup"><span data-stu-id="75032-137">-Context</span></span>
<span data-ttu-id="75032-138">Контекст исходного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75032-138">Source Azure Storage Context.</span></span> <span data-ttu-id="75032-139">Вы можете создать его с помощью New-AzStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="75032-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75032-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75032-140">-DefaultProfile</span></span>
<span data-ttu-id="75032-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75032-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="75032-142">-DestBlob</span></span>
<span data-ttu-id="75032-143">Имя целевого BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="75032-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="75032-144">-DestCloudBlob</span></span>
<span data-ttu-id="75032-145">Конечный объект CloudBlob</span><span class="sxs-lookup"><span data-stu-id="75032-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="75032-146">-DestContainer</span></span>
<span data-ttu-id="75032-147">Имя целевого контейнера</span><span class="sxs-lookup"><span data-stu-id="75032-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="75032-148">-DestContext</span></span>
<span data-ttu-id="75032-149">Контекст целевого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75032-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="75032-150">Вы можете создать его с помощью New-AzStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="75032-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75032-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="75032-152">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="75032-152">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="75032-153">-SrcBlob</span></span>
<span data-ttu-id="75032-154">Имя большого двоичного объекта исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="75032-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="75032-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="75032-156">Время моментального снимка BLOB исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="75032-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="75032-157">-SrcContainer</span></span>
<span data-ttu-id="75032-158">Имя исходного контейнера</span><span class="sxs-lookup"><span data-stu-id="75032-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75032-159">-Confirm</span></span>
<span data-ttu-id="75032-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75032-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75032-161">-WhatIf</span></span>
<span data-ttu-id="75032-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75032-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75032-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75032-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75032-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75032-164">CommonParameters</span></span>
<span data-ttu-id="75032-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75032-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75032-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75032-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75032-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75032-167">INPUTS</span></span>

### <span data-ttu-id="75032-168">Microsoft. Azure. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="75032-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="75032-169">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="75032-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="75032-170">System. String</span><span class="sxs-lookup"><span data-stu-id="75032-170">System.String</span></span>

### <span data-ttu-id="75032-171">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="75032-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75032-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75032-172">OUTPUTS</span></span>

### <span data-ttu-id="75032-173">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="75032-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="75032-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="75032-174">NOTES</span></span>

## <span data-ttu-id="75032-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75032-175">RELATED LINKS</span></span>