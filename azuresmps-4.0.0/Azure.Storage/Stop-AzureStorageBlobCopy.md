---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556344"
---
# <span data-ttu-id="b5ac2-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b5ac2-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="b5ac2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ac2-103">Останавливает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-103">Stops a copy operation.</span></span>

## <span data-ttu-id="b5ac2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5ac2-104">SYNTAX</span></span>

### <span data-ttu-id="b5ac2-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5ac2-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ac2-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b5ac2-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ac2-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b5ac2-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ac2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="b5ac2-109">Командлет **Stop-AzureStorageBlobCopy** останавливает операцию копирования для указанного большого двоичного объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="b5ac2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5ac2-110">EXAMPLES</span></span>

### <span data-ttu-id="b5ac2-111">Пример 1: Остановка копирования операции по имени</span><span class="sxs-lookup"><span data-stu-id="b5ac2-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="b5ac2-112">Эта команда останавливает операцию копирования по имени.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="b5ac2-113">Пример 2: остановка операции копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="b5ac2-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="b5ac2-114">Эта команда останавливает операцию копирования, передавая контейнер на конвейер из **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="b5ac2-115">Пример 3: остановка операции копирования с помощью конвейера и Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b5ac2-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="b5ac2-116">Этот пример останавливает операцию копирования, передавая контейнер на конвейер из командлета Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="b5ac2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5ac2-117">PARAMETERS</span></span>

### <span data-ttu-id="b5ac2-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b5ac2-118">-Blob</span></span>
<span data-ttu-id="b5ac2-119">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="b5ac2-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5ac2-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b5ac2-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b5ac2-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b5ac2-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b5ac2-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b5ac2-124">-CloudBlob</span></span>
<span data-ttu-id="b5ac2-125">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="b5ac2-126">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b5ac2-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b5ac2-127">-CloudBlobContainer</span></span>
<span data-ttu-id="b5ac2-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b5ac2-129">Вы можете создать объект или использовать командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b5ac2-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5ac2-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5ac2-131">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b5ac2-132">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b5ac2-133">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b5ac2-134">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b5ac2-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-135">The default value is 10.</span></span>

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

### <span data-ttu-id="b5ac2-136">-Container</span><span class="sxs-lookup"><span data-stu-id="b5ac2-136">-Container</span></span>
<span data-ttu-id="b5ac2-137">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b5ac2-138">-Context</span><span class="sxs-lookup"><span data-stu-id="b5ac2-138">-Context</span></span>
<span data-ttu-id="b5ac2-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b5ac2-140">Контекст можно создать с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b5ac2-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="b5ac2-141">-CopyId</span></span>
<span data-ttu-id="b5ac2-142">Задает идентификатор копии.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="b5ac2-143">-Force</span><span class="sxs-lookup"><span data-stu-id="b5ac2-143">-Force</span></span>
<span data-ttu-id="b5ac2-144">Останавливает текущую задачу копирования в указанном двоичном объекте, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b5ac2-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5ac2-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b5ac2-146">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b5ac2-147">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b5ac2-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5ac2-148">-Confirm</span></span>
<span data-ttu-id="b5ac2-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ac2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ac2-150">-WhatIf</span></span>
<span data-ttu-id="b5ac2-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ac2-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ac2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ac2-153">CommonParameters</span></span>
<span data-ttu-id="b5ac2-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5ac2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ac2-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ac2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ac2-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5ac2-156">INPUTS</span></span>

## <span data-ttu-id="b5ac2-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ac2-157">OUTPUTS</span></span>

## <span data-ttu-id="b5ac2-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5ac2-158">NOTES</span></span>

## <span data-ttu-id="b5ac2-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5ac2-159">RELATED LINKS</span></span>

[<span data-ttu-id="b5ac2-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b5ac2-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b5ac2-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b5ac2-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="b5ac2-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b5ac2-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="b5ac2-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="b5ac2-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
