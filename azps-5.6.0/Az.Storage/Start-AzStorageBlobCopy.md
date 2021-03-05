---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 754ac7657561ba52e28f90d951c0843a8c206484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002232"
---
# <span data-ttu-id="83e7e-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="83e7e-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="83e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="83e7e-103">Начинается копирование BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="83e7e-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="83e7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83e7e-104">SYNTAX</span></span>

### <span data-ttu-id="83e7e-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83e7e-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83e7e-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83e7e-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83e7e-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83e7e-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="83e7e-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7e-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7e-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7e-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7e-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="83e7e-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83e7e-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="83e7e-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e7e-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83e7e-115">DESCRIPTION</span></span>
<span data-ttu-id="83e7e-116">Начинается копирование BLOB-lob-blob-2016 стебляемого **lob-blob-лета Start-AzStorageBlobCopy.**</span><span class="sxs-lookup"><span data-stu-id="83e7e-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="83e7e-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83e7e-117">EXAMPLES</span></span>

### <span data-ttu-id="83e7e-118">Пример 1. Копирование именуемго BLOB-имени</span><span class="sxs-lookup"><span data-stu-id="83e7e-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="83e7e-119">Эта команда запускает операцию копирования BLOB-части с именем ContosoPlanning2015 из контейнера ContosoUploads в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="83e7e-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="83e7e-120">Пример 2. Получить контейнер для указания BLOB-ветвей для копирования</span><span class="sxs-lookup"><span data-stu-id="83e7e-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="83e7e-121">Эта команда получает контейнер ContosoUploads с помощью командлета **Get-AzStorageContainer,** а затем передает контейнер текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="83e7e-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83e7e-122">Этот cmdlet запускает операцию копирования BLOB-части с именем ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="83e7e-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="83e7e-123">Предыдущий cmdlet предоставляет исходный контейнер.</span><span class="sxs-lookup"><span data-stu-id="83e7e-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="83e7e-124">Параметр *DestContainer* определяет ContosoArchives в качестве контейнера назначения.</span><span class="sxs-lookup"><span data-stu-id="83e7e-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="83e7e-125">Пример 3. Получите все большой бизнес-бизнес в контейнере и скопируйте их</span><span class="sxs-lookup"><span data-stu-id="83e7e-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="83e7e-126">Эта команда получает БД в контейнере ContosoUploads с помощью командлета **Get-AzStorageBlob,** а затем передает результаты текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="83e7e-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83e7e-127">Этот cmdlet запускает операцию копирования BLOB-имен в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="83e7e-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="83e7e-128">Пример 4. Копирование BLOB-объекта, указанного в качестве объекта</span><span class="sxs-lookup"><span data-stu-id="83e7e-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="83e7e-129">Первая команда получает BLOB-проект ContosoPlanning2015 в контейнере ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="83e7e-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="83e7e-130">Эта команда сохраняет этот объект в переменной $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="83e7e-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="83e7e-131">Вторая команда получает BLOB-проект с именем ContosoPlanning2015Archived в контейнере ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="83e7e-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="83e7e-132">Эта команда сохраняет этот объект в переменной $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="83e7e-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="83e7e-133">Последняя команда начинает операцию копирования из контейнера-источника в контейнер назначения.</span><span class="sxs-lookup"><span data-stu-id="83e7e-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="83e7e-134">Для указания объектов **ICloudBlob** для BLOB-объектов $SrcBlob и $DestBlob точками используется стандартная точка.</span><span class="sxs-lookup"><span data-stu-id="83e7e-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="83e7e-135">Пример 5. Копирование BLOB-то из URI</span><span class="sxs-lookup"><span data-stu-id="83e7e-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="83e7e-136">Эта команда создает контекст для учетной записи ContosoGeneral, использующей указанный ключ, а затем сохраняет этот ключ в $Context переменной.</span><span class="sxs-lookup"><span data-stu-id="83e7e-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="83e7e-137">Вторая команда копирует файл из указанного URI в BLOB-файл с именем ContosoPlanning в контейнере ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="83e7e-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="83e7e-138">Команда начинает операцию копирования в контексте назначения, $Context.</span><span class="sxs-lookup"><span data-stu-id="83e7e-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="83e7e-139">Контекста для источника хранилища нет, поэтому у URI источника должен быть доступ к объекту-источнику.</span><span class="sxs-lookup"><span data-stu-id="83e7e-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="83e7e-140">Например, если источником является ни один общедоступный BLOB-проект Azure, то Uri должен содержать маркер SAS, который имеет доступ к нему для чтения.</span><span class="sxs-lookup"><span data-stu-id="83e7e-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="83e7e-141">Пример 6. Копирование BLOB-блоков в контейнер назначения с новым именем BLOB-блоков и назначение BLOB-blob StandardBlobTier в качестве высокого, RehydratePriority as High</span><span class="sxs-lookup"><span data-stu-id="83e7e-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="83e7e-142">Эта команда запускает операцию копирования BLOB-блоков в контейнер назначения с новым именем BLOB-пунктов и назовет назначение BLOB-blob StandardBlobTier как "Hot", RehydratePriority as High</span><span class="sxs-lookup"><span data-stu-id="83e7e-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="83e7e-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83e7e-143">PARAMETERS</span></span>

### <span data-ttu-id="83e7e-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="83e7e-144">-AbsoluteUri</span></span>
<span data-ttu-id="83e7e-145">Определяет абсолютный URI файла, который нужно скопировать в большой объем хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="83e7e-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="83e7e-146">-BlobBaseClient</span></span>
<span data-ttu-id="83e7e-147">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="83e7e-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83e7e-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="83e7e-149">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="83e7e-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="83e7e-150">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="83e7e-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="83e7e-151">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="83e7e-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="83e7e-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-152">-CloudBlob</span></span>
<span data-ttu-id="83e7e-153">Указывает объект **CloudBlob из** библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="83e7e-154">Чтобы получить объект **CloudBlob,** используйте Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="83e7e-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="83e7e-155">-CloudBlobContainer</span></span>
<span data-ttu-id="83e7e-156">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="83e7e-157">Этот cmdlet копирует большой большой проект из контейнера, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="83e7e-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="83e7e-158">Чтобы получить объект **CloudBlobContainer,** воспользуйтесь Get-AzStorageContainer управления.</span><span class="sxs-lookup"><span data-stu-id="83e7e-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="83e7e-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="83e7e-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="83e7e-160">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="83e7e-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="83e7e-161">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="83e7e-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="83e7e-162">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="83e7e-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="83e7e-163">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="83e7e-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="83e7e-164">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="83e7e-164">The default value is 10.</span></span>

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

### <span data-ttu-id="83e7e-165">-Контекст</span><span class="sxs-lookup"><span data-stu-id="83e7e-165">-Context</span></span>
<span data-ttu-id="83e7e-166">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="83e7e-167">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="83e7e-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="83e7e-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e7e-168">-DefaultProfile</span></span>
<span data-ttu-id="83e7e-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e7e-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-170">-DestBlob</span></span>
<span data-ttu-id="83e7e-171">Имя конечного BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="83e7e-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="83e7e-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-172">-DestCloudBlob</span></span>
<span data-ttu-id="83e7e-173">Определяет объект **CloudBlob** назначения.</span><span class="sxs-lookup"><span data-stu-id="83e7e-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="83e7e-174">-DestContainer</span></span>
<span data-ttu-id="83e7e-175">Имя конечного контейнера.</span><span class="sxs-lookup"><span data-stu-id="83e7e-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="83e7e-176">-DestContext</span></span>
<span data-ttu-id="83e7e-177">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="83e7e-178">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="83e7e-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="83e7e-179">-Force</span><span class="sxs-lookup"><span data-stu-id="83e7e-179">-Force</span></span>
<span data-ttu-id="83e7e-180">Указывает на то, что этот cmdlet переописает BLOB-проект назначения, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="83e7e-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="83e7e-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="83e7e-182">Уровень BLOB-ля страницы Premium</span><span class="sxs-lookup"><span data-stu-id="83e7e-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="83e7e-183">-RehydratePriority</span></span>
<span data-ttu-id="83e7e-184">Блокировать BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="83e7e-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="83e7e-185">Приоритет, с помощью которого нужно перегибать архивный BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="83e7e-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="83e7e-186">Допустимые значения: "Высокое" или "Стандартное".</span><span class="sxs-lookup"><span data-stu-id="83e7e-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83e7e-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="83e7e-188">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="83e7e-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="83e7e-189">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="83e7e-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="83e7e-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-190">-SrcBlob</span></span>
<span data-ttu-id="83e7e-191">Имя источника BLOB-имени.</span><span class="sxs-lookup"><span data-stu-id="83e7e-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="83e7e-192">-SrcContainer</span></span>
<span data-ttu-id="83e7e-193">Имя контейнера-источника.</span><span class="sxs-lookup"><span data-stu-id="83e7e-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="83e7e-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="83e7e-194">-SrcDir</span></span>
<span data-ttu-id="83e7e-195">Указывает объект **CloudFileDirectory** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="83e7e-196">-SrcFile</span></span>
<span data-ttu-id="83e7e-197">Указывает объект **CloudFile** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="83e7e-198">Его можно создать или использовать Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="83e7e-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="83e7e-199">-SrcFilePath</span></span>
<span data-ttu-id="83e7e-200">Определяет относительный путь к источнику или папке.</span><span class="sxs-lookup"><span data-stu-id="83e7e-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="83e7e-201">-SrcShare</span></span>
<span data-ttu-id="83e7e-202">Указывает объект **CloudFileShare из** библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="83e7e-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="83e7e-203">Его можно создать или использовать Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="83e7e-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="83e7e-204">-SrcShareName</span></span>
<span data-ttu-id="83e7e-205">Указывает имя источника.</span><span class="sxs-lookup"><span data-stu-id="83e7e-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="83e7e-206">-StandardBlobTier</span></span>
<span data-ttu-id="83e7e-207">Заблокировать уровень BLOB-блоков, допустимые значения — "Hot/Cool/Archive".</span><span class="sxs-lookup"><span data-stu-id="83e7e-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="83e7e-208">Подробности https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="83e7e-208">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83e7e-209">-Confirm</span></span>
<span data-ttu-id="83e7e-210">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83e7e-210">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e7e-211">-WhatIf</span></span>
<span data-ttu-id="83e7e-212">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83e7e-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e7e-213">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="83e7e-213">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7e-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e7e-214">CommonParameters</span></span>
<span data-ttu-id="83e7e-215">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e7e-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e7e-216">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e7e-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e7e-217">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83e7e-217">INPUTS</span></span>

### <span data-ttu-id="83e7e-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="83e7e-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="83e7e-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="83e7e-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="83e7e-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="83e7e-221">System.String</span><span class="sxs-lookup"><span data-stu-id="83e7e-221">System.String</span></span>

### <span data-ttu-id="83e7e-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83e7e-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83e7e-223">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83e7e-223">OUTPUTS</span></span>

### <span data-ttu-id="83e7e-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="83e7e-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="83e7e-225">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83e7e-225">NOTES</span></span>

## <span data-ttu-id="83e7e-226">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83e7e-226">RELATED LINKS</span></span>

[<span data-ttu-id="83e7e-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="83e7e-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="83e7e-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="83e7e-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
