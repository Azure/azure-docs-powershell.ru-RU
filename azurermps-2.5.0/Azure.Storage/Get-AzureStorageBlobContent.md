---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
ms.openlocfilehash: 4b48e4c2e1184c26fd7b50a05e979fad1a61bf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913951"
---
# <span data-ttu-id="ea500-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ea500-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="ea500-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea500-102">SYNOPSIS</span></span>
<span data-ttu-id="ea500-103">Загружает большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="ea500-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea500-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea500-104">SYNTAX</span></span>

### <span data-ttu-id="ea500-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea500-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea500-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ea500-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea500-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ea500-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea500-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea500-108">DESCRIPTION</span></span>
<span data-ttu-id="ea500-109">Командлет **Get-AzureStorageBlobContent** загружает указанный большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="ea500-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="ea500-110">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет автоматически разрешает его, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ea500-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="ea500-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea500-111">EXAMPLES</span></span>

### <span data-ttu-id="ea500-112">Пример 1: Загрузка содержимого BLOB-объектов по имени</span><span class="sxs-lookup"><span data-stu-id="ea500-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="ea500-113">Эта команда загружает большой двоичный объект по имени.</span><span class="sxs-lookup"><span data-stu-id="ea500-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="ea500-114">Пример 2: Загрузка содержимого BLOB-объектов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ea500-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="ea500-115">Эта команда использует конвейер для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ea500-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ea500-116">Пример 3: скачивание содержимого BLOB-объектов с помощью конвейера и подстановочного знака</span><span class="sxs-lookup"><span data-stu-id="ea500-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="ea500-117">В этом примере используется подстановочный знак "звездочка" и канал продаж для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ea500-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="ea500-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea500-118">PARAMETERS</span></span>

### <span data-ttu-id="ea500-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ea500-119">-Blob</span></span>
<span data-ttu-id="ea500-120">Указывает имя большого двоичного объекта, который нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="ea500-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="ea500-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ea500-121">-CheckMd5</span></span>
<span data-ttu-id="ea500-122">Указывает, следует ли проверять сумму Md5 для скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="ea500-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ea500-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea500-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ea500-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ea500-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ea500-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ea500-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ea500-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ea500-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ea500-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ea500-127">-CloudBlob</span></span>
<span data-ttu-id="ea500-128">Задает большой двоичный объект облака.</span><span class="sxs-lookup"><span data-stu-id="ea500-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="ea500-129">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ea500-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea500-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ea500-130">-CloudBlobContainer</span></span>
<span data-ttu-id="ea500-131">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ea500-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="ea500-132">Вы можете создать его или воспользоваться командлетом Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ea500-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea500-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ea500-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ea500-134">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ea500-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ea500-135">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ea500-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ea500-136">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ea500-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ea500-137">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ea500-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ea500-138">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ea500-138">The default value is 10.</span></span>
<span data-ttu-id="ea500-139">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ea500-139">The default value is 10.</span></span>

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

### <span data-ttu-id="ea500-140">-Container</span><span class="sxs-lookup"><span data-stu-id="ea500-140">-Container</span></span>
<span data-ttu-id="ea500-141">Указывает имя контейнера, в котором есть большой двоичный объект, который вы хотите скачать.</span><span class="sxs-lookup"><span data-stu-id="ea500-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="ea500-142">-Context</span><span class="sxs-lookup"><span data-stu-id="ea500-142">-Context</span></span>
<span data-ttu-id="ea500-143">Указывает учетную запись хранения Azure, из которой вы хотите скачать содержимое BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ea500-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="ea500-144">Вы можете использовать командлет New-AzureStorageContext для создания контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="ea500-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="ea500-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea500-145">-DefaultProfile</span></span>
<span data-ttu-id="ea500-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea500-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea500-147">-Destination</span><span class="sxs-lookup"><span data-stu-id="ea500-147">-Destination</span></span>
<span data-ttu-id="ea500-148">Указывает место для хранения скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="ea500-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="ea500-149">-Force</span><span class="sxs-lookup"><span data-stu-id="ea500-149">-Force</span></span>
<span data-ttu-id="ea500-150">Перезаписывает существующий файл без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ea500-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="ea500-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea500-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ea500-152">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="ea500-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ea500-153">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ea500-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ea500-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea500-154">-Confirm</span></span>
<span data-ttu-id="ea500-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea500-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea500-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea500-156">-WhatIf</span></span>
<span data-ttu-id="ea500-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea500-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea500-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea500-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea500-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea500-159">CommonParameters</span></span>
<span data-ttu-id="ea500-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea500-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea500-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea500-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea500-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea500-162">INPUTS</span></span>

### <span data-ttu-id="ea500-163">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ea500-163">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ea500-164">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ea500-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ea500-165">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ea500-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ea500-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea500-166">OUTPUTS</span></span>

### <span data-ttu-id="ea500-167">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ea500-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ea500-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea500-168">NOTES</span></span>
* <span data-ttu-id="ea500-169">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет по возможности разрешает его.</span><span class="sxs-lookup"><span data-stu-id="ea500-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="ea500-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea500-170">RELATED LINKS</span></span>

[<span data-ttu-id="ea500-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ea500-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="ea500-172">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ea500-172">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ea500-173">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ea500-173">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
