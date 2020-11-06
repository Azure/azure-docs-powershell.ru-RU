---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556219"
---
# <span data-ttu-id="0fe26-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0fe26-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="0fe26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fe26-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe26-103">Создание контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe26-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="0fe26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fe26-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0fe26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe26-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe26-106">Командлет **New-AzureStorageContainer** создает контейнер хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe26-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="0fe26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fe26-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe26-108">Пример 1: создание контейнера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="0fe26-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="0fe26-109">Эта команда создает контейнер хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fe26-109">This command creates a storage container.</span></span>

### <span data-ttu-id="0fe26-110">Пример 2: создание нескольких контейнеров хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="0fe26-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="0fe26-111">В этом примере создается несколько контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fe26-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="0fe26-112">Он использует метод **Split** класса **String** .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="0fe26-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="0fe26-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fe26-113">PARAMETERS</span></span>

### <span data-ttu-id="0fe26-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0fe26-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0fe26-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0fe26-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0fe26-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="0fe26-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0fe26-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0fe26-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0fe26-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0fe26-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0fe26-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0fe26-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0fe26-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0fe26-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0fe26-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="0fe26-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0fe26-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0fe26-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0fe26-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0fe26-123">The default value is 10.</span></span>

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

### <span data-ttu-id="0fe26-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0fe26-124">-Context</span></span>
<span data-ttu-id="0fe26-125">Задает контекст для нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fe26-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="0fe26-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fe26-126">-Name</span></span>
<span data-ttu-id="0fe26-127">Задает имя нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fe26-127">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="0fe26-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="0fe26-128">-Permission</span></span>
<span data-ttu-id="0fe26-129">Указывает уровень общедоступного доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="0fe26-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="0fe26-130">По умолчанию контейнер и любые большие двоичные объекты в нем могут быть доступны только владельцу учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fe26-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="0fe26-131">Чтобы предоставить анонимным пользователям разрешения на чтение контейнера и его больших двоичных объектов, вы можете задать разрешения на доступ к контейнеру, чтобы включить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="0fe26-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="0fe26-132">Анонимные пользователи могут читать большие двоичные объекты в общедоступном контейнере без проверки подлинности запроса.</span><span class="sxs-lookup"><span data-stu-id="0fe26-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="0fe26-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0fe26-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fe26-134">Контейнер.</span><span class="sxs-lookup"><span data-stu-id="0fe26-134">Container.</span></span>
<span data-ttu-id="0fe26-135">Предоставляет полный доступ на чтение для контейнера и его больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="0fe26-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="0fe26-136">Клиенты могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса, но не могут перечислять контейнеры в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fe26-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="0fe26-137">Большом.</span><span class="sxs-lookup"><span data-stu-id="0fe26-137">Blob.</span></span>
<span data-ttu-id="0fe26-138">Предоставляет доступ на чтение к данным больших двоичных объектов во всем контейнере с помощью анонимного запроса, но не предоставляет доступ к данным контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fe26-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="0fe26-139">Клиенты не могут перечислять большие двоичные объекты в контейнере с помощью анонимного запроса.</span><span class="sxs-lookup"><span data-stu-id="0fe26-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="0fe26-140">Выйти.</span><span class="sxs-lookup"><span data-stu-id="0fe26-140">Off.</span></span>
<span data-ttu-id="0fe26-141">Которая ограничивает доступ только владельцам учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fe26-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe26-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0fe26-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0fe26-143">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="0fe26-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0fe26-144">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0fe26-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0fe26-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe26-145">CommonParameters</span></span>
<span data-ttu-id="0fe26-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fe26-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe26-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe26-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe26-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fe26-148">INPUTS</span></span>

## <span data-ttu-id="0fe26-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe26-149">OUTPUTS</span></span>

## <span data-ttu-id="0fe26-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fe26-150">NOTES</span></span>

## <span data-ttu-id="0fe26-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fe26-151">RELATED LINKS</span></span>

[<span data-ttu-id="0fe26-152">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0fe26-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="0fe26-153">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0fe26-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="0fe26-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0fe26-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


