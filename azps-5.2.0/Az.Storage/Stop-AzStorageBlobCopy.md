---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324033"
---
# <span data-ttu-id="922ff-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="922ff-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="922ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922ff-102">SYNOPSIS</span></span>
<span data-ttu-id="922ff-103">Остановка операции копирования.</span><span class="sxs-lookup"><span data-stu-id="922ff-103">Stops a copy operation.</span></span>

## <span data-ttu-id="922ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="922ff-104">SYNTAX</span></span>

### <span data-ttu-id="922ff-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="922ff-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="922ff-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="922ff-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="922ff-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="922ff-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="922ff-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="922ff-108">DESCRIPTION</span></span>
<span data-ttu-id="922ff-109">При **этом операция копирования** в указанный BLOB-проект прекращается.</span><span class="sxs-lookup"><span data-stu-id="922ff-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="922ff-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="922ff-110">EXAMPLES</span></span>

### <span data-ttu-id="922ff-111">Пример 1. Остановка копирования по имени</span><span class="sxs-lookup"><span data-stu-id="922ff-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="922ff-112">Эта команда останавливает операцию копирования по имени.</span><span class="sxs-lookup"><span data-stu-id="922ff-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="922ff-113">Пример 2. Остановка копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="922ff-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="922ff-114">Эта команда останавливает операцию копирования, передавая контейнер в конвейере из **Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="922ff-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="922ff-115">Пример 3. Остановка копирования с помощью конвейера и Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="922ff-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="922ff-116">В этом примере операция копирования прекращается, передавая контейнер в конвейере из Get-AzStorageBlob-Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="922ff-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="922ff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="922ff-117">PARAMETERS</span></span>

### <span data-ttu-id="922ff-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="922ff-118">-Blob</span></span>
<span data-ttu-id="922ff-119">Имя BLOB-адреса.</span><span class="sxs-lookup"><span data-stu-id="922ff-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="922ff-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="922ff-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="922ff-121">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="922ff-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="922ff-122">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="922ff-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="922ff-123">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="922ff-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="922ff-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="922ff-124">-CloudBlob</span></span>
<span data-ttu-id="922ff-125">Указывает объект **CloudBlob из** библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="922ff-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="922ff-126">Чтобы получить объект **CloudBlob,** воспользуйтесь Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="922ff-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="922ff-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="922ff-127">-CloudBlobContainer</span></span>
<span data-ttu-id="922ff-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="922ff-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="922ff-129">Вы можете создать объект или воспользоваться Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="922ff-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="922ff-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="922ff-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="922ff-131">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="922ff-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="922ff-132">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="922ff-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="922ff-133">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="922ff-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="922ff-134">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="922ff-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="922ff-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="922ff-135">The default value is 10.</span></span>

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

### <span data-ttu-id="922ff-136">-Container</span><span class="sxs-lookup"><span data-stu-id="922ff-136">-Container</span></span>
<span data-ttu-id="922ff-137">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="922ff-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="922ff-138">-Контекст</span><span class="sxs-lookup"><span data-stu-id="922ff-138">-Context</span></span>
<span data-ttu-id="922ff-139">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="922ff-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="922ff-140">Вы можете создать контекст с помощью New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="922ff-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="922ff-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="922ff-141">-CopyId</span></span>
<span data-ttu-id="922ff-142">Определяет копию ИД.</span><span class="sxs-lookup"><span data-stu-id="922ff-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="922ff-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922ff-143">-DefaultProfile</span></span>
<span data-ttu-id="922ff-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="922ff-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922ff-145">-Force</span><span class="sxs-lookup"><span data-stu-id="922ff-145">-Force</span></span>
<span data-ttu-id="922ff-146">Остановка текущей задачи копирования для указанного BLOB-задача без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="922ff-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="922ff-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="922ff-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="922ff-148">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="922ff-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="922ff-149">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="922ff-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="922ff-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="922ff-150">-Confirm</span></span>
<span data-ttu-id="922ff-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922ff-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922ff-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922ff-152">-WhatIf</span></span>
<span data-ttu-id="922ff-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922ff-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922ff-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="922ff-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922ff-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922ff-155">CommonParameters</span></span>
<span data-ttu-id="922ff-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922ff-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922ff-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922ff-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922ff-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="922ff-158">INPUTS</span></span>

### <span data-ttu-id="922ff-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="922ff-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="922ff-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="922ff-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="922ff-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="922ff-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="922ff-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="922ff-162">OUTPUTS</span></span>

### <span data-ttu-id="922ff-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="922ff-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="922ff-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="922ff-164">NOTES</span></span>

## <span data-ttu-id="922ff-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="922ff-165">RELATED LINKS</span></span>

[<span data-ttu-id="922ff-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="922ff-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="922ff-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="922ff-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="922ff-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="922ff-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="922ff-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="922ff-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
