---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324789"
---
# <span data-ttu-id="1f479-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f479-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="1f479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f479-102">SYNOPSIS</span></span>
<span data-ttu-id="1f479-103">Создает контейнер хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1f479-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="1f479-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f479-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1f479-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f479-105">DESCRIPTION</span></span>
<span data-ttu-id="1f479-106">Для создания контейнера хранилища Azure будет создаваться проектлет **New-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="1f479-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="1f479-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f479-107">EXAMPLES</span></span>

### <span data-ttu-id="1f479-108">Пример 1. Создание контейнера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1f479-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="1f479-109">Эта команда создает контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="1f479-109">This command creates a storage container.</span></span>

### <span data-ttu-id="1f479-110">Пример 2. Создание нескольких контейнеров хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1f479-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="1f479-111">В этом примере создается несколько контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="1f479-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="1f479-112">Для этого используется **метод разделения** класса .NET **String,** который передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="1f479-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="1f479-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f479-113">PARAMETERS</span></span>

### <span data-ttu-id="1f479-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f479-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1f479-115">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="1f479-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1f479-116">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="1f479-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1f479-117">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1f479-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1f479-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1f479-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1f479-119">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="1f479-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1f479-120">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="1f479-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1f479-121">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="1f479-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1f479-122">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="1f479-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1f479-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="1f479-123">The default value is 10.</span></span>

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

### <span data-ttu-id="1f479-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="1f479-124">-Context</span></span>
<span data-ttu-id="1f479-125">Определяет контекст для нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="1f479-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="1f479-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f479-126">-DefaultProfile</span></span>
<span data-ttu-id="1f479-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f479-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f479-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1f479-128">-Name</span></span>
<span data-ttu-id="1f479-129">Указывает имя нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="1f479-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="1f479-130">-Permission</span><span class="sxs-lookup"><span data-stu-id="1f479-130">-Permission</span></span>
<span data-ttu-id="1f479-131">Определяет уровень общего доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="1f479-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="1f479-132">По умолчанию доступ к контейнеру и всем его BLOB-сайтам может получить только владелец учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1f479-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="1f479-133">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его BLOB-проекту, можно настроить разрешения для контейнера, чтобы разрешить общедоступный доступ.</span><span class="sxs-lookup"><span data-stu-id="1f479-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="1f479-134">Анонимные пользователи могут читать большой объем в общедоступных контейнерах без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="1f479-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="1f479-135">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1f479-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f479-136">"Контейнер".</span><span class="sxs-lookup"><span data-stu-id="1f479-136">Container.</span></span>
<span data-ttu-id="1f479-137">Обеспечивает полный доступ для чтения к контейнеру и его BLOB-лям.</span><span class="sxs-lookup"><span data-stu-id="1f479-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="1f479-138">Клиенты могут с помощью анонимного запроса укаймировать в контейнере BLOB-контейнер, но не могут прогонять контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1f479-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="1f479-139">BLOB.;</span><span class="sxs-lookup"><span data-stu-id="1f479-139">Blob.</span></span>
<span data-ttu-id="1f479-140">Обеспечивает доступ к данным lob-lob во всем контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="1f479-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="1f479-141">Клиенты не могут с помощью анонимного запроса промерять BLOB-lob-ы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="1f479-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="1f479-142">"Выключи".</span><span class="sxs-lookup"><span data-stu-id="1f479-142">Off.</span></span>
<span data-ttu-id="1f479-143">Это ограничение доступа только для владельца учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1f479-143">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="1f479-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f479-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1f479-145">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1f479-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1f479-146">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1f479-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1f479-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f479-147">CommonParameters</span></span>
<span data-ttu-id="1f479-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f479-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f479-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f479-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f479-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f479-150">INPUTS</span></span>

### <span data-ttu-id="1f479-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1f479-151">System.String</span></span>

### <span data-ttu-id="1f479-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f479-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f479-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f479-153">OUTPUTS</span></span>

### <span data-ttu-id="1f479-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f479-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="1f479-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f479-155">NOTES</span></span>

## <span data-ttu-id="1f479-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f479-156">RELATED LINKS</span></span>

[<span data-ttu-id="1f479-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f479-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="1f479-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f479-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="1f479-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1f479-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


