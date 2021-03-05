---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 317d25ecfa48203c411f368aa5b00ac3380773ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002760"
---
# <span data-ttu-id="c2fa6-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c2fa6-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="c2fa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fa6-103">Список BLOB-то в контейнере.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="c2fa6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2fa6-104">SYNTAX</span></span>

### <span data-ttu-id="c2fa6-105">BlobName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2fa6-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2fa6-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c2fa6-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c2fa6-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="c2fa6-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c2fa6-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="c2fa6-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c2fa6-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2fa6-109">DESCRIPTION</span></span>
<span data-ttu-id="c2fa6-110">С его учетной записью в учетной записи хранилища Azure в списке **BLOB-хранилищ в Get-AzStorageBlob** перечислены BLOB-клиенты в указанном контейнере.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="c2fa6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2fa6-111">EXAMPLES</span></span>

### <span data-ttu-id="c2fa6-112">Пример 1. Получить большой бизнес-бизнес по имени</span><span class="sxs-lookup"><span data-stu-id="c2fa6-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="c2fa6-113">Эта команда использует имя BLOB-ля и поддиавный знак для его получения.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="c2fa6-114">Пример 2. В контейнере можно получать большой объем в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c2fa6-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="c2fa6-115">Эта команда использует канал для получения всех BLOB-проектов (включая их в состоянии "Удаленные") в контейнер.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="c2fa6-116">Пример 3. Получить BLOB-бизнес по префиксу имени</span><span class="sxs-lookup"><span data-stu-id="c2fa6-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="c2fa6-117">Для этого используется префикс имени.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="c2fa6-118">Пример 4. Список BLOB-залов в нескольких пакетах</span><span class="sxs-lookup"><span data-stu-id="c2fa6-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="c2fa6-119">В этом примере *параметры MaxCount* и *ContinuationToken* используются для списка BLOB-залов хранилища Azure в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="c2fa6-120">Первые четыре команды присваивают значения переменным, которые используются в примере.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="c2fa6-121">Пятая команда указывает на утверждение **Do-While,** использующее командлет **Get-AzStorageBlob** для получения BLOB-ей части.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="c2fa6-122">Она включает маркер продолжения, который хранится в переменной $Token продолжения.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="c2fa6-123">$Token изменяет значение по мере его цикла.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="c2fa6-124">Для получения дополнительных сведений введите `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="c2fa6-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="c2fa6-125">Для отображения итогового числа в конечной команде используется команда **Echo.**</span><span class="sxs-lookup"><span data-stu-id="c2fa6-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="c2fa6-126">Пример 5. Все BLOB-lob-lob в контейнере включают версию BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="c2fa6-126">Example 5: Get all blobs in a container include blob version</span></span>
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

<span data-ttu-id="c2fa6-127">Эта команда получает все BLOB-lob-lob в контейнере, включая версию BLOB-lob.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="c2fa6-128">Пример 6. Получить одну версию BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="c2fa6-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="c2fa6-129">Эта команда получает одну вершину BLOB-команд с VersionId.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="c2fa6-130">Пример 7. Получить один моментальный снимок BLOB-бизнеса</span><span class="sxs-lookup"><span data-stu-id="c2fa6-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="c2fa6-131">Эта команда получает один моментальный снимок большой lob-lob-2016 с помощью Моментального времени.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="c2fa6-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fa6-132">PARAMETERS</span></span>

### <span data-ttu-id="c2fa6-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c2fa6-133">-Blob</span></span>
<span data-ttu-id="c2fa6-134">Определяет имя или шаблон имени, который можно использовать для поиска поддерев.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="c2fa6-135">Если имя BLOB-ля не задано, будет выдан список всех BLOB-имен в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="c2fa6-136">Если для этого параметра задано значение, командлет перечисляет все BLOB-lob-группы с именами, которые соответствуют этому параметру.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="c2fa6-137">Этот параметр поддерживает поддиавные знаки в любом месте строки.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-137">This parameter supports wildcards anywhere in the string.</span></span>

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

### <span data-ttu-id="c2fa6-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2fa6-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c2fa6-139">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c2fa6-140">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c2fa6-141">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c2fa6-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c2fa6-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c2fa6-143">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c2fa6-144">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c2fa6-145">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c2fa6-146">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c2fa6-147">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-147">The default value is 10.</span></span>

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

### <span data-ttu-id="c2fa6-148">-Container</span><span class="sxs-lookup"><span data-stu-id="c2fa6-148">-Container</span></span>
<span data-ttu-id="c2fa6-149">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="c2fa6-150">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c2fa6-150">-Context</span></span>
<span data-ttu-id="c2fa6-151">Указывает учетную запись хранилища Azure, из которой вы хотите получить список BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="c2fa6-152">С помощью New-AzStorageContext можно создать контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="c2fa6-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c2fa6-153">-ContinuationToken</span></span>
<span data-ttu-id="c2fa6-154">Указывает маркер продолжения для списка BLOB-приложений.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="c2fa6-155">Используйте этот параметр и параметр *MaxCount* для списка BLOB-залов в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="c2fa6-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fa6-156">-DefaultProfile</span></span>
<span data-ttu-id="c2fa6-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fa6-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="c2fa6-158">-IncludeDeleted</span></span>
<span data-ttu-id="c2fa6-159">Include Deleted BLOB, по умолчанию он не включает удаленный BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="c2fa6-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="c2fa6-160">-IncludeVersion</span></span>
<span data-ttu-id="c2fa6-161">Версии BLOB-параметров будут перечислены только в том случае, если этот параметр присутствует, по умолчанию они не включают BLOB-версии.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

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

### <span data-ttu-id="c2fa6-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c2fa6-162">-MaxCount</span></span>
<span data-ttu-id="c2fa6-163">Указывает максимальное количество объектов, возвращаемых этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="c2fa6-164">-Префикс</span><span class="sxs-lookup"><span data-stu-id="c2fa6-164">-Prefix</span></span>
<span data-ttu-id="c2fa6-165">Указывает префикс для имен BLOB-имен, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="c2fa6-166">Этот параметр не поддерживает использование регулярных выражений или поддикт-знаков для поиска.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="c2fa6-167">Это означает, что если в контейнере есть только BLOB-lob-группы "Мой", "МойBlob1" и "MyBlob2" и вы указали "-Prefix My\*", cmdlet returns no blobs.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="c2fa6-168">Однако если указать "-Префикс Мой", будет возвращены "Мой", "МойBlob1" и "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="c2fa6-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="c2fa6-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2fa6-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c2fa6-170">Для запроса указывается интервал времени, заданный для времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c2fa6-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c2fa6-171">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c2fa6-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c2fa6-172">-SnapshotTime</span></span>
<span data-ttu-id="c2fa6-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c2fa6-173">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="c2fa6-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="c2fa6-174">-VersionId</span></span>
<span data-ttu-id="c2fa6-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="c2fa6-175">Blob VersionId</span></span>

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

### <span data-ttu-id="c2fa6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fa6-176">CommonParameters</span></span>
<span data-ttu-id="c2fa6-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fa6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fa6-178">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fa6-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fa6-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fa6-179">INPUTS</span></span>

### <span data-ttu-id="c2fa6-180">System.String</span><span class="sxs-lookup"><span data-stu-id="c2fa6-180">System.String</span></span>

### <span data-ttu-id="c2fa6-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2fa6-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2fa6-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fa6-182">OUTPUTS</span></span>

### <span data-ttu-id="c2fa6-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c2fa6-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c2fa6-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2fa6-184">NOTES</span></span>

## <span data-ttu-id="c2fa6-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2fa6-185">RELATED LINKS</span></span>

[<span data-ttu-id="c2fa6-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c2fa6-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="c2fa6-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c2fa6-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="c2fa6-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c2fa6-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


