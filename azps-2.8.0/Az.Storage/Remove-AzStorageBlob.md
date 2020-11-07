---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: aaaa26078133846711bfba7b0e5765d1c6458eca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907210"
---
# <span data-ttu-id="2cbaa-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2cbaa-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="2cbaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbaa-103">Удаляет указанный большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="2cbaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cbaa-104">SYNTAX</span></span>

### <span data-ttu-id="2cbaa-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cbaa-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cbaa-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2cbaa-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cbaa-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2cbaa-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cbaa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cbaa-108">DESCRIPTION</span></span>
<span data-ttu-id="2cbaa-109">Командлет **Remove-AzStorageBlob** удаляет указанный большой двоичный объект из учетной записи хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="2cbaa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cbaa-110">EXAMPLES</span></span>

### <span data-ttu-id="2cbaa-111">Пример 1: удаление BLOB-объекта хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="2cbaa-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="2cbaa-112">Эта команда удаляет большой двоичный объект, идентифицированный по его имени.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="2cbaa-113">Пример 2: удаление большого двоичного объекта хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="2cbaa-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="2cbaa-114">В этой команде используется конвейер.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="2cbaa-115">Пример 3: удаление больших двоичных объектов хранилища с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="2cbaa-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="2cbaa-116">Эта команда использует подстановочный знак "звездочка" (\*) и конвейер для извлечения BLOB-объектов или больших двоичных объектов, а затем удаляет их.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="2cbaa-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cbaa-117">PARAMETERS</span></span>

### <span data-ttu-id="2cbaa-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2cbaa-118">-Blob</span></span>
<span data-ttu-id="2cbaa-119">Указывает имя большого двоичного объекта, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="2cbaa-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cbaa-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2cbaa-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2cbaa-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2cbaa-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2cbaa-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2cbaa-124">-CloudBlob</span></span>
<span data-ttu-id="2cbaa-125">Задает большой двоичный объект облака.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="2cbaa-126">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2cbaa-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2cbaa-127">-CloudBlobContainer</span></span>
<span data-ttu-id="2cbaa-128">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2cbaa-129">Вы можете использовать командлет Get-AzStorageContainer, чтобы получить его.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="2cbaa-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2cbaa-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2cbaa-131">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2cbaa-132">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2cbaa-133">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2cbaa-134">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2cbaa-135">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-135">The default value is 10.</span></span>

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

### <span data-ttu-id="2cbaa-136">-Container</span><span class="sxs-lookup"><span data-stu-id="2cbaa-136">-Container</span></span>
<span data-ttu-id="2cbaa-137">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="2cbaa-138">-Context</span><span class="sxs-lookup"><span data-stu-id="2cbaa-138">-Context</span></span>
<span data-ttu-id="2cbaa-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2cbaa-140">Вы можете создать его с помощью командлета New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="2cbaa-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbaa-141">-DefaultProfile</span></span>
<span data-ttu-id="2cbaa-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cbaa-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cbaa-143">-DeleteSnapshot</span></span>
<span data-ttu-id="2cbaa-144">Указывает, что все моментальные снимки удаляются, но не базовый блоб.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="2cbaa-145">Если этот параметр не указан, базовый двоичный объект и его снимки удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="2cbaa-146">Пользователю будет предложено подтвердить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="2cbaa-147">-Force</span><span class="sxs-lookup"><span data-stu-id="2cbaa-147">-Force</span></span>
<span data-ttu-id="2cbaa-148">Указывает на то, что этот командлет удаляет большой двоичный объект и его снимок без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="2cbaa-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cbaa-149">-PassThru</span></span>
<span data-ttu-id="2cbaa-150">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2cbaa-151">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2cbaa-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cbaa-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2cbaa-153">Указывает профиль Azure для прочтения командлета.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="2cbaa-154">Если не указан, командлет считывает данные из профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="2cbaa-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cbaa-155">-Confirm</span></span>
<span data-ttu-id="2cbaa-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbaa-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbaa-157">-WhatIf</span></span>
<span data-ttu-id="2cbaa-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cbaa-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbaa-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbaa-160">CommonParameters</span></span>
<span data-ttu-id="2cbaa-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cbaa-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbaa-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbaa-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbaa-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cbaa-163">INPUTS</span></span>

### <span data-ttu-id="2cbaa-164">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2cbaa-164">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2cbaa-165">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2cbaa-165">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2cbaa-166">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cbaa-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2cbaa-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cbaa-167">OUTPUTS</span></span>

### <span data-ttu-id="2cbaa-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cbaa-168">System.Boolean</span></span>

## <span data-ttu-id="2cbaa-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cbaa-169">NOTES</span></span>

## <span data-ttu-id="2cbaa-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cbaa-170">RELATED LINKS</span></span>

[<span data-ttu-id="2cbaa-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2cbaa-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2cbaa-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2cbaa-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="2cbaa-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2cbaa-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
