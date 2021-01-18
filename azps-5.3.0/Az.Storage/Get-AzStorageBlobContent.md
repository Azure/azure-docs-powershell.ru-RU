---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505842"
---
# <span data-ttu-id="ccf19-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ccf19-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="ccf19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf19-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf19-103">Скачивает большой объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccf19-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="ccf19-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ccf19-104">SYNTAX</span></span>

### <span data-ttu-id="ccf19-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccf19-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccf19-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ccf19-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf19-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ccf19-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf19-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccf19-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf19-109">Для **скачивания указанного BLOB-blob-blob-хранилища будет скачен cmdlet Get-AzStorageBlobContent.**</span><span class="sxs-lookup"><span data-stu-id="ccf19-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="ccf19-110">Если имя BLOB-имени не является допустимым для локального компьютера, этот cmdlet автоматически разрешит его, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ccf19-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="ccf19-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ccf19-111">EXAMPLES</span></span>

### <span data-ttu-id="ccf19-112">Пример 1. Загрузка содержимого BLOB-содержимого по имени</span><span class="sxs-lookup"><span data-stu-id="ccf19-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="ccf19-113">Эта команда скачивает BLOB-файл по имени.</span><span class="sxs-lookup"><span data-stu-id="ccf19-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="ccf19-114">Пример 2. Загрузка содержимого BLOB-содержимого с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ccf19-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="ccf19-115">Эта команда использует канал для поиска и скачивания содержимого BLOB-содержимого.</span><span class="sxs-lookup"><span data-stu-id="ccf19-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ccf19-116">Пример 3. Загрузка содержимого BLOB-содержимого с помощью конвейера и поддиавного знака</span><span class="sxs-lookup"><span data-stu-id="ccf19-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="ccf19-117">В этом примере для поиска и скачивания содержимого BLOB-содержимого используется поддеревка звездочки и конвейер.</span><span class="sxs-lookup"><span data-stu-id="ccf19-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ccf19-118">Пример 4. Получите объект BLOB-объектов и сохраните его в переменной, а затем скачайте его вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="ccf19-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="ccf19-119">В этом примере сначала получить BLOB-объект и сохранить его в переменной, а затем скачать его вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="ccf19-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="ccf19-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccf19-120">PARAMETERS</span></span>

### <span data-ttu-id="ccf19-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccf19-121">-AsJob</span></span>
<span data-ttu-id="ccf19-122">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ccf19-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ccf19-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ccf19-123">-Blob</span></span>
<span data-ttu-id="ccf19-124">Имя загружаемого BLOB-приложения.</span><span class="sxs-lookup"><span data-stu-id="ccf19-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ccf19-125">-BlobBaseClient</span></span>
<span data-ttu-id="ccf19-126">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ccf19-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ccf19-127">-CheckMd5</span></span>
<span data-ttu-id="ccf19-128">Указывает, нужно ли проверять сумму MD5 для загруженного файла.</span><span class="sxs-lookup"><span data-stu-id="ccf19-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ccf19-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ccf19-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ccf19-130">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ccf19-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ccf19-131">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="ccf19-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ccf19-132">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ccf19-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ccf19-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ccf19-133">-CloudBlob</span></span>
<span data-ttu-id="ccf19-134">Определяет облачный большой документ.</span><span class="sxs-lookup"><span data-stu-id="ccf19-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="ccf19-135">Чтобы получить объект **CloudBlob,** воспользуйтесь Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="ccf19-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ccf19-136">-CloudBlobContainer</span></span>
<span data-ttu-id="ccf19-137">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf19-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="ccf19-138">Вы можете создать его или использовать Get-AzStorageContainer- или Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ccf19-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ccf19-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ccf19-140">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ccf19-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ccf19-141">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ccf19-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ccf19-142">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="ccf19-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ccf19-143">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="ccf19-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ccf19-144">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ccf19-144">The default value is 10.</span></span>

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

### <span data-ttu-id="ccf19-145">-Container</span><span class="sxs-lookup"><span data-stu-id="ccf19-145">-Container</span></span>
<span data-ttu-id="ccf19-146">Имя контейнера с BLOB-файлом, который вы хотите скачать.</span><span class="sxs-lookup"><span data-stu-id="ccf19-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-147">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ccf19-147">-Context</span></span>
<span data-ttu-id="ccf19-148">Указывает учетную запись хранилища Azure, из которой вы хотите скачать содержимое BLOB-содержимого.</span><span class="sxs-lookup"><span data-stu-id="ccf19-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="ccf19-149">С помощью New-AzStorageContext можно создать контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccf19-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="ccf19-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf19-150">-DefaultProfile</span></span>
<span data-ttu-id="ccf19-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf19-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf19-152">-Destination</span><span class="sxs-lookup"><span data-stu-id="ccf19-152">-Destination</span></span>
<span data-ttu-id="ccf19-153">Расположение для хранения загруженного файла.</span><span class="sxs-lookup"><span data-stu-id="ccf19-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf19-154">-Force</span><span class="sxs-lookup"><span data-stu-id="ccf19-154">-Force</span></span>
<span data-ttu-id="ccf19-155">Переописает существующий файл без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ccf19-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="ccf19-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ccf19-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ccf19-157">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="ccf19-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ccf19-158">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ccf19-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ccf19-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccf19-159">-Confirm</span></span>
<span data-ttu-id="ccf19-160">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ccf19-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf19-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf19-161">-WhatIf</span></span>
<span data-ttu-id="ccf19-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccf19-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf19-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ccf19-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf19-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf19-164">CommonParameters</span></span>
<span data-ttu-id="ccf19-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf19-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf19-166">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf19-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf19-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccf19-167">INPUTS</span></span>

### <span data-ttu-id="ccf19-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ccf19-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ccf19-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ccf19-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ccf19-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ccf19-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ccf19-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ccf19-171">OUTPUTS</span></span>

### <span data-ttu-id="ccf19-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ccf19-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ccf19-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ccf19-173">NOTES</span></span>
* <span data-ttu-id="ccf19-174">Если имя BLOB-имени недопустимо для локального компьютера, этот cmdlet автоматически перезапустит его, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ccf19-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="ccf19-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccf19-175">RELATED LINKS</span></span>

[<span data-ttu-id="ccf19-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ccf19-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="ccf19-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ccf19-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ccf19-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ccf19-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
