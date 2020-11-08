---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077510"
---
# <span data-ttu-id="c283a-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c283a-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="c283a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c283a-102">SYNOPSIS</span></span>
<span data-ttu-id="c283a-103">Удаляет указанный большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="c283a-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="c283a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c283a-104">SYNTAX</span></span>

### <span data-ttu-id="c283a-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c283a-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c283a-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c283a-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c283a-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c283a-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c283a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c283a-108">DESCRIPTION</span></span>
<span data-ttu-id="c283a-109">Командлет **Remove-AzStorageBlob** удаляет указанный большой двоичный объект из учетной записи хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="c283a-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="c283a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c283a-110">EXAMPLES</span></span>

### <span data-ttu-id="c283a-111">Пример 1: удаление BLOB-объекта хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="c283a-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="c283a-112">Эта команда удаляет большой двоичный объект, идентифицированный по его имени.</span><span class="sxs-lookup"><span data-stu-id="c283a-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="c283a-113">Пример 2: удаление большого двоичного объекта хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c283a-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="c283a-114">В этой команде используется конвейер.</span><span class="sxs-lookup"><span data-stu-id="c283a-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="c283a-115">Пример 3: удаление больших двоичных объектов хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c283a-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="c283a-116">Эта команда использует подстановочный знак "звездочка" (\*) и конвейер для извлечения BLOB-объектов или больших двоичных объектов, а затем удаляет их.</span><span class="sxs-lookup"><span data-stu-id="c283a-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="c283a-117">Пример 4: удаление единственной версии большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="c283a-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="c283a-118">Эта команда удаляет один и тот же BLOB-объект, verion с VersionId.</span><span class="sxs-lookup"><span data-stu-id="c283a-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="c283a-119">Пример 5: Удаление одного снимка большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="c283a-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="c283a-120">Эта команда удаляет один снимок больших двоичных объектов с помощью SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="c283a-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="c283a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c283a-121">PARAMETERS</span></span>

### <span data-ttu-id="c283a-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c283a-122">-Blob</span></span>
<span data-ttu-id="c283a-123">Указывает имя большого двоичного объекта, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="c283a-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="c283a-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c283a-124">-BlobBaseClient</span></span>
<span data-ttu-id="c283a-125">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c283a-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="c283a-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c283a-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c283a-127">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c283a-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c283a-128">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="c283a-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c283a-129">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c283a-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c283a-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c283a-130">-CloudBlob</span></span>
<span data-ttu-id="c283a-131">Задает большой двоичный объект облака.</span><span class="sxs-lookup"><span data-stu-id="c283a-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="c283a-132">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="c283a-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="c283a-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c283a-133">-CloudBlobContainer</span></span>
<span data-ttu-id="c283a-134">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c283a-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="c283a-135">Вы можете использовать командлет Get-AzStorageContainer, чтобы получить его.</span><span class="sxs-lookup"><span data-stu-id="c283a-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="c283a-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c283a-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c283a-137">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c283a-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c283a-138">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c283a-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c283a-139">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="c283a-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c283a-140">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="c283a-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c283a-141">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c283a-141">The default value is 10.</span></span>

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

### <span data-ttu-id="c283a-142">-Container</span><span class="sxs-lookup"><span data-stu-id="c283a-142">-Container</span></span>
<span data-ttu-id="c283a-143">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c283a-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="c283a-144">-Context</span><span class="sxs-lookup"><span data-stu-id="c283a-144">-Context</span></span>
<span data-ttu-id="c283a-145">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c283a-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c283a-146">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c283a-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="c283a-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c283a-147">-DefaultProfile</span></span>
<span data-ttu-id="c283a-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c283a-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c283a-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="c283a-149">-DeleteSnapshot</span></span>
<span data-ttu-id="c283a-150">Указывает, что все моментальные снимки удаляются, но не базовый блоб.</span><span class="sxs-lookup"><span data-stu-id="c283a-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="c283a-151">Если этот параметр не указан, базовый двоичный объект и его снимки удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="c283a-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="c283a-152">Пользователю будет предложено подтвердить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="c283a-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="c283a-153">-Force</span><span class="sxs-lookup"><span data-stu-id="c283a-153">-Force</span></span>
<span data-ttu-id="c283a-154">Указывает на то, что этот командлет удаляет большой двоичный объект и его снимок без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c283a-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="c283a-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c283a-155">-PassThru</span></span>
<span data-ttu-id="c283a-156">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="c283a-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c283a-157">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c283a-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c283a-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c283a-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c283a-159">Указывает профиль Azure для прочтения командлета.</span><span class="sxs-lookup"><span data-stu-id="c283a-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="c283a-160">Если не указан, командлет считывает данные из профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c283a-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="c283a-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c283a-161">-SnapshotTime</span></span>
<span data-ttu-id="c283a-162">SnapshotTime больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="c283a-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="c283a-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="c283a-163">-VersionId</span></span>
<span data-ttu-id="c283a-164">VersionId BLOB</span><span class="sxs-lookup"><span data-stu-id="c283a-164">Blob VersionId</span></span>

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

### <span data-ttu-id="c283a-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c283a-165">-Confirm</span></span>
<span data-ttu-id="c283a-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c283a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c283a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c283a-167">-WhatIf</span></span>
<span data-ttu-id="c283a-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c283a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c283a-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c283a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c283a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c283a-170">CommonParameters</span></span>
<span data-ttu-id="c283a-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c283a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c283a-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c283a-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c283a-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c283a-173">INPUTS</span></span>

### <span data-ttu-id="c283a-174">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c283a-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c283a-175">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c283a-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c283a-176">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c283a-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c283a-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c283a-177">OUTPUTS</span></span>

### <span data-ttu-id="c283a-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c283a-178">System.Boolean</span></span>

## <span data-ttu-id="c283a-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="c283a-179">NOTES</span></span>

## <span data-ttu-id="c283a-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c283a-180">RELATED LINKS</span></span>

[<span data-ttu-id="c283a-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c283a-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c283a-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c283a-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="c283a-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c283a-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
