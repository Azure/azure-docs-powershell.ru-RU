---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002264"
---
# <span data-ttu-id="b7f81-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b7f81-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="b7f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f81-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f81-103">Задает разрешение на общедоступный доступ для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="b7f81-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="b7f81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7f81-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b7f81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f81-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f81-106">**Cmdlet Set-AzStorageContainerAcl** задает разрешение на общедоступный доступ для указанного контейнера хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f81-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="b7f81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7f81-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f81-108">Пример 1. Настройка ACL контейнера хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="b7f81-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="b7f81-109">Эта команда создает контейнер, не доступный всем.</span><span class="sxs-lookup"><span data-stu-id="b7f81-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="b7f81-110">Пример 2. Настройка ACL контейнера хранилища Azure с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="b7f81-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="b7f81-111">Эта команда получает все контейнеры хранилища, имя которых начинается с контейнера, а затем передает результат в конвейере, чтобы установить для них разрешение на доступ к BLOB-проекту.</span><span class="sxs-lookup"><span data-stu-id="b7f81-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="b7f81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f81-112">PARAMETERS</span></span>

### <span data-ttu-id="b7f81-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7f81-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b7f81-114">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b7f81-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b7f81-115">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="b7f81-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b7f81-116">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b7f81-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b7f81-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b7f81-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b7f81-118">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="b7f81-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b7f81-119">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="b7f81-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b7f81-120">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="b7f81-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b7f81-121">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="b7f81-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b7f81-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="b7f81-122">The default value is 10.</span></span>

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

### <span data-ttu-id="b7f81-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b7f81-123">-Context</span></span>
<span data-ttu-id="b7f81-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f81-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b7f81-125">Его можно создать с помощью New-AzStorageContext-управления.</span><span class="sxs-lookup"><span data-stu-id="b7f81-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b7f81-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f81-126">-DefaultProfile</span></span>
<span data-ttu-id="b7f81-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f81-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f81-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b7f81-128">-Name</span></span>
<span data-ttu-id="b7f81-129">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="b7f81-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="b7f81-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7f81-130">-PassThru</span></span>
<span data-ttu-id="b7f81-131">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b7f81-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7f81-132">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b7f81-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7f81-133">-Permission</span><span class="sxs-lookup"><span data-stu-id="b7f81-133">-Permission</span></span>
<span data-ttu-id="b7f81-134">Определяет уровень общего доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="b7f81-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="b7f81-135">По умолчанию доступ к контейнеру и всем его BLOB-сайтам может получить только владелец учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b7f81-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="b7f81-136">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его BLOB-контейнера, можно настроить разрешения на доступ к контейнеру для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b7f81-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="b7f81-137">Анонимные пользователи могут читать большой объем в общедоступных контейнерах без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="b7f81-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="b7f81-138">Допустимые значения для этого параметра: --Container.</span><span class="sxs-lookup"><span data-stu-id="b7f81-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="b7f81-139">Обеспечивает полный доступ для чтения к контейнеру и его BLOB-лям.</span><span class="sxs-lookup"><span data-stu-id="b7f81-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="b7f81-140">Клиенты могут с помощью анонимного запроса укаймировать в контейнере BLOB-контейнер, но не могут продумыть контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b7f81-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="b7f81-141">--BLOB.)</span><span class="sxs-lookup"><span data-stu-id="b7f81-141">--Blob.</span></span>
<span data-ttu-id="b7f81-142">Обеспечивает доступ считываемой информации в контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="b7f81-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="b7f81-143">Клиенты не могут с помощью анонимного запроса укаймировать BLOB-клиенты в контейнере.</span><span class="sxs-lookup"><span data-stu-id="b7f81-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="b7f81-144">--Выключите.</span><span class="sxs-lookup"><span data-stu-id="b7f81-144">--Off.</span></span>
<span data-ttu-id="b7f81-145">Ограничивает доступ только к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b7f81-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f81-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7f81-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b7f81-147">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="b7f81-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b7f81-148">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b7f81-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="b7f81-149">Время времени, не в течение времени, в течение времени, за который сервер должен быть отсвея на каждом запросе</span><span class="sxs-lookup"><span data-stu-id="b7f81-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="b7f81-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f81-150">CommonParameters</span></span>
<span data-ttu-id="b7f81-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f81-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f81-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f81-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f81-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f81-153">INPUTS</span></span>

### <span data-ttu-id="b7f81-154">System.String</span><span class="sxs-lookup"><span data-stu-id="b7f81-154">System.String</span></span>

### <span data-ttu-id="b7f81-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7f81-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b7f81-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f81-156">OUTPUTS</span></span>

### <span data-ttu-id="b7f81-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7f81-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="b7f81-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7f81-158">NOTES</span></span>

## <span data-ttu-id="b7f81-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7f81-159">RELATED LINKS</span></span>

[<span data-ttu-id="b7f81-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7f81-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="b7f81-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7f81-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="b7f81-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7f81-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


