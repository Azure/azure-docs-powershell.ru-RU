---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988756"
---
# <span data-ttu-id="eb214-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="eb214-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="eb214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb214-102">SYNOPSIS</span></span>
<span data-ttu-id="eb214-103">Копирование BLOB-lob синхронно.</span><span class="sxs-lookup"><span data-stu-id="eb214-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="eb214-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb214-104">SYNTAX</span></span>

### <span data-ttu-id="eb214-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb214-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb214-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="eb214-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb214-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="eb214-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb214-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb214-108">DESCRIPTION</span></span>
<span data-ttu-id="eb214-109">**Cmdlet Copy-AzStorageBlob** копирует BLOB-проект синхронно, в настоящее время поддерживается только большой BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="eb214-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="eb214-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb214-110">EXAMPLES</span></span>

### <span data-ttu-id="eb214-111">Пример 1. Копирование именоваемого BLOB-имени в другой</span><span class="sxs-lookup"><span data-stu-id="eb214-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="eb214-112">Эта команда копирует BLOB-проект из контейнера-источника в контейнер назначения с новым именем.</span><span class="sxs-lookup"><span data-stu-id="eb214-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="eb214-113">Пример 2. Копирование BLOB-объектов из BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="eb214-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="eb214-114">Эта команда копирует BLOB-объект из объекта-источника в контейнер назначения с новым именем BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="eb214-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="eb214-115">Пример 3. Копирование BLOB-uri из BLOB-URI</span><span class="sxs-lookup"><span data-stu-id="eb214-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="eb214-116">Первая команда создает URI BLOB-uri источника с маркером разрешений sas "rt".</span><span class="sxs-lookup"><span data-stu-id="eb214-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="eb214-117">Вторая команда копирует его из URI источника в uri назначения.</span><span class="sxs-lookup"><span data-stu-id="eb214-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="eb214-118">Пример 4. Обновление области шифрования BLOB-блоков</span><span class="sxs-lookup"><span data-stu-id="eb214-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="eb214-119">Эта команда обновляет область шифрования блоков BLOB-файлов, копируя их в себя с новой областью шифрования.</span><span class="sxs-lookup"><span data-stu-id="eb214-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="eb214-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb214-120">PARAMETERS</span></span>

### <span data-ttu-id="eb214-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="eb214-121">-AbsoluteUri</span></span>
<span data-ttu-id="eb214-122">URI источника BLOB-uri</span><span class="sxs-lookup"><span data-stu-id="eb214-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb214-123">-AsJob</span></span>
<span data-ttu-id="eb214-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb214-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb214-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eb214-125">-BlobBaseClient</span></span>
<span data-ttu-id="eb214-126">Объект BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eb214-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-127">-Контекст</span><span class="sxs-lookup"><span data-stu-id="eb214-127">-Context</span></span>
<span data-ttu-id="eb214-128">Объект контекстного контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="eb214-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb214-129">-DefaultProfile</span></span>
<span data-ttu-id="eb214-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb214-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb214-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="eb214-131">-DestBlob</span></span>
<span data-ttu-id="eb214-132">Имя BLOB-имени назначения</span><span class="sxs-lookup"><span data-stu-id="eb214-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="eb214-133">-DestContainer</span></span>
<span data-ttu-id="eb214-134">Имя контейнера назначения</span><span class="sxs-lookup"><span data-stu-id="eb214-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="eb214-135">-DestContext</span></span>
<span data-ttu-id="eb214-136">Объект контекстного хранилища назначения</span><span class="sxs-lookup"><span data-stu-id="eb214-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="eb214-137">-EncryptionScope</span></span>
<span data-ttu-id="eb214-138">Область шифрования, используемая при создании запросов к BLOB-проекту dest.</span><span class="sxs-lookup"><span data-stu-id="eb214-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="eb214-139">-Force</span><span class="sxs-lookup"><span data-stu-id="eb214-139">-Force</span></span>
<span data-ttu-id="eb214-140">Принудительное переописывание существующего BLOB-файла</span><span class="sxs-lookup"><span data-stu-id="eb214-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="eb214-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="eb214-141">-RehydratePriority</span></span>
<span data-ttu-id="eb214-142">Блокировать BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="eb214-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="eb214-143">Приоритет, с помощью которого нужно перегибать архивный BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="eb214-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="eb214-144">Допустимые значения: "Высокое" или "Стандартное".</span><span class="sxs-lookup"><span data-stu-id="eb214-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="eb214-145">-SrcBlob</span></span>
<span data-ttu-id="eb214-146">Имя BLOB-ля</span><span class="sxs-lookup"><span data-stu-id="eb214-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="eb214-147">-SrcContainer</span></span>
<span data-ttu-id="eb214-148">Имя контейнера источника</span><span class="sxs-lookup"><span data-stu-id="eb214-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="eb214-149">-StandardBlobTier</span></span>
<span data-ttu-id="eb214-150">Заблокировать уровень BLOB-блоков, допустимые значения — "Hot/Cool/Archive".</span><span class="sxs-lookup"><span data-stu-id="eb214-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="eb214-151">Подробности https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="eb214-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb214-152">-Confirm</span></span>
<span data-ttu-id="eb214-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb214-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb214-154">-WhatIf</span></span>
<span data-ttu-id="eb214-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb214-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb214-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb214-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb214-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb214-157">CommonParameters</span></span>
<span data-ttu-id="eb214-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb214-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb214-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb214-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb214-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb214-160">INPUTS</span></span>

### <span data-ttu-id="eb214-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="eb214-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="eb214-162">System.String</span><span class="sxs-lookup"><span data-stu-id="eb214-162">System.String</span></span>

### <span data-ttu-id="eb214-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb214-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eb214-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb214-164">OUTPUTS</span></span>

### <span data-ttu-id="eb214-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="eb214-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="eb214-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb214-166">NOTES</span></span>

## <span data-ttu-id="eb214-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb214-167">RELATED LINKS</span></span>
