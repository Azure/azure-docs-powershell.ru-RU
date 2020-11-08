---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065971"
---
# <span data-ttu-id="4ea25-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ea25-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="4ea25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ea25-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea25-103">Останавливает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="4ea25-103">Stops a copy operation.</span></span>

## <span data-ttu-id="4ea25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ea25-104">SYNTAX</span></span>

### <span data-ttu-id="4ea25-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ea25-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ea25-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="4ea25-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ea25-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="4ea25-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ea25-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea25-108">DESCRIPTION</span></span>
<span data-ttu-id="4ea25-109">Командлет **Stop-AzStorageBlobCopy** останавливает операцию копирования для указанного большого двоичного объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="4ea25-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="4ea25-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ea25-110">EXAMPLES</span></span>

### <span data-ttu-id="4ea25-111">Пример 1: Остановка копирования операции по имени</span><span class="sxs-lookup"><span data-stu-id="4ea25-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="4ea25-112">Эта команда останавливает операцию копирования по имени.</span><span class="sxs-lookup"><span data-stu-id="4ea25-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="4ea25-113">Пример 2: остановка операции копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="4ea25-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="4ea25-114">Эта команда останавливает операцию копирования, передавая контейнер на конвейер из **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="4ea25-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="4ea25-115">Пример 3: остановка операции копирования с помощью конвейера и Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ea25-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="4ea25-116">Этот пример останавливает операцию копирования, передавая контейнер на конвейер из командлета Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="4ea25-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="4ea25-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ea25-117">PARAMETERS</span></span>

### <span data-ttu-id="4ea25-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4ea25-118">-Blob</span></span>
<span data-ttu-id="4ea25-119">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea25-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="4ea25-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ea25-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4ea25-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4ea25-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4ea25-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="4ea25-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4ea25-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4ea25-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4ea25-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4ea25-124">-CloudBlob</span></span>
<span data-ttu-id="4ea25-125">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea25-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="4ea25-126">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="4ea25-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="4ea25-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4ea25-127">-CloudBlobContainer</span></span>
<span data-ttu-id="4ea25-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea25-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4ea25-129">Вы можете создать объект или использовать командлет Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="4ea25-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="4ea25-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4ea25-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4ea25-131">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4ea25-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4ea25-132">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4ea25-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4ea25-133">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="4ea25-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4ea25-134">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="4ea25-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4ea25-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4ea25-135">The default value is 10.</span></span>

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

### <span data-ttu-id="4ea25-136">-Container</span><span class="sxs-lookup"><span data-stu-id="4ea25-136">-Container</span></span>
<span data-ttu-id="4ea25-137">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="4ea25-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4ea25-138">-Context</span><span class="sxs-lookup"><span data-stu-id="4ea25-138">-Context</span></span>
<span data-ttu-id="4ea25-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea25-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4ea25-140">Контекст можно создать с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4ea25-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4ea25-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="4ea25-141">-CopyId</span></span>
<span data-ttu-id="4ea25-142">Задает идентификатор копии.</span><span class="sxs-lookup"><span data-stu-id="4ea25-142">Specifies the copy ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea25-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea25-143">-DefaultProfile</span></span>
<span data-ttu-id="4ea25-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea25-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea25-145">-Force</span><span class="sxs-lookup"><span data-stu-id="4ea25-145">-Force</span></span>
<span data-ttu-id="4ea25-146">Останавливает текущую задачу копирования в указанном двоичном объекте, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4ea25-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4ea25-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ea25-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4ea25-148">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="4ea25-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4ea25-149">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4ea25-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4ea25-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea25-150">-Confirm</span></span>
<span data-ttu-id="4ea25-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ea25-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea25-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea25-152">-WhatIf</span></span>
<span data-ttu-id="4ea25-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ea25-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea25-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ea25-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea25-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea25-155">CommonParameters</span></span>
<span data-ttu-id="4ea25-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ea25-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea25-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea25-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea25-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ea25-158">INPUTS</span></span>

### <span data-ttu-id="4ea25-159">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4ea25-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4ea25-160">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4ea25-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4ea25-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ea25-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ea25-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea25-162">OUTPUTS</span></span>

### <span data-ttu-id="4ea25-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ea25-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="4ea25-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ea25-164">NOTES</span></span>

## <span data-ttu-id="4ea25-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ea25-165">RELATED LINKS</span></span>

[<span data-ttu-id="4ea25-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ea25-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="4ea25-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4ea25-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="4ea25-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ea25-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="4ea25-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="4ea25-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
