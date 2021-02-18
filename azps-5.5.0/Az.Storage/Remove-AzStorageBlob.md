---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231601"
---
# <span data-ttu-id="ab38d-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ab38d-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="ab38d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab38d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab38d-103">Удаляет указанный BLOB-проект хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab38d-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="ab38d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab38d-104">SYNTAX</span></span>

### <span data-ttu-id="ab38d-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab38d-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab38d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ab38d-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab38d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ab38d-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab38d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab38d-108">DESCRIPTION</span></span>
<span data-ttu-id="ab38d-109">С **его учетной записью в** Azure указанный BLOB-проект удаляется.</span><span class="sxs-lookup"><span data-stu-id="ab38d-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="ab38d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab38d-110">EXAMPLES</span></span>

### <span data-ttu-id="ab38d-111">Пример 1. Удаление BLOB-хранилищ по имени</span><span class="sxs-lookup"><span data-stu-id="ab38d-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="ab38d-112">Эта команда удаляет большой именем.</span><span class="sxs-lookup"><span data-stu-id="ab38d-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="ab38d-113">Пример 2. Удаление BLOB-хранилищ с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ab38d-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="ab38d-114">Эта команда использует канал.</span><span class="sxs-lookup"><span data-stu-id="ab38d-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="ab38d-115">Пример 3. Удаление BLOB-проектов хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ab38d-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="ab38d-116">В этой команде используется поддиавный знак звездочки (\*) и канал для извлечения ИТ-проектов и их удаления.</span><span class="sxs-lookup"><span data-stu-id="ab38d-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="ab38d-117">Пример 4. Удаление одной версии BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="ab38d-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="ab38d-118">Эта команда удаляет одну вершину BLOB-команд с versionId.</span><span class="sxs-lookup"><span data-stu-id="ab38d-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="ab38d-119">Пример 5. Удаление одного моментального снимка BLOB-ля</span><span class="sxs-lookup"><span data-stu-id="ab38d-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="ab38d-120">Эта команда удаляет один моментальный снимок BLOB-lob с помощью SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="ab38d-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="ab38d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab38d-121">PARAMETERS</span></span>

### <span data-ttu-id="ab38d-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ab38d-122">-Blob</span></span>
<span data-ttu-id="ab38d-123">Имя BLOB-части, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="ab38d-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="ab38d-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ab38d-124">-BlobBaseClient</span></span>
<span data-ttu-id="ab38d-125">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ab38d-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="ab38d-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab38d-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ab38d-127">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ab38d-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ab38d-128">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="ab38d-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ab38d-129">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ab38d-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ab38d-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ab38d-130">-CloudBlob</span></span>
<span data-ttu-id="ab38d-131">Указывает облачный BLOB-л.</span><span class="sxs-lookup"><span data-stu-id="ab38d-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="ab38d-132">Чтобы получить объект **CloudBlob,** используйте Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="ab38d-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ab38d-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ab38d-133">-CloudBlobContainer</span></span>
<span data-ttu-id="ab38d-134">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ab38d-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ab38d-135">Чтобы получить Get-AzStorageContainer, воспользуйтесь этим Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ab38d-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="ab38d-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ab38d-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ab38d-137">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ab38d-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ab38d-138">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ab38d-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ab38d-139">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="ab38d-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ab38d-140">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="ab38d-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ab38d-141">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ab38d-141">The default value is 10.</span></span>

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

### <span data-ttu-id="ab38d-142">-Container</span><span class="sxs-lookup"><span data-stu-id="ab38d-142">-Container</span></span>
<span data-ttu-id="ab38d-143">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ab38d-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="ab38d-144">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ab38d-144">-Context</span></span>
<span data-ttu-id="ab38d-145">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ab38d-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ab38d-146">Для создания New-AzStorageContext можно использовать новый New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab38d-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="ab38d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab38d-147">-DefaultProfile</span></span>
<span data-ttu-id="ab38d-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab38d-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab38d-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="ab38d-149">-DeleteSnapshot</span></span>
<span data-ttu-id="ab38d-150">Указывает, что будут удалены все моментальные снимки, но не базовый BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="ab38d-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="ab38d-151">Если этот параметр не задан, базовый BLOB-проект и его снимки удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="ab38d-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="ab38d-152">Пользователю будет предложено подтвердить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="ab38d-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="ab38d-153">-Force</span><span class="sxs-lookup"><span data-stu-id="ab38d-153">-Force</span></span>
<span data-ttu-id="ab38d-154">Указывает на то, что этот cmdlet удаляет BLOB-проект и его моментальный снимок без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ab38d-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="ab38d-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab38d-155">-PassThru</span></span>
<span data-ttu-id="ab38d-156">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="ab38d-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ab38d-157">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ab38d-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ab38d-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab38d-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ab38d-159">Указывает профиль Azure, который нужно прочитать для cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab38d-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="ab38d-160">Если он не задан, он будет прочитано из профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab38d-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="ab38d-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="ab38d-161">-SnapshotTime</span></span>
<span data-ttu-id="ab38d-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="ab38d-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="ab38d-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="ab38d-163">-VersionId</span></span>
<span data-ttu-id="ab38d-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="ab38d-164">Blob VersionId</span></span>

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

### <span data-ttu-id="ab38d-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab38d-165">-Confirm</span></span>
<span data-ttu-id="ab38d-166">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ab38d-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab38d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab38d-167">-WhatIf</span></span>
<span data-ttu-id="ab38d-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab38d-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab38d-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab38d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab38d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab38d-170">CommonParameters</span></span>
<span data-ttu-id="ab38d-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab38d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab38d-172">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab38d-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab38d-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab38d-173">INPUTS</span></span>

### <span data-ttu-id="ab38d-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ab38d-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ab38d-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ab38d-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ab38d-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab38d-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab38d-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab38d-177">OUTPUTS</span></span>

### <span data-ttu-id="ab38d-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab38d-178">System.Boolean</span></span>

## <span data-ttu-id="ab38d-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab38d-179">NOTES</span></span>

## <span data-ttu-id="ab38d-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab38d-180">RELATED LINKS</span></span>

[<span data-ttu-id="ab38d-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ab38d-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ab38d-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab38d-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="ab38d-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab38d-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
