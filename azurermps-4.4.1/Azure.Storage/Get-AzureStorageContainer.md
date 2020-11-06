---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567208"
---
# <span data-ttu-id="95652-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95652-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="95652-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95652-102">SYNOPSIS</span></span>
<span data-ttu-id="95652-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="95652-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95652-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95652-104">SYNTAX</span></span>

### <span data-ttu-id="95652-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95652-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="95652-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="95652-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="95652-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95652-107">DESCRIPTION</span></span>
<span data-ttu-id="95652-108">Командлет **Get-AzureStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="95652-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="95652-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95652-109">EXAMPLES</span></span>

### <span data-ttu-id="95652-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="95652-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="95652-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="95652-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="95652-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="95652-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="95652-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="95652-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="95652-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95652-114">PARAMETERS</span></span>

### <span data-ttu-id="95652-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95652-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="95652-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="95652-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="95652-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="95652-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="95652-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="95652-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="95652-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="95652-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="95652-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="95652-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="95652-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="95652-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="95652-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="95652-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="95652-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="95652-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="95652-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="95652-124">The default value is 10.</span></span>

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

### <span data-ttu-id="95652-125">-Context</span><span class="sxs-lookup"><span data-stu-id="95652-125">-Context</span></span>
<span data-ttu-id="95652-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="95652-126">Specifies the storage context.</span></span>
<span data-ttu-id="95652-127">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="95652-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="95652-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="95652-128">-ContinuationToken</span></span>
<span data-ttu-id="95652-129">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="95652-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="95652-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="95652-130">-MaxCount</span></span>
<span data-ttu-id="95652-131">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="95652-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="95652-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95652-132">-Name</span></span>
<span data-ttu-id="95652-133">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="95652-133">Specifies the container name.</span></span>
<span data-ttu-id="95652-134">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="95652-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="95652-135">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="95652-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="95652-136">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="95652-136">-Prefix</span></span>
<span data-ttu-id="95652-137">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="95652-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="95652-138">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="95652-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="95652-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95652-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="95652-140">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="95652-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="95652-141">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="95652-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="95652-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95652-142">CommonParameters</span></span>
<span data-ttu-id="95652-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95652-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95652-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95652-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95652-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95652-145">INPUTS</span></span>

### <span data-ttu-id="95652-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="95652-146">IStorageContext</span></span>

<span data-ttu-id="95652-147">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="95652-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="95652-148">Подстрок</span><span class="sxs-lookup"><span data-stu-id="95652-148">String</span></span>

<span data-ttu-id="95652-149">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="95652-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="95652-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95652-150">OUTPUTS</span></span>

### <span data-ttu-id="95652-151">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95652-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="95652-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="95652-152">NOTES</span></span>

## <span data-ttu-id="95652-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95652-153">RELATED LINKS</span></span>

[<span data-ttu-id="95652-154">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95652-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="95652-155">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95652-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="95652-156">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="95652-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


