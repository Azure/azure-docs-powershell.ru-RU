---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232508"
---
# <span data-ttu-id="a4626-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4626-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="a4626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4626-102">SYNOPSIS</span></span>
<span data-ttu-id="a4626-103">Создает контейнер хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a4626-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="a4626-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4626-104">SYNTAX</span></span>

### <span data-ttu-id="a4626-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4626-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a4626-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a4626-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a4626-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4626-107">DESCRIPTION</span></span>
<span data-ttu-id="a4626-108">Для создания контейнера хранилища Azure создается проектлет **New-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="a4626-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="a4626-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4626-109">EXAMPLES</span></span>

### <span data-ttu-id="a4626-110">Пример 1. Создание контейнера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="a4626-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="a4626-111">Эта команда создает контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4626-111">This command creates a storage container.</span></span>

### <span data-ttu-id="a4626-112">Пример 2. Создание нескольких контейнеров хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="a4626-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="a4626-113">В этом примере создается несколько контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4626-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="a4626-114">Для этого используется **метод разделения** класса .NET **String,** который передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="a4626-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="a4626-115">Пример 3. Создание контейнера хранилища Azure с областью шифрования</span><span class="sxs-lookup"><span data-stu-id="a4626-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="a4626-116">Эта команда создает контейнер хранилища с областью шифрования по умолчанию в качестве myencryptscope и предотвращает отправку BLOB-файлов с другой областью шифрования для этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4626-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="a4626-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4626-117">PARAMETERS</span></span>

### <span data-ttu-id="a4626-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4626-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a4626-119">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a4626-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a4626-120">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="a4626-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a4626-121">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a4626-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a4626-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a4626-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a4626-123">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="a4626-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a4626-124">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="a4626-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a4626-125">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="a4626-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a4626-126">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="a4626-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a4626-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a4626-127">The default value is 10.</span></span>

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

### <span data-ttu-id="a4626-128">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a4626-128">-Context</span></span>
<span data-ttu-id="a4626-129">Определяет контекст для нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4626-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="a4626-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a4626-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="a4626-131">Заданный объем шифрования для всех записей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4626-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4626-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4626-132">-DefaultProfile</span></span>
<span data-ttu-id="a4626-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4626-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4626-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a4626-134">-Name</span></span>
<span data-ttu-id="a4626-135">Указывает имя нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4626-135">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4626-136">-Permission</span><span class="sxs-lookup"><span data-stu-id="a4626-136">-Permission</span></span>
<span data-ttu-id="a4626-137">Определяет уровень общего доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="a4626-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="a4626-138">По умолчанию доступ к контейнеру и всем его BLOB-сайтам может получить только владелец учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a4626-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="a4626-139">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его BLOB-контейнера, можно настроить разрешения на доступ к контейнеру для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="a4626-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="a4626-140">Анонимные пользователи могут читать большой объем в общедоступных контейнерах без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="a4626-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="a4626-141">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="a4626-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4626-142">"Контейнер".</span><span class="sxs-lookup"><span data-stu-id="a4626-142">Container.</span></span>
<span data-ttu-id="a4626-143">Обеспечивает полный доступ для чтения к контейнеру и его BLOB-лям.</span><span class="sxs-lookup"><span data-stu-id="a4626-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="a4626-144">Клиенты могут с помощью анонимного запроса укаймировать в контейнере BLOB-контейнер, но не могут прогонять контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a4626-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="a4626-145">BLOB.;</span><span class="sxs-lookup"><span data-stu-id="a4626-145">Blob.</span></span>
<span data-ttu-id="a4626-146">Обеспечивает доступ к данным lob-lob во всем контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4626-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="a4626-147">Клиенты не могут с помощью анонимного запроса укаймировать BLOB-клиенты в контейнере.</span><span class="sxs-lookup"><span data-stu-id="a4626-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="a4626-148">"Выключи".</span><span class="sxs-lookup"><span data-stu-id="a4626-148">Off.</span></span>
<span data-ttu-id="a4626-149">Это ограничение доступа только для владельца учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a4626-149">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4626-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="a4626-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="a4626-151">Заблокировать переопределения области шифрования, заданную по умолчанию для контейнера.</span><span class="sxs-lookup"><span data-stu-id="a4626-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4626-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4626-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a4626-153">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a4626-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a4626-154">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a4626-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a4626-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4626-155">CommonParameters</span></span>
<span data-ttu-id="a4626-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4626-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4626-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4626-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4626-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4626-158">INPUTS</span></span>

### <span data-ttu-id="a4626-159">System.String</span><span class="sxs-lookup"><span data-stu-id="a4626-159">System.String</span></span>

### <span data-ttu-id="a4626-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4626-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a4626-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4626-161">OUTPUTS</span></span>

### <span data-ttu-id="a4626-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4626-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="a4626-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4626-163">NOTES</span></span>

## <span data-ttu-id="a4626-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4626-164">RELATED LINKS</span></span>

[<span data-ttu-id="a4626-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4626-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="a4626-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a4626-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="a4626-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a4626-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


