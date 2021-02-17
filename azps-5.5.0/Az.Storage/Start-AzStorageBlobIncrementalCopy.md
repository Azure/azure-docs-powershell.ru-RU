---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243173"
---
# <span data-ttu-id="988f0-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="988f0-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="988f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988f0-102">SYNOPSIS</span></span>
<span data-ttu-id="988f0-103">Запуск операции добавоической копии из моментального снимка BLOB-сайта страницы в указанный BLOB-проект страницы.</span><span class="sxs-lookup"><span data-stu-id="988f0-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="988f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="988f0-104">SYNTAX</span></span>

### <span data-ttu-id="988f0-105">ContainerInstance (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="988f0-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988f0-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="988f0-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988f0-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="988f0-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988f0-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="988f0-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988f0-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="988f0-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988f0-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="988f0-110">DESCRIPTION</span></span>
<span data-ttu-id="988f0-111">Запуск операции добавоической копии из моментального снимка BLOB-сайта страницы в указанный BLOB-проект страницы.</span><span class="sxs-lookup"><span data-stu-id="988f0-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="988f0-112">Дополнительные сведения о функции см. в https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="988f0-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="988f0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="988f0-113">EXAMPLES</span></span>

### <span data-ttu-id="988f0-114">Пример 1. Запуск добавонной операции копирования по имени BLOB-имени и времени моментального снимка</span><span class="sxs-lookup"><span data-stu-id="988f0-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="988f0-115">Эта команда начинает добаво бытовую операцию копирования по имени BLOB-имени и времени моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="988f0-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="988f0-116">Пример 2. Запуск добавонной операции копирования с использованием URI источника</span><span class="sxs-lookup"><span data-stu-id="988f0-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="988f0-117">Эта команда начинает добаво бытовую операцию копирования с использованием URI источника</span><span class="sxs-lookup"><span data-stu-id="988f0-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="988f0-118">Пример 3. Запуск добавонной операции копирования с использованием конвейера контейнера от GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="988f0-119">Эта команда запускает добаво бытовую операцию копирования с использованием конвейера контейнера от GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="988f0-120">Пример 4. Запуск добавочной операции копирования из объекта CloudPageBlob в назначение BLOB-объектов с именем BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="988f0-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="988f0-121">Эта команда запускает добавочное копирование из объекта CloudPageBlob в объект назначения BLOB-объекта с именем BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="988f0-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="988f0-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="988f0-122">PARAMETERS</span></span>

### <span data-ttu-id="988f0-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="988f0-123">-AbsoluteUri</span></span>
<span data-ttu-id="988f0-124">Абсолютный URI источника.</span><span class="sxs-lookup"><span data-stu-id="988f0-124">Absolute Uri to the source.</span></span> <span data-ttu-id="988f0-125">Следует отметить, что учетные данные должны быть предоставлены в коде URI, если источник их требует.</span><span class="sxs-lookup"><span data-stu-id="988f0-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="988f0-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="988f0-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="988f0-127">Максимальное время выполнения каждого запроса на стороне клиента в секундах.</span><span class="sxs-lookup"><span data-stu-id="988f0-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="988f0-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-128">-CloudBlob</span></span>
<span data-ttu-id="988f0-129">Объект CloudBlob из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="988f0-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="988f0-130">Его можно создать или использовать Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="988f0-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="988f0-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-131">-CloudBlobContainer</span></span>
<span data-ttu-id="988f0-132">Объект CloudBlobContainer из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="988f0-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="988f0-133">Его можно создать или использовать Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="988f0-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="988f0-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="988f0-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="988f0-135">Общее количество одновременной работы с async.</span><span class="sxs-lookup"><span data-stu-id="988f0-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="988f0-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="988f0-136">The default value is 10.</span></span>

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

### <span data-ttu-id="988f0-137">-Контекст</span><span class="sxs-lookup"><span data-stu-id="988f0-137">-Context</span></span>
<span data-ttu-id="988f0-138">Контекст источника хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="988f0-138">Source Azure Storage Context.</span></span> <span data-ttu-id="988f0-139">Его можно создать с помощью New-AzStorageContext- или New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="988f0-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="988f0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988f0-140">-DefaultProfile</span></span>
<span data-ttu-id="988f0-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="988f0-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988f0-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-142">-DestBlob</span></span>
<span data-ttu-id="988f0-143">Имя BLOB-имени назначения</span><span class="sxs-lookup"><span data-stu-id="988f0-143">Destination blob name</span></span>

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

### <span data-ttu-id="988f0-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-144">-DestCloudBlob</span></span>
<span data-ttu-id="988f0-145">Объект CloudBlob назначения</span><span class="sxs-lookup"><span data-stu-id="988f0-145">Destination CloudBlob object</span></span>

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

### <span data-ttu-id="988f0-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-146">-DestContainer</span></span>
<span data-ttu-id="988f0-147">Имя контейнера назначения</span><span class="sxs-lookup"><span data-stu-id="988f0-147">Destination container name</span></span>

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

### <span data-ttu-id="988f0-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="988f0-148">-DestContext</span></span>
<span data-ttu-id="988f0-149">Контекст места назначения хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="988f0-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="988f0-150">Его можно создать с помощью New-AzStorageContext- или New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="988f0-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="988f0-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="988f0-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="988f0-152">Время с часовой стрелкой для каждого запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="988f0-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="988f0-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-153">-SrcBlob</span></span>
<span data-ttu-id="988f0-154">Имя BLOB-сайта страницы.</span><span class="sxs-lookup"><span data-stu-id="988f0-154">Source page blob name.</span></span>

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

### <span data-ttu-id="988f0-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="988f0-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="988f0-156">Время моментального снимка BLOB-сайта на первой странице.</span><span class="sxs-lookup"><span data-stu-id="988f0-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="988f0-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-157">-SrcContainer</span></span>
<span data-ttu-id="988f0-158">Имя контейнера источника</span><span class="sxs-lookup"><span data-stu-id="988f0-158">Source Container name</span></span>

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

### <span data-ttu-id="988f0-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="988f0-159">-Confirm</span></span>
<span data-ttu-id="988f0-160">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="988f0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988f0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988f0-161">-WhatIf</span></span>
<span data-ttu-id="988f0-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988f0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988f0-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="988f0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988f0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988f0-164">CommonParameters</span></span>
<span data-ttu-id="988f0-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988f0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988f0-166">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988f0-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988f0-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="988f0-167">INPUTS</span></span>

### <span data-ttu-id="988f0-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="988f0-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="988f0-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="988f0-170">System.String</span><span class="sxs-lookup"><span data-stu-id="988f0-170">System.String</span></span>

### <span data-ttu-id="988f0-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="988f0-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="988f0-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="988f0-172">OUTPUTS</span></span>

### <span data-ttu-id="988f0-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="988f0-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="988f0-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="988f0-174">NOTES</span></span>

## <span data-ttu-id="988f0-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="988f0-175">RELATED LINKS</span></span>
