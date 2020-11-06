---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565097"
---
# <span data-ttu-id="58dee-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58dee-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="58dee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58dee-102">SYNOPSIS</span></span>
<span data-ttu-id="58dee-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="58dee-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58dee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58dee-104">SYNTAX</span></span>

### <span data-ttu-id="58dee-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58dee-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="58dee-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="58dee-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="58dee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58dee-107">DESCRIPTION</span></span>
<span data-ttu-id="58dee-108">Командлет **Get-AzureStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="58dee-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="58dee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58dee-109">EXAMPLES</span></span>

### <span data-ttu-id="58dee-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="58dee-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="58dee-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="58dee-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="58dee-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="58dee-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="58dee-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="58dee-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="58dee-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58dee-114">PARAMETERS</span></span>

### <span data-ttu-id="58dee-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58dee-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58dee-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58dee-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="58dee-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="58dee-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="58dee-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="58dee-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="58dee-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58dee-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58dee-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="58dee-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="58dee-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="58dee-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="58dee-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="58dee-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="58dee-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="58dee-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="58dee-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="58dee-124">The default value is 10.</span></span>

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

### <span data-ttu-id="58dee-125">-Context</span><span class="sxs-lookup"><span data-stu-id="58dee-125">-Context</span></span>
<span data-ttu-id="58dee-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="58dee-126">Specifies the storage context.</span></span>
<span data-ttu-id="58dee-127">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="58dee-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="58dee-128">Командлет завершится сбоем, если вы используете контекст хранения, созданный из маркера SAS, так как он будет запрашивать разрешения контейнера, требующие разрешения ключа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58dee-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="58dee-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="58dee-129">-ContinuationToken</span></span>
<span data-ttu-id="58dee-130">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="58dee-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dee-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="58dee-131">-MaxCount</span></span>
<span data-ttu-id="58dee-132">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="58dee-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="58dee-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58dee-133">-Name</span></span>
<span data-ttu-id="58dee-134">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="58dee-134">Specifies the container name.</span></span>
<span data-ttu-id="58dee-135">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="58dee-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="58dee-136">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="58dee-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="58dee-137">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="58dee-137">-Prefix</span></span>
<span data-ttu-id="58dee-138">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="58dee-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="58dee-139">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="58dee-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dee-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58dee-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58dee-141">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="58dee-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="58dee-142">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="58dee-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="58dee-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58dee-143">CommonParameters</span></span>
<span data-ttu-id="58dee-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58dee-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58dee-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58dee-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58dee-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58dee-146">INPUTS</span></span>

### <span data-ttu-id="58dee-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="58dee-147">IStorageContext</span></span>

<span data-ttu-id="58dee-148">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="58dee-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="58dee-149">Подстрок</span><span class="sxs-lookup"><span data-stu-id="58dee-149">String</span></span>

<span data-ttu-id="58dee-150">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="58dee-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="58dee-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58dee-151">OUTPUTS</span></span>

### <span data-ttu-id="58dee-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58dee-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="58dee-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="58dee-153">NOTES</span></span>

## <span data-ttu-id="58dee-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58dee-154">RELATED LINKS</span></span>

[<span data-ttu-id="58dee-155">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58dee-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="58dee-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="58dee-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="58dee-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="58dee-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


