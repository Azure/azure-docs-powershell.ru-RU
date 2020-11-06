---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559404"
---
# <span data-ttu-id="29aa3-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="29aa3-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="29aa3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="29aa3-103">Список больших двоичных объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="29aa3-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29aa3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29aa3-104">SYNTAX</span></span>

### <span data-ttu-id="29aa3-105">BlobName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29aa3-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="29aa3-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="29aa3-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="29aa3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="29aa3-108">Командлет **Get-AzureStorageBlob** перечисляет большие двоичные объекты в указанном контейнере в учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="29aa3-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="29aa3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29aa3-109">EXAMPLES</span></span>

### <span data-ttu-id="29aa3-110">Пример 1: получение большого двоичного объекта по имени BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="29aa3-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="29aa3-111">Эта команда использует имя большого двоичного объекта и подстановочный знак для получения большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="29aa3-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="29aa3-112">Пример 2: получение больших двоичных объектов в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="29aa3-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

<span data-ttu-id="29aa3-113">Эта команда использует конвейер для получения всех больших двоичных объектов (включая BLOB-объекты в удаленном состоянии) в контейнере.</span><span class="sxs-lookup"><span data-stu-id="29aa3-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="29aa3-114">Пример 3: Получение двоичных BLOB-имен с помощью префикса</span><span class="sxs-lookup"><span data-stu-id="29aa3-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="29aa3-115">Эта команда использует префикс имени для получения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="29aa3-116">Пример 4: список больших двоичных объектов в нескольких пакетах</span><span class="sxs-lookup"><span data-stu-id="29aa3-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="29aa3-117">В этом примере параметры *maxcount* и *ContinuationToken* используются для перечисления больших двоичных объектов хранилища Azure в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="29aa3-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="29aa3-118">Первые четыре команды назначают значения переменным для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="29aa3-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="29aa3-119">Пятая команда задает оператор **Do-** in, использующий командлет **Get-AzureStorageBlob** для получения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="29aa3-120">Оператор включает токен продолжения, хранящийся в переменной $Token.</span><span class="sxs-lookup"><span data-stu-id="29aa3-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="29aa3-121">$Token изменения значения по мере выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="29aa3-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="29aa3-122">Для получения дополнительных сведений введите `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="29aa3-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="29aa3-123">В последней команде используется команда **echo** для отображения итогового значения.</span><span class="sxs-lookup"><span data-stu-id="29aa3-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="29aa3-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29aa3-124">PARAMETERS</span></span>

### <span data-ttu-id="29aa3-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="29aa3-125">-Blob</span></span>
<span data-ttu-id="29aa3-126">Указывает имя или шаблон имени, которые можно использовать для поиска с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="29aa3-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="29aa3-127">Если имя BLOB-объектов не указано, командлет выводит список всех больших двоичных объектов в указанном контейнере.</span><span class="sxs-lookup"><span data-stu-id="29aa3-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="29aa3-128">Если для этого параметра задано значение, командлет выводит список всех больших двоичных объектов с именами, которые соответствуют этому параметру.</span><span class="sxs-lookup"><span data-stu-id="29aa3-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="29aa3-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29aa3-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="29aa3-130">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="29aa3-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="29aa3-131">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="29aa3-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="29aa3-132">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="29aa3-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="29aa3-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29aa3-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29aa3-134">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="29aa3-135">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="29aa3-136">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="29aa3-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="29aa3-137">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="29aa3-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="29aa3-138">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="29aa3-138">The default value is 10.</span></span>

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

### <span data-ttu-id="29aa3-139">-Container</span><span class="sxs-lookup"><span data-stu-id="29aa3-139">-Container</span></span>
<span data-ttu-id="29aa3-140">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="29aa3-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29aa3-141">-Context</span><span class="sxs-lookup"><span data-stu-id="29aa3-141">-Context</span></span>
<span data-ttu-id="29aa3-142">Указывает учетную запись хранения Azure, из которой вы хотите получить список больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="29aa3-143">Вы можете использовать командлет New-AzureStorageContext для создания контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="29aa3-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="29aa3-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="29aa3-144">-ContinuationToken</span></span>
<span data-ttu-id="29aa3-145">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="29aa3-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="29aa3-146">Используйте этот параметр и параметр *maxcount* для перечисления BLOB-объектов в нескольких пакетах.</span><span class="sxs-lookup"><span data-stu-id="29aa3-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29aa3-147">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="29aa3-147">-IncludeDeleted</span></span>
<span data-ttu-id="29aa3-148">Включить удаленную подбольшой двоичный объект. по умолчанию для BLOB-объектов Get не указан удаленный блоб.</span><span class="sxs-lookup"><span data-stu-id="29aa3-148">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="29aa3-149">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="29aa3-149">-MaxCount</span></span>
<span data-ttu-id="29aa3-150">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="29aa3-150">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="29aa3-151">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="29aa3-151">-Prefix</span></span>
<span data-ttu-id="29aa3-152">Задает префикс для имен больших двоичных объектов, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="29aa3-152">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="29aa3-153">Этот параметр не поддерживает использование регулярных выражений и подстановочных знаков для поиска.</span><span class="sxs-lookup"><span data-stu-id="29aa3-153">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="29aa3-154">Это означает, что если контейнер содержит только большие двоичные объекты с именами "My", "MyBlob1" и "MyBlob2", а вы указали "-prefix My \*", командлет не вернет BLOB-объекты.</span><span class="sxs-lookup"><span data-stu-id="29aa3-154">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="29aa3-155">Тем не менее, если указать "-prefix My", командлет возвращает "My", "MyBlob1" и "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="29aa3-155">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29aa3-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29aa3-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="29aa3-157">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="29aa3-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="29aa3-158">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="29aa3-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="29aa3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29aa3-159">CommonParameters</span></span>
<span data-ttu-id="29aa3-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29aa3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29aa3-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29aa3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29aa3-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29aa3-162">INPUTS</span></span>

### <span data-ttu-id="29aa3-163">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29aa3-163">IStorageContext</span></span>
<span data-ttu-id="29aa3-164">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="29aa3-164">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="29aa3-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29aa3-165">OUTPUTS</span></span>

### <span data-ttu-id="29aa3-166">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="29aa3-166">AzureStorageBlob</span></span>

## <span data-ttu-id="29aa3-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="29aa3-167">NOTES</span></span>

## <span data-ttu-id="29aa3-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29aa3-168">RELATED LINKS</span></span>

[<span data-ttu-id="29aa3-169">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="29aa3-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="29aa3-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="29aa3-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="29aa3-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="29aa3-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


