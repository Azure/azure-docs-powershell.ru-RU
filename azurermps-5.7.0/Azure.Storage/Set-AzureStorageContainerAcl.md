---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: 5cfd42ebbdae85d59bf6715f41ffbe99911ec35c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566648"
---
# <span data-ttu-id="e6b41-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e6b41-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="e6b41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6b41-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b41-103">Задает разрешение Public Access для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e6b41-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6b41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6b41-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e6b41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b41-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b41-106">Командлет **Set-AzureStorageContainerAcl** задает разрешение Public Access указанному контейнеру хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b41-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="e6b41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6b41-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b41-108">Пример 1: Настройка ACL контейнера хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="e6b41-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="e6b41-109">Эта команда создает контейнер, у которого нет общедоступного доступа.</span><span class="sxs-lookup"><span data-stu-id="e6b41-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="e6b41-110">Пример 2: Настройка ACL контейнера хранилища Azure с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="e6b41-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="e6b41-111">Эта команда получает все контейнеры хранилища с именем, начинающимся с Container, и передает результат в конвейер, чтобы установить для него разрешение на доступ ко всем двоичным объектам.</span><span class="sxs-lookup"><span data-stu-id="e6b41-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="e6b41-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6b41-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b41-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6b41-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e6b41-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e6b41-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e6b41-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e6b41-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e6b41-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e6b41-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e6b41-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e6b41-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e6b41-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e6b41-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e6b41-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e6b41-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="e6b41-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e6b41-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="e6b41-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e6b41-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e6b41-122">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e6b41-123">-Context</span></span>
<span data-ttu-id="e6b41-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b41-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e6b41-125">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e6b41-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6b41-126">-Name</span></span>
<span data-ttu-id="e6b41-127">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6b41-127">Specifies a container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6b41-128">-PassThru</span></span>
<span data-ttu-id="e6b41-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e6b41-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6b41-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e6b41-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-131">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e6b41-131">-Permission</span></span>
<span data-ttu-id="e6b41-132">Указывает уровень общедоступного доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="e6b41-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="e6b41-133">По умолчанию контейнер и любые большие двоичные объекты в нем могут быть доступны только владельцу учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e6b41-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="e6b41-134">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его больших двоичных объектов, вы можете задать разрешения на доступ к контейнеру, чтобы включить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e6b41-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="e6b41-135">Анонимные пользователи могут читать большие двоичные объекты в общедоступном контейнере без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="e6b41-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="e6b41-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e6b41-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="e6b41-137">--Контейнер.</span><span class="sxs-lookup"><span data-stu-id="e6b41-137">--Container.</span></span>
<span data-ttu-id="e6b41-138">Предоставляет полный доступ на чтение для контейнера и его больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="e6b41-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="e6b41-139">Клиенты могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса, но не могут перечислять контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e6b41-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="e6b41-140">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="e6b41-140">--Blob.</span></span>
<span data-ttu-id="e6b41-141">Предоставляет доступ на чтение к данным BLOB-объектов в контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6b41-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="e6b41-142">Клиенты не могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса.</span><span class="sxs-lookup"><span data-stu-id="e6b41-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="e6b41-143">-Отключение.</span><span class="sxs-lookup"><span data-stu-id="e6b41-143">--Off.</span></span>
<span data-ttu-id="e6b41-144">Ограничивает доступ только владельцам учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e6b41-144">Restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6b41-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e6b41-146">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="e6b41-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e6b41-147">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e6b41-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="e6b41-148">Время на стороне сервера для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="e6b41-148">Server side time out for each request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b41-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b41-149">CommonParameters</span></span>
<span data-ttu-id="e6b41-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6b41-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b41-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b41-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b41-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6b41-152">INPUTS</span></span>

### <span data-ttu-id="e6b41-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6b41-153">IStorageContext</span></span>

<span data-ttu-id="e6b41-154">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6b41-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e6b41-155">Подстрок</span><span class="sxs-lookup"><span data-stu-id="e6b41-155">String</span></span>

<span data-ttu-id="e6b41-156">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6b41-156">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e6b41-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b41-157">OUTPUTS</span></span>

### <span data-ttu-id="e6b41-158">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6b41-158">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="e6b41-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6b41-159">NOTES</span></span>

## <span data-ttu-id="e6b41-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6b41-160">RELATED LINKS</span></span>

[<span data-ttu-id="e6b41-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6b41-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="e6b41-162">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6b41-162">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="e6b41-163">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6b41-163">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


