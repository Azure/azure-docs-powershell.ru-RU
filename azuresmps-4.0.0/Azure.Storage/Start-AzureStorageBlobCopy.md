---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01edb18c72487ada7c51408ce38502b6e87b2f56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731810"
---
# <span data-ttu-id="38b75-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="38b75-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="38b75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38b75-102">SYNOPSIS</span></span>
<span data-ttu-id="38b75-103">Начинает копирование большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="38b75-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="38b75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38b75-104">SYNTAX</span></span>

### <span data-ttu-id="38b75-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38b75-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-109">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="38b75-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="38b75-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b75-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="38b75-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b75-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38b75-115">DESCRIPTION</span></span>
<span data-ttu-id="38b75-116">Командлет **Start-AzureStorageBlobCopy** начинает копирование большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="38b75-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="38b75-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38b75-117">EXAMPLES</span></span>

### <span data-ttu-id="38b75-118">Пример 1: копирование именованного большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="38b75-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="38b75-119">Эта команда запускает операцию копирования большого двоичного объекта с именем ContosoPlanning2015 из контейнера с именем ContosoUploads в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="38b75-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="38b75-120">Пример 2: получение контейнера для выбора больших двоичных объектов для копирования</span><span class="sxs-lookup"><span data-stu-id="38b75-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="38b75-121">Эта команда получает контейнер с именем ContosoUploads с помощью командлета **Get-AzureStorageContainer** , а затем передает контейнер текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="38b75-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38b75-122">Этот командлет запускает операцию копирования большого двоичного объекта с именем ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="38b75-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="38b75-123">Предыдущий командлет предоставляет исходный контейнер.</span><span class="sxs-lookup"><span data-stu-id="38b75-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="38b75-124">Параметр *DestContainer* указывает, что ContosoArchives является конечным контейнером.</span><span class="sxs-lookup"><span data-stu-id="38b75-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="38b75-125">Пример 3: получение блоба для копирования</span><span class="sxs-lookup"><span data-stu-id="38b75-125">Example 3: Get a blob to copy</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="38b75-126">Эта команда получает большие двоичные объекты в контейнере с именем ContosoUploads с помощью командлета **Get-AzureStorageBlob** , а затем передает результаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="38b75-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38b75-127">Этот командлет запускает операцию копирования больших двоичных объектов в контейнер с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="38b75-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="38b75-128">Пример 4: копирование большого двоичного объекта, указанного как объект</span><span class="sxs-lookup"><span data-stu-id="38b75-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="38b75-129">Первая команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="38b75-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="38b75-130">Команда сохраняет этот объект в переменной $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="38b75-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="38b75-131">Вторая команда получает большой двоичный объект с именем ContosoPlanning2015Archived в контейнере с именем ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="38b75-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="38b75-132">Команда сохраняет этот объект в переменной $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="38b75-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="38b75-133">Последняя команда запускает операцию копирования из исходного контейнера в целевой контейнер.</span><span class="sxs-lookup"><span data-stu-id="38b75-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="38b75-134">В команде используется стандартная точечная нотация для задания объектов **ICloudBlob** для $SrcBlob и $DestBlob больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="38b75-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="38b75-135">Пример 5: копирование большого двоичного объекта из URI</span><span class="sxs-lookup"><span data-stu-id="38b75-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="38b75-136">Эта команда создает контекст для учетной записи с именем ContosoGeneral, использующей указанный ключ, и сохраняет этот ключ в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="38b75-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="38b75-137">Вторая команда копирует файл из указанного URI в большой двоичный объект с именем ContosoPlanning в контейнере с именем ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="38b75-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="38b75-138">Команда запускает операцию копирования в контексте, который хранится в $Context.</span><span class="sxs-lookup"><span data-stu-id="38b75-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="38b75-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38b75-139">PARAMETERS</span></span>

### <span data-ttu-id="38b75-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="38b75-140">-AbsoluteUri</span></span>
<span data-ttu-id="38b75-141">Указывает абсолютный универсальный код ресурса (URI) файла, который нужно скопировать в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="38b75-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38b75-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="38b75-143">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="38b75-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="38b75-144">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="38b75-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="38b75-145">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="38b75-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="38b75-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="38b75-146">-CloudBlob</span></span>
<span data-ttu-id="38b75-147">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="38b75-148">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="38b75-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="38b75-149">-CloudBlobContainer</span></span>
<span data-ttu-id="38b75-150">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="38b75-151">Этот командлет копирует большой двоичный объект из контейнера, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="38b75-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="38b75-152">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="38b75-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="38b75-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="38b75-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="38b75-154">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="38b75-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="38b75-155">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="38b75-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="38b75-156">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="38b75-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="38b75-157">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="38b75-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="38b75-158">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="38b75-158">The default value is 10.</span></span>

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

### <span data-ttu-id="38b75-159">-Context</span><span class="sxs-lookup"><span data-stu-id="38b75-159">-Context</span></span>
<span data-ttu-id="38b75-160">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38b75-161">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="38b75-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="38b75-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="38b75-162">-DestBlob</span></span>
<span data-ttu-id="38b75-163">Указывает имя целевого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="38b75-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="38b75-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="38b75-164">-DestCloudBlob</span></span>
<span data-ttu-id="38b75-165">Указывает конечный объект **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="38b75-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="38b75-166">-DestContainer</span></span>
<span data-ttu-id="38b75-167">Указывает имя конечного контейнера.</span><span class="sxs-lookup"><span data-stu-id="38b75-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="38b75-168">-DestContext</span></span>
<span data-ttu-id="38b75-169">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38b75-170">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="38b75-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38b75-171">-Force</span><span class="sxs-lookup"><span data-stu-id="38b75-171">-Force</span></span>
<span data-ttu-id="38b75-172">Указывает на то, что этот командлет перезапишет конечный двоичный объект, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="38b75-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="38b75-173">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38b75-173">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="38b75-174">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="38b75-174">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="38b75-175">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="38b75-175">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="38b75-176">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="38b75-176">-SrcBlob</span></span>
<span data-ttu-id="38b75-177">Указывает имя исходного объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="38b75-177">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-178">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="38b75-178">-SrcContainer</span></span>
<span data-ttu-id="38b75-179">Указывает имя исходного контейнера.</span><span class="sxs-lookup"><span data-stu-id="38b75-179">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="38b75-180">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="38b75-180">-SrcDir</span></span>
<span data-ttu-id="38b75-181">Указывает объект **CloudFileDirectory** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-181">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-182">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="38b75-182">-SrcFile</span></span>
<span data-ttu-id="38b75-183">Specifes объект **CloudFile** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-183">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="38b75-184">Вы можете создать его или воспользоваться командлетом Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="38b75-184">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-185">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="38b75-185">-SrcFilePath</span></span>
<span data-ttu-id="38b75-186">Указывает относительный путь к исходному каталогу или исходному общему файлу.</span><span class="sxs-lookup"><span data-stu-id="38b75-186">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-187">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="38b75-187">-SrcShare</span></span>
<span data-ttu-id="38b75-188">Указывает объект **CloudFileShare** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="38b75-188">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="38b75-189">Вы можете создать его или воспользоваться командлетом Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="38b75-189">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-190">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="38b75-190">-SrcShareName</span></span>
<span data-ttu-id="38b75-191">Указывает имя исходного общего файлового источника.</span><span class="sxs-lookup"><span data-stu-id="38b75-191">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b75-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38b75-192">-Confirm</span></span>
<span data-ttu-id="38b75-193">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38b75-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b75-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b75-194">-WhatIf</span></span>
<span data-ttu-id="38b75-195">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38b75-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b75-196">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38b75-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b75-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b75-197">CommonParameters</span></span>
<span data-ttu-id="38b75-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38b75-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b75-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b75-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b75-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38b75-200">INPUTS</span></span>

## <span data-ttu-id="38b75-201">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38b75-201">OUTPUTS</span></span>

## <span data-ttu-id="38b75-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="38b75-202">NOTES</span></span>

## <span data-ttu-id="38b75-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38b75-203">RELATED LINKS</span></span>

[<span data-ttu-id="38b75-204">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="38b75-204">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="38b75-205">Остановить-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="38b75-205">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
