---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077525"
---
# <span data-ttu-id="3799b-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3799b-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="3799b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3799b-102">SYNOPSIS</span></span>
<span data-ttu-id="3799b-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="3799b-103">Lists the storage containers.</span></span>

## <span data-ttu-id="3799b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3799b-104">SYNTAX</span></span>

### <span data-ttu-id="3799b-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3799b-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3799b-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="3799b-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3799b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3799b-107">DESCRIPTION</span></span>
<span data-ttu-id="3799b-108">Командлет **Get-AzStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="3799b-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="3799b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3799b-109">EXAMPLES</span></span>

### <span data-ttu-id="3799b-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="3799b-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="3799b-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="3799b-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="3799b-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="3799b-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="3799b-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="3799b-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="3799b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3799b-114">PARAMETERS</span></span>

### <span data-ttu-id="3799b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3799b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3799b-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3799b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3799b-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="3799b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3799b-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3799b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3799b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3799b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3799b-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3799b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3799b-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3799b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3799b-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="3799b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3799b-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="3799b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3799b-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3799b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="3799b-125">-Context</span><span class="sxs-lookup"><span data-stu-id="3799b-125">-Context</span></span>
<span data-ttu-id="3799b-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="3799b-126">Specifies the storage context.</span></span>
<span data-ttu-id="3799b-127">Чтобы создать его, можно использовать командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3799b-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="3799b-128">Разрешения на доступ к контейнеру не будут извлекаться, если вы используете контекст хранилища, созданный из маркера SAS, так как для разрешений контейнера запросов требуется разрешение ключа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3799b-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="3799b-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3799b-129">-ContinuationToken</span></span>
<span data-ttu-id="3799b-130">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="3799b-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3799b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3799b-131">-DefaultProfile</span></span>
<span data-ttu-id="3799b-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3799b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3799b-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3799b-133">-MaxCount</span></span>
<span data-ttu-id="3799b-134">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3799b-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="3799b-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3799b-135">-Name</span></span>
<span data-ttu-id="3799b-136">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="3799b-136">Specifies the container name.</span></span>
<span data-ttu-id="3799b-137">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3799b-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="3799b-138">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="3799b-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3799b-139">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="3799b-139">-Prefix</span></span>
<span data-ttu-id="3799b-140">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="3799b-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="3799b-141">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="3799b-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3799b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3799b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3799b-143">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="3799b-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3799b-144">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3799b-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3799b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3799b-145">CommonParameters</span></span>
<span data-ttu-id="3799b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3799b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3799b-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3799b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3799b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3799b-148">INPUTS</span></span>

### <span data-ttu-id="3799b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3799b-149">System.String</span></span>

### <span data-ttu-id="3799b-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3799b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3799b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3799b-151">OUTPUTS</span></span>

### <span data-ttu-id="3799b-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3799b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3799b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="3799b-153">NOTES</span></span>

## <span data-ttu-id="3799b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3799b-154">RELATED LINKS</span></span>

[<span data-ttu-id="3799b-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3799b-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="3799b-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3799b-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="3799b-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3799b-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)

