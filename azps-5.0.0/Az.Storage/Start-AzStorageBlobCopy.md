---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245746"
---
# <span data-ttu-id="0bcb1-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0bcb1-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="0bcb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcb1-103">Начинает копирование большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="0bcb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bcb1-104">SYNTAX</span></span>

### <span data-ttu-id="0bcb1-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0bcb1-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-109">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="0bcb1-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="0bcb1-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcb1-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="0bcb1-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bcb1-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bcb1-115">DESCRIPTION</span></span>
<span data-ttu-id="0bcb1-116">Командлет **Start-AzStorageBlobCopy** начинает копирование большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="0bcb1-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bcb1-117">EXAMPLES</span></span>

### <span data-ttu-id="0bcb1-118">Пример 1: копирование именованного большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="0bcb1-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="0bcb1-119">Эта команда запускает операцию копирования большого двоичного объекта с именем ContosoPlanning2015 из контейнера с именем ContosoUploads в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="0bcb1-120">Пример 2: получение контейнера для выбора больших двоичных объектов для копирования</span><span class="sxs-lookup"><span data-stu-id="0bcb1-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="0bcb1-121">Эта команда получает контейнер с именем ContosoUploads с помощью командлета **Get-AzStorageContainer** , а затем передает контейнер текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0bcb1-122">Этот командлет запускает операцию копирования большого двоичного объекта с именем ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="0bcb1-123">Предыдущий командлет предоставляет исходный контейнер.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="0bcb1-124">Параметр *DestContainer* указывает, что ContosoArchives является конечным контейнером.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="0bcb1-125">Пример 3: получение всех больших двоичных объектов в контейнере и их копирование</span><span class="sxs-lookup"><span data-stu-id="0bcb1-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="0bcb1-126">Эта команда получает большие двоичные объекты в контейнере с именем ContosoUploads с помощью командлета **Get-AzStorageBlob** , а затем передает результаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0bcb1-127">Этот командлет запускает операцию копирования больших двоичных объектов в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="0bcb1-128">Пример 4: копирование большого двоичного объекта, указанного как объект</span><span class="sxs-lookup"><span data-stu-id="0bcb1-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="0bcb1-129">Первая команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="0bcb1-130">Команда сохраняет этот объект в переменной $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="0bcb1-131">Вторая команда получает большой двоичный объект с именем ContosoPlanning2015Archived в контейнере с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="0bcb1-132">Команда сохраняет этот объект в переменной $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="0bcb1-133">Последняя команда запускает операцию копирования из исходного контейнера в целевой контейнер.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="0bcb1-134">В команде используется стандартная точечная нотация для задания объектов **ICloudBlob** для $SrcBlob и $DestBlob больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="0bcb1-135">Пример 5: копирование большого двоичного объекта из URI</span><span class="sxs-lookup"><span data-stu-id="0bcb1-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="0bcb1-136">Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот ключ в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="0bcb1-137">Вторая команда копирует файл из указанного URI в большой двоичный объект с именем ContosoPlanning в контейнере с именем ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="0bcb1-138">Команда запускает операцию копирования в контекст назначения, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="0bcb1-139">Контекст хранения исходного кода отсутствует, поэтому URI источника должен иметь доступ к исходному объекту.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="0bcb1-140">Например: Если источник не является общедоступным BLOB-объектом Azure None, URI должен содержать токен SAS, имеющий доступ на чтение к большому двоичному объекту.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="0bcb1-141">Пример 6: копирование блока большого двоичного объекта в конечный контейнер с новым именем большого двоичного объекта и назначение BLOB-объектов назначения StandardBlobTier как нагревается, RehydratePriority как высокий.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="0bcb1-142">Эта команда запускает операцию копирования для блочного большого двоичного объекта в конечный контейнер с новым именем большого двоичного объекта и задает для целевого объекта BLOB StandardBlobTier значение "горячий", RehydratePriority как высокий.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="0bcb1-143">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bcb1-143">PARAMETERS</span></span>

### <span data-ttu-id="0bcb1-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="0bcb1-144">-AbsoluteUri</span></span>
<span data-ttu-id="0bcb1-145">Указывает абсолютный универсальный код ресурса (URI) файла, который нужно скопировать в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="0bcb1-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0bcb1-146">-BlobBaseClient</span></span>
<span data-ttu-id="0bcb1-147">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0bcb1-147">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="0bcb1-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0bcb1-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0bcb1-149">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0bcb1-150">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0bcb1-151">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0bcb1-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-152">-CloudBlob</span></span>
<span data-ttu-id="0bcb1-153">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0bcb1-154">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0bcb1-155">-CloudBlobContainer</span></span>
<span data-ttu-id="0bcb1-156">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0bcb1-157">Этот командлет копирует большой двоичный объект из контейнера, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="0bcb1-158">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0bcb1-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0bcb1-160">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0bcb1-161">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0bcb1-162">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0bcb1-163">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0bcb1-164">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-164">The default value is 10.</span></span>

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

### <span data-ttu-id="0bcb1-165">-Context</span><span class="sxs-lookup"><span data-stu-id="0bcb1-165">-Context</span></span>
<span data-ttu-id="0bcb1-166">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0bcb1-167">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcb1-168">-DefaultProfile</span></span>
<span data-ttu-id="0bcb1-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bcb1-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-170">-DestBlob</span></span>
<span data-ttu-id="0bcb1-171">Указывает имя целевого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="0bcb1-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-172">-DestCloudBlob</span></span>
<span data-ttu-id="0bcb1-173">Указывает конечный объект **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="0bcb1-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="0bcb1-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="0bcb1-174">-DestContainer</span></span>
<span data-ttu-id="0bcb1-175">Указывает имя конечного контейнера.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="0bcb1-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="0bcb1-176">-DestContext</span></span>
<span data-ttu-id="0bcb1-177">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0bcb1-178">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-179">-Force</span><span class="sxs-lookup"><span data-stu-id="0bcb1-179">-Force</span></span>
<span data-ttu-id="0bcb1-180">Указывает на то, что этот командлет перезапишет конечный двоичный объект, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0bcb1-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="0bcb1-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="0bcb1-182">Уровень больших двоичных объектов страницы Premium</span><span class="sxs-lookup"><span data-stu-id="0bcb1-182">Premium Page Blob Tier</span></span>

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

### <span data-ttu-id="0bcb1-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="0bcb1-183">-RehydratePriority</span></span>
<span data-ttu-id="0bcb1-184">Блокировать RehydratePriority больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="0bcb1-185">Указывает приоритет, с которым требуется возобновлень архивный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="0bcb1-186">Допустимые значения: High/Standard.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-186">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="0bcb1-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0bcb1-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0bcb1-188">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0bcb1-189">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0bcb1-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-190">-SrcBlob</span></span>
<span data-ttu-id="0bcb1-191">Указывает имя исходного объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="0bcb1-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="0bcb1-192">-SrcContainer</span></span>
<span data-ttu-id="0bcb1-193">Указывает имя исходного контейнера.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="0bcb1-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="0bcb1-194">-SrcDir</span></span>
<span data-ttu-id="0bcb1-195">Указывает объект **CloudFileDirectory** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="0bcb1-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="0bcb1-196">-SrcFile</span></span>
<span data-ttu-id="0bcb1-197">Указывает объект **CloudFile** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0bcb1-198">Вы можете создать его или воспользоваться командлетом Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="0bcb1-199">-SrcFilePath</span></span>
<span data-ttu-id="0bcb1-200">Указывает относительный путь к исходному каталогу или исходному общему файлу.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="0bcb1-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="0bcb1-201">-SrcShare</span></span>
<span data-ttu-id="0bcb1-202">Указывает объект **CloudFileShare** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0bcb1-203">Вы можете создать его или воспользоваться командлетом Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="0bcb1-204">-SrcShareName</span></span>
<span data-ttu-id="0bcb1-205">Указывает имя исходного общего файлового источника.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="0bcb1-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="0bcb1-206">-StandardBlobTier</span></span>
<span data-ttu-id="0bcb1-207">Блокировать уровень больших двоичных объектов. Допустимые значения: горячий/крутой/архивный.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="0bcb1-208">Подробные сведения https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="0bcb1-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="0bcb1-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bcb1-209">-Confirm</span></span>
<span data-ttu-id="0bcb1-210">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bcb1-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bcb1-211">-WhatIf</span></span>
<span data-ttu-id="0bcb1-212">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bcb1-213">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bcb1-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcb1-214">CommonParameters</span></span>
<span data-ttu-id="0bcb1-215">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bcb1-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcb1-216">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bcb1-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcb1-217">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bcb1-217">INPUTS</span></span>

### <span data-ttu-id="0bcb1-218">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0bcb1-219">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0bcb1-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0bcb1-220">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0bcb1-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="0bcb1-221">System. String</span><span class="sxs-lookup"><span data-stu-id="0bcb1-221">System.String</span></span>

### <span data-ttu-id="0bcb1-222">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0bcb1-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0bcb1-223">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bcb1-223">OUTPUTS</span></span>

### <span data-ttu-id="0bcb1-224">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0bcb1-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0bcb1-225">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bcb1-225">NOTES</span></span>

## <span data-ttu-id="0bcb1-226">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bcb1-226">RELATED LINKS</span></span>

[<span data-ttu-id="0bcb1-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="0bcb1-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="0bcb1-228">Остановить-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0bcb1-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)