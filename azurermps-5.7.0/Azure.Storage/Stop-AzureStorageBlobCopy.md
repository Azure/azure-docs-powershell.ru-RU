---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
ms.openlocfilehash: 5e21c52c1ce87ea9b030d2e4e573ad326bb04804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734199"
---
# <span data-ttu-id="27514-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27514-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="27514-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27514-102">SYNOPSIS</span></span>
<span data-ttu-id="27514-103">Останавливает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="27514-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27514-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27514-104">SYNTAX</span></span>

### <span data-ttu-id="27514-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27514-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27514-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="27514-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27514-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="27514-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27514-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27514-108">DESCRIPTION</span></span>
<span data-ttu-id="27514-109">Командлет **Stop-AzureStorageBlobCopy** останавливает операцию копирования для указанного большого двоичного объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="27514-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="27514-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27514-110">EXAMPLES</span></span>

### <span data-ttu-id="27514-111">Пример 1: Остановка копирования операции по имени</span><span class="sxs-lookup"><span data-stu-id="27514-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="27514-112">Эта команда останавливает операцию копирования по имени.</span><span class="sxs-lookup"><span data-stu-id="27514-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="27514-113">Пример 2: остановка операции копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="27514-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="27514-114">Эта команда останавливает операцию копирования, передавая контейнер на конвейер из **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="27514-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="27514-115">Пример 3: остановка операции копирования с помощью конвейера и Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="27514-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="27514-116">Этот пример останавливает операцию копирования, передавая контейнер на конвейер из командлета Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="27514-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="27514-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27514-117">PARAMETERS</span></span>

### <span data-ttu-id="27514-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="27514-118">-Blob</span></span>
<span data-ttu-id="27514-119">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="27514-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27514-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="27514-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="27514-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="27514-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="27514-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="27514-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="27514-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="27514-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="27514-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="27514-124">-CloudBlob</span></span>
<span data-ttu-id="27514-125">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27514-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="27514-126">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="27514-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27514-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="27514-127">-CloudBlobContainer</span></span>
<span data-ttu-id="27514-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27514-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="27514-129">Вы можете создать объект или использовать командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="27514-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27514-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="27514-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="27514-131">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="27514-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="27514-132">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="27514-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="27514-133">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="27514-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="27514-134">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="27514-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="27514-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="27514-135">The default value is 10.</span></span>

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

### <span data-ttu-id="27514-136">-Container</span><span class="sxs-lookup"><span data-stu-id="27514-136">-Container</span></span>
<span data-ttu-id="27514-137">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="27514-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27514-138">-Context</span><span class="sxs-lookup"><span data-stu-id="27514-138">-Context</span></span>
<span data-ttu-id="27514-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27514-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="27514-140">Контекст можно создать с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="27514-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27514-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="27514-141">-CopyId</span></span>
<span data-ttu-id="27514-142">Задает идентификатор копии.</span><span class="sxs-lookup"><span data-stu-id="27514-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27514-143">-Force</span><span class="sxs-lookup"><span data-stu-id="27514-143">-Force</span></span>
<span data-ttu-id="27514-144">Останавливает текущую задачу копирования в указанном двоичном объекте, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="27514-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="27514-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="27514-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="27514-146">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="27514-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="27514-147">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="27514-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="27514-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27514-148">-Confirm</span></span>
<span data-ttu-id="27514-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27514-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27514-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27514-150">-WhatIf</span></span>
<span data-ttu-id="27514-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27514-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27514-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27514-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27514-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27514-153">CommonParameters</span></span>
<span data-ttu-id="27514-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27514-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27514-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27514-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27514-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27514-156">INPUTS</span></span>

### <span data-ttu-id="27514-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27514-157">IStorageContext</span></span>

<span data-ttu-id="27514-158">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27514-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="27514-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27514-159">OUTPUTS</span></span>

### <span data-ttu-id="27514-160">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="27514-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="27514-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="27514-161">NOTES</span></span>

## <span data-ttu-id="27514-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27514-162">RELATED LINKS</span></span>

[<span data-ttu-id="27514-163">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="27514-163">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="27514-164">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="27514-164">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="27514-165">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27514-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="27514-166">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="27514-166">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
