---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229881"
---
# <span data-ttu-id="963e8-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="963e8-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="963e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="963e8-102">SYNOPSIS</span></span>
<span data-ttu-id="963e8-103">Применяет простую язык SQL (SQL) к содержимому BLOB-файла и сохраняет только запрашиваемую подмножество данных в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="963e8-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="963e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="963e8-104">SYNTAX</span></span>

### <span data-ttu-id="963e8-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="963e8-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="963e8-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="963e8-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="963e8-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="963e8-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="963e8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="963e8-108">DESCRIPTION</span></span>
<span data-ttu-id="963e8-109">С помощью cmdlet язык SQL (SQL) для содержимого **BLOB-содержимого get-AzStorageBlobQueryResult** можно сохранить запросы в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="963e8-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="963e8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="963e8-110">EXAMPLES</span></span>

### <span data-ttu-id="963e8-111">Пример 1. Запрос BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="963e8-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="963e8-112">Эта команда запрашивает У BLOB-файл succssfully с входными данными config в качестве CSV-файла, а выводит config в качестве json и сохраняет выходные данные в локальный c:\resultfile.js"c:\resultfile.js".</span><span class="sxs-lookup"><span data-stu-id="963e8-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="963e8-113">Пример 2. Запрос на моментальный снимок BLOB-клиента</span><span class="sxs-lookup"><span data-stu-id="963e8-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="963e8-114">Эта команда сначала получает объект BLOB-объектов для моментального снимка BLOB-объектов, а затем запрашивает его моментальный снимок и возвращает результат ошибки запроса.</span><span class="sxs-lookup"><span data-stu-id="963e8-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="963e8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="963e8-115">PARAMETERS</span></span>

### <span data-ttu-id="963e8-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="963e8-116">-Blob</span></span>
<span data-ttu-id="963e8-117">Имя BLOB-ля</span><span class="sxs-lookup"><span data-stu-id="963e8-117">Blob name</span></span>

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

### <span data-ttu-id="963e8-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="963e8-118">-BlobBaseClient</span></span>
<span data-ttu-id="963e8-119">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="963e8-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="963e8-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="963e8-120">-BlobContainerClient</span></span>
<span data-ttu-id="963e8-121">Объект BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="963e8-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="963e8-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="963e8-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="963e8-123">Максимальное время выполнения каждого запроса на стороне клиента в секундах.</span><span class="sxs-lookup"><span data-stu-id="963e8-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="963e8-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="963e8-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="963e8-125">Общий объем одновременной работы с async.</span><span class="sxs-lookup"><span data-stu-id="963e8-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="963e8-126">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="963e8-126">The default value is 10.</span></span>

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

### <span data-ttu-id="963e8-127">-Container</span><span class="sxs-lookup"><span data-stu-id="963e8-127">-Container</span></span>
<span data-ttu-id="963e8-128">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="963e8-128">Container name</span></span>

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

### <span data-ttu-id="963e8-129">-Контекст</span><span class="sxs-lookup"><span data-stu-id="963e8-129">-Context</span></span>
<span data-ttu-id="963e8-130">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="963e8-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="963e8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963e8-131">-DefaultProfile</span></span>
<span data-ttu-id="963e8-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="963e8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963e8-133">-Force</span><span class="sxs-lookup"><span data-stu-id="963e8-133">-Force</span></span>
<span data-ttu-id="963e8-134">Принудительно переопишем существующий файл.</span><span class="sxs-lookup"><span data-stu-id="963e8-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="963e8-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="963e8-135">-InputTextConfiguration</span></span>
<span data-ttu-id="963e8-136">Конфигурация, используемая для обработки входного текста запроса.</span><span class="sxs-lookup"><span data-stu-id="963e8-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="963e8-137">Создайте объект конфигурации с помощью New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="963e8-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="963e8-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="963e8-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="963e8-139">Конфигурация, используемая для обработки текста вывода запроса.</span><span class="sxs-lookup"><span data-stu-id="963e8-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="963e8-140">Создайте объект конфигурации с помощью New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="963e8-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="963e8-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="963e8-141">-PassThru</span></span>
<span data-ttu-id="963e8-142">Возвращает, успешно ли запрашивается указанный BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="963e8-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="963e8-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="963e8-143">-QueryString</span></span>
<span data-ttu-id="963e8-144">Строка запроса. Дополнительные сведения см. в: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="963e8-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="963e8-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="963e8-145">-ResultFile</span></span>
<span data-ttu-id="963e8-146">Путь к локальному файлу для сохранения результата запроса.</span><span class="sxs-lookup"><span data-stu-id="963e8-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="963e8-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="963e8-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="963e8-148">Время с часовой стрелкой для каждого запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="963e8-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="963e8-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="963e8-149">-SnapshotTime</span></span>
<span data-ttu-id="963e8-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="963e8-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="963e8-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="963e8-151">-VersionId</span></span>
<span data-ttu-id="963e8-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="963e8-152">Blob VersionId</span></span>

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

### <span data-ttu-id="963e8-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="963e8-153">-Confirm</span></span>
<span data-ttu-id="963e8-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="963e8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="963e8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="963e8-155">-WhatIf</span></span>
<span data-ttu-id="963e8-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="963e8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="963e8-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="963e8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="963e8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963e8-158">CommonParameters</span></span>
<span data-ttu-id="963e8-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963e8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963e8-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="963e8-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963e8-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="963e8-161">INPUTS</span></span>

### <span data-ttu-id="963e8-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="963e8-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="963e8-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="963e8-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="963e8-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="963e8-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="963e8-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="963e8-165">OUTPUTS</span></span>

### <span data-ttu-id="963e8-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="963e8-166">System.Boolean</span></span>

## <span data-ttu-id="963e8-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="963e8-167">NOTES</span></span>

## <span data-ttu-id="963e8-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="963e8-168">RELATED LINKS</span></span>
