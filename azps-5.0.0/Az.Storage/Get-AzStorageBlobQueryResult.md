---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246014"
---
# <span data-ttu-id="f8672-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="f8672-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="f8672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8672-102">SYNOPSIS</span></span>
<span data-ttu-id="f8672-103">Применяет инструкцию SQL для простого структурированного запроса и сохраняет только запрашиваемое подмножество данных в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="f8672-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="f8672-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8672-104">SYNTAX</span></span>

### <span data-ttu-id="f8672-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8672-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8672-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="f8672-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8672-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="f8672-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8672-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8672-108">DESCRIPTION</span></span>
<span data-ttu-id="f8672-109">Командлет **Get-AzStorageBlobQueryResult** применяет простой оператор структурированного запроса (SQL) к содержимому BLOB-объектов и сохраняет запрашиваемое подмножество данных в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="f8672-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="f8672-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8672-110">EXAMPLES</span></span>

### <span data-ttu-id="f8672-111">Пример 1: запрос больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="f8672-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="f8672-112">Эта команда запрашивает большой двоичный объект succsssfully с параметром input config as CSV, а выходной файл конфигурации — в формате JSON и сохраняет выходные данные в локальный файл "c:\resultfile.json".</span><span class="sxs-lookup"><span data-stu-id="f8672-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="f8672-113">Пример 2: запрос моментального снимка большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="f8672-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="f8672-114">Эта команда сначала получает объект BLOB для моментального снимка BLOB, затем запрашивает снимок большого двоичного объекта и отображает результат ошибки запроса включения.</span><span class="sxs-lookup"><span data-stu-id="f8672-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="f8672-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8672-115">PARAMETERS</span></span>

### <span data-ttu-id="f8672-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="f8672-116">-Blob</span></span>
<span data-ttu-id="f8672-117">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="f8672-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="f8672-118">-BlobBaseClient</span></span>
<span data-ttu-id="f8672-119">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="f8672-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="f8672-120">-BlobContainerClient</span></span>
<span data-ttu-id="f8672-121">Объект BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="f8672-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8672-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f8672-123">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="f8672-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="f8672-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f8672-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f8672-125">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="f8672-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="f8672-126">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f8672-126">The default value is 10.</span></span>

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

### <span data-ttu-id="f8672-127">-Container</span><span class="sxs-lookup"><span data-stu-id="f8672-127">-Container</span></span>
<span data-ttu-id="f8672-128">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="f8672-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-129">-Context</span><span class="sxs-lookup"><span data-stu-id="f8672-129">-Context</span></span>
<span data-ttu-id="f8672-130">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="f8672-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f8672-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8672-131">-DefaultProfile</span></span>
<span data-ttu-id="f8672-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8672-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8672-133">-Force</span><span class="sxs-lookup"><span data-stu-id="f8672-133">-Force</span></span>
<span data-ttu-id="f8672-134">Принудительно перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="f8672-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="f8672-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8672-135">-InputTextConfiguration</span></span>
<span data-ttu-id="f8672-136">Конфигурация, используемая для обработки ввода текста запроса.</span><span class="sxs-lookup"><span data-stu-id="f8672-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="f8672-137">Создайте объект конфигурации с помощью New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="f8672-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8672-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="f8672-139">Конфигурация, используемая для обработки текста вывода запроса.</span><span class="sxs-lookup"><span data-stu-id="f8672-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="f8672-140">Создайте объект конфигурации с помощью New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="f8672-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8672-141">-PassThru</span></span>
<span data-ttu-id="f8672-142">Возвращает значение, указывающее, успешно ли запрашивается указанный двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="f8672-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="f8672-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="f8672-143">-QueryString</span></span>
<span data-ttu-id="f8672-144">Строке запроса ознакомьтесь с дополнительными сведениями в следующих случаях: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="f8672-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="f8672-145">-ResultFile</span></span>
<span data-ttu-id="f8672-146">Локальный путь к файлу для сохранения результата запроса.</span><span class="sxs-lookup"><span data-stu-id="f8672-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f8672-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f8672-148">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="f8672-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="f8672-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="f8672-149">-SnapshotTime</span></span>
<span data-ttu-id="f8672-150">SnapshotTime больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="f8672-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="f8672-151">-VersionId</span></span>
<span data-ttu-id="f8672-152">VersionId BLOB</span><span class="sxs-lookup"><span data-stu-id="f8672-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8672-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8672-153">-Confirm</span></span>
<span data-ttu-id="f8672-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8672-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8672-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8672-155">-WhatIf</span></span>
<span data-ttu-id="f8672-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8672-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8672-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8672-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8672-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8672-158">CommonParameters</span></span>
<span data-ttu-id="f8672-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8672-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8672-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8672-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8672-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8672-161">INPUTS</span></span>

### <span data-ttu-id="f8672-162">Azure. Storage. BLOB. специализированные. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="f8672-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="f8672-163">Azure. Storage. BLOB. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="f8672-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="f8672-164">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8672-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f8672-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8672-165">OUTPUTS</span></span>

### <span data-ttu-id="f8672-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8672-166">System.Boolean</span></span>

## <span data-ttu-id="f8672-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8672-167">NOTES</span></span>

## <span data-ttu-id="f8672-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8672-168">RELATED LINKS</span></span>
