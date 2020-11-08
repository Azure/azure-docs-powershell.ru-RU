---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235254"
---
# <span data-ttu-id="d3fbc-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fbc-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="d3fbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fbc-103">Список больших двоичных объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="d3fbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3fbc-104">SYNTAX</span></span>

### <span data-ttu-id="d3fbc-105">BlobName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3fbc-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3fbc-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d3fbc-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d3fbc-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="d3fbc-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d3fbc-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="d3fbc-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d3fbc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3fbc-109">DESCRIPTION</span></span>
<span data-ttu-id="d3fbc-110">Командлет **Get-AzStorageBlob** перечисляет большие двоичные объекты в указанном контейнере в учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="d3fbc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3fbc-111">EXAMPLES</span></span>

### <span data-ttu-id="d3fbc-112">Пример 1: получение большого двоичного объекта по имени BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="d3fbc-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="d3fbc-113">Эта команда использует имя большого двоичного объекта и подстановочный знак для получения большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="d3fbc-114">Пример 2: получение больших двоичных объектов в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="d3fbc-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="d3fbc-115">Эта команда использует конвейер для получения всех больших двоичных объектов (включая BLOB-объекты в удаленном состоянии) в контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="d3fbc-116">Пример 3: Получение двоичных BLOB-имен с помощью префикса</span><span class="sxs-lookup"><span data-stu-id="d3fbc-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="d3fbc-117">Эта команда использует префикс имени для получения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="d3fbc-118">Пример 4: список больших двоичных объектов в нескольких пакетах</span><span class="sxs-lookup"><span data-stu-id="d3fbc-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="d3fbc-119">В этом примере параметры *maxcount* и *ContinuationToken* используются для перечисления больших двоичных объектов хранилища Azure в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="d3fbc-120">Первые четыре команды назначают значения переменным для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="d3fbc-121">Пятая команда задает оператор **Do-** in, использующий командлет **Get-AzStorageBlob** для получения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="d3fbc-122">Оператор включает токен продолжения, хранящийся в переменной $Token.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="d3fbc-123">$Token изменения значения по мере выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="d3fbc-124">Для получения дополнительных сведений введите `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="d3fbc-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="d3fbc-125">В последней команде используется команда **echo** для отображения итогового значения.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="d3fbc-126">Пример 5: получение всех больших двоичных объектов в контейнере, включающее версию BLOB</span><span class="sxs-lookup"><span data-stu-id="d3fbc-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="d3fbc-127">Эта команда возвращает для всех BLOB-объектов в контейнере версию большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="d3fbc-128">Пример 6: получение единственной версии большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="d3fbc-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="d3fbc-129">Эта команда возвращает один BLOB-объект verion с VersionId.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="d3fbc-130">Пример 7: получение единственного снимка большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="d3fbc-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="d3fbc-131">Эта команда возвращает один снимок больших двоичных объектов с помощью SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="d3fbc-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3fbc-132">PARAMETERS</span></span>

### <span data-ttu-id="d3fbc-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d3fbc-133">-Blob</span></span>
<span data-ttu-id="d3fbc-134">Указывает имя или шаблон имени, которые можно использовать для поиска с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="d3fbc-135">Если имя BLOB-объектов не указано, командлет выводит список всех больших двоичных объектов в указанном контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="d3fbc-136">Если для этого параметра задано значение, командлет выводит список всех больших двоичных объектов с именами, которые соответствуют этому параметру.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="d3fbc-137">Этот параметр поддерживает подстановочные знаки в любом месте строки.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3fbc-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d3fbc-139">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d3fbc-140">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d3fbc-141">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d3fbc-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d3fbc-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d3fbc-143">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d3fbc-144">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d3fbc-145">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d3fbc-146">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d3fbc-147">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-147">The default value is 10.</span></span>

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

### <span data-ttu-id="d3fbc-148">-Container</span><span class="sxs-lookup"><span data-stu-id="d3fbc-148">-Container</span></span>
<span data-ttu-id="d3fbc-149">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-150">-Context</span><span class="sxs-lookup"><span data-stu-id="d3fbc-150">-Context</span></span>
<span data-ttu-id="d3fbc-151">Указывает учетную запись хранения Azure, из которой вы хотите получить список больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="d3fbc-152">Вы можете использовать командлет New-AzStorageContext для создания контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="d3fbc-153">-ContinuationToken</span></span>
<span data-ttu-id="d3fbc-154">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="d3fbc-155">Используйте этот параметр и параметр *maxcount* для перечисления BLOB-объектов в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fbc-156">-DefaultProfile</span></span>
<span data-ttu-id="d3fbc-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3fbc-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="d3fbc-158">-IncludeDeleted</span></span>
<span data-ttu-id="d3fbc-159">Включить удаленную подбольшой двоичный объект. по умолчанию для BLOB-объектов Get не указан удаленный блоб.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="d3fbc-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="d3fbc-160">-IncludeVersion</span></span>
<span data-ttu-id="d3fbc-161">Версии двоичных объектов будут перечислены только в том случае, если этот параметр указан, по умолчанию "получить двоичный объект не содержит версий BLOB-объектов".</span><span class="sxs-lookup"><span data-stu-id="d3fbc-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d3fbc-162">-MaxCount</span></span>
<span data-ttu-id="d3fbc-163">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="d3fbc-164">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="d3fbc-164">-Prefix</span></span>
<span data-ttu-id="d3fbc-165">Задает префикс для имен больших двоичных объектов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="d3fbc-166">Этот параметр не поддерживает использование регулярных выражений и подстановочных знаков для поиска.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="d3fbc-167">Это означает, что если контейнер содержит только большие двоичные объекты с именами "My", "MyBlob1" и "MyBlob2", а вы указали "-prefix My \*", командлет не вернет BLOB-объекты.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="d3fbc-168">Тем не менее, если указать "-prefix My", командлет возвращает "My", "MyBlob1" и "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="d3fbc-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3fbc-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d3fbc-170">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d3fbc-171">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d3fbc-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d3fbc-172">-SnapshotTime</span></span>
<span data-ttu-id="d3fbc-173">SnapshotTime больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="d3fbc-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="d3fbc-174">-VersionId</span></span>
<span data-ttu-id="d3fbc-175">VersionId BLOB</span><span class="sxs-lookup"><span data-stu-id="d3fbc-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fbc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fbc-176">CommonParameters</span></span>
<span data-ttu-id="d3fbc-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3fbc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fbc-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3fbc-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fbc-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3fbc-179">INPUTS</span></span>

### <span data-ttu-id="d3fbc-180">System. String</span><span class="sxs-lookup"><span data-stu-id="d3fbc-180">System.String</span></span>

### <span data-ttu-id="d3fbc-181">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3fbc-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3fbc-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3fbc-182">OUTPUTS</span></span>

### <span data-ttu-id="d3fbc-183">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fbc-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="d3fbc-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3fbc-184">NOTES</span></span>

## <span data-ttu-id="d3fbc-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3fbc-185">RELATED LINKS</span></span>

[<span data-ttu-id="d3fbc-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d3fbc-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="d3fbc-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d3fbc-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="d3fbc-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d3fbc-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


