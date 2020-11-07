---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
ms.openlocfilehash: 95931b9aeb7c3b9f2869bc35115ab49a8aaf901f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913403"
---
# <span data-ttu-id="ac4c8-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ac4c8-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="ac4c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4c8-103">Задает разрешение Public Access для контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac4c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac4c8-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ac4c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ac4c8-106">Командлет **Set-AzureStorageContainerAcl** задает разрешение Public Access указанному контейнеру хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="ac4c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="ac4c8-108">Пример 1: Настройка ACL контейнера хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="ac4c8-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="ac4c8-109">Эта команда создает контейнер, у которого нет общедоступного доступа.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="ac4c8-110">Пример 2: Настройка ACL контейнера хранилища Azure с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ac4c8-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="ac4c8-111">Эта команда получает все контейнеры хранилища с именем, начинающимся с Container, и передает результат в конвейер, чтобы установить для него разрешение на доступ ко всем двоичным объектам.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="ac4c8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac4c8-112">PARAMETERS</span></span>

### <span data-ttu-id="ac4c8-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac4c8-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ac4c8-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ac4c8-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ac4c8-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ac4c8-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ac4c8-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ac4c8-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ac4c8-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ac4c8-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ac4c8-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ac4c8-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ac4c8-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ac4c8-123">-Context</span></span>
<span data-ttu-id="ac4c8-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ac4c8-125">Вы можете создать его с помощью командлета New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ac4c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4c8-126">-DefaultProfile</span></span>
<span data-ttu-id="ac4c8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac4c8-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac4c8-128">-Name</span></span>
<span data-ttu-id="ac4c8-129">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="ac4c8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac4c8-130">-PassThru</span></span>
<span data-ttu-id="ac4c8-131">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac4c8-132">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac4c8-133">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="ac4c8-133">-Permission</span></span>
<span data-ttu-id="ac4c8-134">Указывает уровень общедоступного доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ac4c8-135">По умолчанию контейнер и любые большие двоичные объекты в нем могут быть доступны только владельцу учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ac4c8-136">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его больших двоичных объектов, вы можете задать разрешения на доступ к контейнеру, чтобы включить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ac4c8-137">Анонимные пользователи могут читать большие двоичные объекты в общедоступном контейнере без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ac4c8-138">Допустимые значения этого параметра:--Container.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="ac4c8-139">Предоставляет полный доступ на чтение для контейнера и его больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ac4c8-140">Клиенты могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса, но не могут перечислять контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="ac4c8-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-141">--Blob.</span></span>
<span data-ttu-id="ac4c8-142">Предоставляет доступ на чтение к данным BLOB-объектов в контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ac4c8-143">Клиенты не могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="ac4c8-144">-Отключение.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-144">--Off.</span></span>
<span data-ttu-id="ac4c8-145">Ограничивает доступ только владельцам учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac4c8-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac4c8-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ac4c8-147">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ac4c8-148">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="ac4c8-149">Время на стороне сервера для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="ac4c8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4c8-150">CommonParameters</span></span>
<span data-ttu-id="ac4c8-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac4c8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4c8-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac4c8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4c8-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac4c8-153">INPUTS</span></span>

### <span data-ttu-id="ac4c8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ac4c8-154">System.String</span></span>

### <span data-ttu-id="ac4c8-155">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac4c8-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac4c8-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac4c8-156">OUTPUTS</span></span>

### <span data-ttu-id="ac4c8-157">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ac4c8-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ac4c8-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac4c8-158">NOTES</span></span>

## <span data-ttu-id="ac4c8-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac4c8-159">RELATED LINKS</span></span>

[<span data-ttu-id="ac4c8-160">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ac4c8-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ac4c8-161">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ac4c8-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="ac4c8-162">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ac4c8-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


