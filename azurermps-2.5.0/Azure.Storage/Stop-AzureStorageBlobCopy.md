---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
ms.openlocfilehash: 2a338773ae8745ae6412014bfd176e5b29fa380f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913931"
---
# <span data-ttu-id="ebf2b-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ebf2b-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="ebf2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebf2b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf2b-103">Останавливает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebf2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebf2b-104">SYNTAX</span></span>

### <span data-ttu-id="ebf2b-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebf2b-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebf2b-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ebf2b-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebf2b-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ebf2b-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebf2b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf2b-108">DESCRIPTION</span></span>
<span data-ttu-id="ebf2b-109">Командлет **Stop-AzureStorageBlobCopy** останавливает операцию копирования для указанного большого двоичного объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="ebf2b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebf2b-110">EXAMPLES</span></span>

### <span data-ttu-id="ebf2b-111">Пример 1: Остановка копирования операции по имени</span><span class="sxs-lookup"><span data-stu-id="ebf2b-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="ebf2b-112">Эта команда останавливает операцию копирования по имени.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="ebf2b-113">Пример 2: остановка операции копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ebf2b-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="ebf2b-114">Эта команда останавливает операцию копирования, передавая контейнер на конвейер из **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="ebf2b-115">Пример 3: остановка операции копирования с помощью конвейера и Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ebf2b-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="ebf2b-116">Этот пример останавливает операцию копирования, передавая контейнер на конвейер из командлета Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="ebf2b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebf2b-117">PARAMETERS</span></span>

### <span data-ttu-id="ebf2b-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ebf2b-118">-Blob</span></span>
<span data-ttu-id="ebf2b-119">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="ebf2b-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebf2b-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ebf2b-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ebf2b-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ebf2b-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ebf2b-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ebf2b-124">-CloudBlob</span></span>
<span data-ttu-id="ebf2b-125">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="ebf2b-126">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ebf2b-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ebf2b-127">-CloudBlobContainer</span></span>
<span data-ttu-id="ebf2b-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ebf2b-129">Вы можете создать объект или использовать командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="ebf2b-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ebf2b-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ebf2b-131">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ebf2b-132">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ebf2b-133">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ebf2b-134">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ebf2b-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-135">The default value is 10.</span></span>

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

### <span data-ttu-id="ebf2b-136">-Container</span><span class="sxs-lookup"><span data-stu-id="ebf2b-136">-Container</span></span>
<span data-ttu-id="ebf2b-137">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="ebf2b-138">-Context</span><span class="sxs-lookup"><span data-stu-id="ebf2b-138">-Context</span></span>
<span data-ttu-id="ebf2b-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ebf2b-140">Контекст можно создать с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ebf2b-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="ebf2b-141">-CopyId</span></span>
<span data-ttu-id="ebf2b-142">Задает идентификатор копии.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="ebf2b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2b-143">-DefaultProfile</span></span>
<span data-ttu-id="ebf2b-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf2b-145">-Force</span><span class="sxs-lookup"><span data-stu-id="ebf2b-145">-Force</span></span>
<span data-ttu-id="ebf2b-146">Останавливает текущую задачу копирования в указанном двоичном объекте, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ebf2b-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebf2b-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ebf2b-148">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ebf2b-149">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ebf2b-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebf2b-150">-Confirm</span></span>
<span data-ttu-id="ebf2b-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf2b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf2b-152">-WhatIf</span></span>
<span data-ttu-id="ebf2b-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf2b-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf2b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf2b-155">CommonParameters</span></span>
<span data-ttu-id="ebf2b-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebf2b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf2b-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf2b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf2b-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebf2b-158">INPUTS</span></span>

### <span data-ttu-id="ebf2b-159">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ebf2b-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ebf2b-160">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ebf2b-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ebf2b-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ebf2b-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ebf2b-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf2b-162">OUTPUTS</span></span>

### <span data-ttu-id="ebf2b-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ebf2b-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ebf2b-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebf2b-164">NOTES</span></span>

## <span data-ttu-id="ebf2b-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebf2b-165">RELATED LINKS</span></span>

[<span data-ttu-id="ebf2b-166">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ebf2b-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ebf2b-167">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ebf2b-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ebf2b-168">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ebf2b-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="ebf2b-169">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="ebf2b-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
