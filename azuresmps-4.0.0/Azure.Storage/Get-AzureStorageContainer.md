---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556271"
---
# <span data-ttu-id="5f1a2-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5f1a2-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="5f1a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1a2-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-103">Lists the storage containers.</span></span>

## <span data-ttu-id="5f1a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f1a2-104">SYNTAX</span></span>

### <span data-ttu-id="5f1a2-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f1a2-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5f1a2-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="5f1a2-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5f1a2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-107">DESCRIPTION</span></span>
<span data-ttu-id="5f1a2-108">Командлет **Get-AzureStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="5f1a2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-109">EXAMPLES</span></span>

### <span data-ttu-id="5f1a2-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="5f1a2-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="5f1a2-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="5f1a2-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="5f1a2-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="5f1a2-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="5f1a2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-114">PARAMETERS</span></span>

### <span data-ttu-id="5f1a2-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f1a2-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f1a2-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f1a2-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f1a2-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f1a2-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f1a2-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f1a2-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f1a2-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f1a2-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f1a2-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f1a2-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-124">The default value is 10.</span></span>

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

### <span data-ttu-id="5f1a2-125">-Context</span><span class="sxs-lookup"><span data-stu-id="5f1a2-125">-Context</span></span>
<span data-ttu-id="5f1a2-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-126">Specifies the storage context.</span></span>
<span data-ttu-id="5f1a2-127">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f1a2-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="5f1a2-128">-ContinuationToken</span></span>
<span data-ttu-id="5f1a2-129">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="5f1a2-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5f1a2-130">-MaxCount</span></span>
<span data-ttu-id="5f1a2-131">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="5f1a2-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f1a2-132">-Name</span></span>
<span data-ttu-id="5f1a2-133">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-133">Specifies the container name.</span></span>
<span data-ttu-id="5f1a2-134">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="5f1a2-135">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1a2-136">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="5f1a2-136">-Prefix</span></span>
<span data-ttu-id="5f1a2-137">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="5f1a2-138">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="5f1a2-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="5f1a2-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f1a2-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f1a2-140">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="5f1a2-141">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="5f1a2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1a2-142">CommonParameters</span></span>
<span data-ttu-id="5f1a2-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f1a2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1a2-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f1a2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1a2-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f1a2-145">INPUTS</span></span>

## <span data-ttu-id="5f1a2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-146">OUTPUTS</span></span>

## <span data-ttu-id="5f1a2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f1a2-147">NOTES</span></span>

## <span data-ttu-id="5f1a2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f1a2-148">RELATED LINKS</span></span>

[<span data-ttu-id="5f1a2-149">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5f1a2-149">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="5f1a2-150">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5f1a2-150">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="5f1a2-151">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="5f1a2-151">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


