---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 320de9e1dab757265d626b1df34e5049c691b7bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906926"
---
# <span data-ttu-id="cf11d-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cf11d-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="cf11d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf11d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf11d-103">Загружает большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf11d-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="cf11d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf11d-104">SYNTAX</span></span>

### <span data-ttu-id="cf11d-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf11d-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf11d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="cf11d-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf11d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="cf11d-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf11d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf11d-108">DESCRIPTION</span></span>
<span data-ttu-id="cf11d-109">Командлет **Get-AzStorageBlobContent** загружает указанный большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf11d-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="cf11d-110">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет автоматически разрешает его, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="cf11d-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="cf11d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf11d-111">EXAMPLES</span></span>

### <span data-ttu-id="cf11d-112">Пример 1: Загрузка содержимого BLOB-объектов по имени</span><span class="sxs-lookup"><span data-stu-id="cf11d-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="cf11d-113">Эта команда загружает большой двоичный объект по имени.</span><span class="sxs-lookup"><span data-stu-id="cf11d-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="cf11d-114">Пример 2: Загрузка содержимого BLOB-объектов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="cf11d-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="cf11d-115">Эта команда использует конвейер для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cf11d-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="cf11d-116">Пример 3: скачивание содержимого BLOB-объектов с помощью конвейера и подстановочного знака</span><span class="sxs-lookup"><span data-stu-id="cf11d-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="cf11d-117">В этом примере используется подстановочный знак "звездочка" и канал продаж для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cf11d-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="cf11d-118">Пример 4: получение объекта BLOB и его сохранение в переменной, затем Загрузка содержимого BLOB-объектов с помощью объекта BLOB</span><span class="sxs-lookup"><span data-stu-id="cf11d-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="cf11d-119">В этом примере сначала нужно получить объект BLOB и сохранить его в переменной, а затем загрузить содержимое BLOB-объектов с помощью объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="cf11d-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="cf11d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf11d-120">PARAMETERS</span></span>

### <span data-ttu-id="cf11d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf11d-121">-AsJob</span></span>
<span data-ttu-id="cf11d-122">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cf11d-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cf11d-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="cf11d-123">-Blob</span></span>
<span data-ttu-id="cf11d-124">Указывает имя большого двоичного объекта, который нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="cf11d-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="cf11d-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="cf11d-125">-CheckMd5</span></span>
<span data-ttu-id="cf11d-126">Указывает, следует ли проверять сумму Md5 для скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="cf11d-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="cf11d-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf11d-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf11d-128">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="cf11d-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf11d-129">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="cf11d-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf11d-130">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf11d-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf11d-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cf11d-131">-CloudBlob</span></span>
<span data-ttu-id="cf11d-132">Задает большой двоичный объект облака.</span><span class="sxs-lookup"><span data-stu-id="cf11d-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="cf11d-133">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="cf11d-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="cf11d-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cf11d-134">-CloudBlobContainer</span></span>
<span data-ttu-id="cf11d-135">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cf11d-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="cf11d-136">Вы можете создать его или воспользоваться командлетом Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="cf11d-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="cf11d-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf11d-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf11d-138">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="cf11d-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf11d-139">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="cf11d-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf11d-140">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="cf11d-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf11d-141">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="cf11d-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf11d-142">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="cf11d-142">The default value is 10.</span></span>

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

### <span data-ttu-id="cf11d-143">-Container</span><span class="sxs-lookup"><span data-stu-id="cf11d-143">-Container</span></span>
<span data-ttu-id="cf11d-144">Указывает имя контейнера, в котором есть большой двоичный объект, который вы хотите скачать.</span><span class="sxs-lookup"><span data-stu-id="cf11d-144">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="cf11d-145">-Context</span><span class="sxs-lookup"><span data-stu-id="cf11d-145">-Context</span></span>
<span data-ttu-id="cf11d-146">Указывает учетную запись хранения Azure, из которой вы хотите скачать содержимое BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cf11d-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="cf11d-147">Вы можете использовать командлет New-AzStorageContext для создания контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf11d-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="cf11d-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf11d-148">-DefaultProfile</span></span>
<span data-ttu-id="cf11d-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf11d-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf11d-150">-Destination</span><span class="sxs-lookup"><span data-stu-id="cf11d-150">-Destination</span></span>
<span data-ttu-id="cf11d-151">Указывает место для хранения скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="cf11d-151">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="cf11d-152">-Force</span><span class="sxs-lookup"><span data-stu-id="cf11d-152">-Force</span></span>
<span data-ttu-id="cf11d-153">Перезаписывает существующий файл без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cf11d-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="cf11d-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf11d-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf11d-155">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="cf11d-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cf11d-156">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf11d-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cf11d-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf11d-157">-Confirm</span></span>
<span data-ttu-id="cf11d-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf11d-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf11d-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf11d-159">-WhatIf</span></span>
<span data-ttu-id="cf11d-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf11d-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf11d-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf11d-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf11d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf11d-162">CommonParameters</span></span>
<span data-ttu-id="cf11d-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf11d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf11d-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf11d-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf11d-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf11d-165">INPUTS</span></span>

### <span data-ttu-id="cf11d-166">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cf11d-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cf11d-167">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cf11d-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cf11d-168">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cf11d-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf11d-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf11d-169">OUTPUTS</span></span>

### <span data-ttu-id="cf11d-170">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf11d-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cf11d-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf11d-171">NOTES</span></span>
* <span data-ttu-id="cf11d-172">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет по возможности разрешает его.</span><span class="sxs-lookup"><span data-stu-id="cf11d-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="cf11d-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf11d-173">RELATED LINKS</span></span>

[<span data-ttu-id="cf11d-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cf11d-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="cf11d-175">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf11d-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="cf11d-176">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cf11d-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
