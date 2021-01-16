---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404023"
---
# <span data-ttu-id="ca5c2-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ca5c2-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="ca5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5c2-103">Удаляет указанный BLOB-проект хранилища.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="ca5c2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca5c2-104">SYNTAX</span></span>

### <span data-ttu-id="ca5c2-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca5c2-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca5c2-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ca5c2-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca5c2-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ca5c2-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca5c2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca5c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ca5c2-109">С **его учетной записью в** Azure указанный BLOB-проект удаляется.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="ca5c2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca5c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ca5c2-111">Пример 1. Удаление BLOB-хранилищ по имени</span><span class="sxs-lookup"><span data-stu-id="ca5c2-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="ca5c2-112">Эта команда удаляет большой ветвь, который определен по имени.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="ca5c2-113">Пример 2. Удаление BLOB-хранилищ с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ca5c2-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="ca5c2-114">Эта команда использует канал.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="ca5c2-115">Пример 3. Удаление BLOB-проектов хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ca5c2-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="ca5c2-116">В этой команде используется поддиавный знак звездочки (\*) и канал для извлечения ИТ-проектов и их удаления.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="ca5c2-117">Пример 4. Удаление одной версии BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="ca5c2-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="ca5c2-118">Эта команда удаляет одну вершину BLOB-команд с versionId.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="ca5c2-119">Пример 5. Удаление одного моментального снимка BLOB-ля</span><span class="sxs-lookup"><span data-stu-id="ca5c2-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="ca5c2-120">Эта команда удаляет один моментальный снимок BLOB-lob с помощью SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="ca5c2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca5c2-121">PARAMETERS</span></span>

### <span data-ttu-id="ca5c2-122">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ca5c2-122">-Blob</span></span>
<span data-ttu-id="ca5c2-123">Имя BLOB-части, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="ca5c2-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ca5c2-124">-BlobBaseClient</span></span>
<span data-ttu-id="ca5c2-125">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ca5c2-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="ca5c2-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca5c2-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca5c2-127">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca5c2-128">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca5c2-129">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca5c2-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ca5c2-130">-CloudBlob</span></span>
<span data-ttu-id="ca5c2-131">Определяет облачный большой документ.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="ca5c2-132">Чтобы получить объект **CloudBlob,** воспользуйтесь Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="ca5c2-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ca5c2-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ca5c2-133">-CloudBlobContainer</span></span>
<span data-ttu-id="ca5c2-134">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ca5c2-135">Чтобы получить Get-AzStorageContainer, воспользуйтесь этим Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="ca5c2-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca5c2-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca5c2-137">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca5c2-138">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca5c2-139">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca5c2-140">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca5c2-141">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-141">The default value is 10.</span></span>

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

### <span data-ttu-id="ca5c2-142">-Container</span><span class="sxs-lookup"><span data-stu-id="ca5c2-142">-Container</span></span>
<span data-ttu-id="ca5c2-143">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="ca5c2-144">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ca5c2-144">-Context</span></span>
<span data-ttu-id="ca5c2-145">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ca5c2-146">Для создания New-AzStorageContext можно использовать новый New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="ca5c2-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5c2-147">-DefaultProfile</span></span>
<span data-ttu-id="ca5c2-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5c2-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="ca5c2-149">-DeleteSnapshot</span></span>
<span data-ttu-id="ca5c2-150">Указывает, что будут удалены все моментальные снимки, но не базовый BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="ca5c2-151">Если этот параметр не задан, базовый BLOB-проект и его снимки удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="ca5c2-152">Пользователю будет предложено подтвердить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="ca5c2-153">-Force</span><span class="sxs-lookup"><span data-stu-id="ca5c2-153">-Force</span></span>
<span data-ttu-id="ca5c2-154">Указывает на то, что этот cmdlet удаляет BLOB-проект и его моментальный снимок без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="ca5c2-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca5c2-155">-PassThru</span></span>
<span data-ttu-id="ca5c2-156">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ca5c2-157">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ca5c2-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca5c2-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca5c2-159">Определяет профиль Azure для прочитаемого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="ca5c2-160">Если он не задан, он будет прочитано из профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="ca5c2-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="ca5c2-161">-SnapshotTime</span></span>
<span data-ttu-id="ca5c2-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="ca5c2-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="ca5c2-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="ca5c2-163">-VersionId</span></span>
<span data-ttu-id="ca5c2-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="ca5c2-164">Blob VersionId</span></span>

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

### <span data-ttu-id="ca5c2-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca5c2-165">-Confirm</span></span>
<span data-ttu-id="ca5c2-166">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5c2-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5c2-167">-WhatIf</span></span>
<span data-ttu-id="ca5c2-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5c2-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5c2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5c2-170">CommonParameters</span></span>
<span data-ttu-id="ca5c2-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5c2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5c2-172">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5c2-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5c2-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca5c2-173">INPUTS</span></span>

### <span data-ttu-id="ca5c2-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ca5c2-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ca5c2-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ca5c2-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ca5c2-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca5c2-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca5c2-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca5c2-177">OUTPUTS</span></span>

### <span data-ttu-id="ca5c2-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca5c2-178">System.Boolean</span></span>

## <span data-ttu-id="ca5c2-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca5c2-179">NOTES</span></span>

## <span data-ttu-id="ca5c2-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca5c2-180">RELATED LINKS</span></span>

[<span data-ttu-id="ca5c2-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ca5c2-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ca5c2-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca5c2-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="ca5c2-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ca5c2-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
