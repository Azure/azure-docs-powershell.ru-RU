---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 62d2e0cfa96c2085b13416ba8a305acf565b23ee
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914313"
---
# <span data-ttu-id="34076-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34076-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="34076-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34076-102">SYNOPSIS</span></span>
<span data-ttu-id="34076-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="34076-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34076-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34076-104">SYNTAX</span></span>

### <span data-ttu-id="34076-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34076-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="34076-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="34076-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="34076-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34076-107">DESCRIPTION</span></span>
<span data-ttu-id="34076-108">Командлет **Get-AzureStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="34076-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="34076-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34076-109">EXAMPLES</span></span>

### <span data-ttu-id="34076-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="34076-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="34076-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="34076-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="34076-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="34076-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="34076-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="34076-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="34076-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34076-114">PARAMETERS</span></span>

### <span data-ttu-id="34076-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34076-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34076-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="34076-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34076-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="34076-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34076-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="34076-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34076-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34076-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34076-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="34076-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34076-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="34076-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34076-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="34076-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34076-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="34076-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34076-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="34076-124">The default value is 10.</span></span>

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

### <span data-ttu-id="34076-125">-Context</span><span class="sxs-lookup"><span data-stu-id="34076-125">-Context</span></span>
<span data-ttu-id="34076-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="34076-126">Specifies the storage context.</span></span>
<span data-ttu-id="34076-127">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="34076-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="34076-128">Командлет завершится сбоем, если вы используете контекст хранения, созданный из маркера SAS, так как он будет запрашивать разрешения контейнера, требующие разрешения ключа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="34076-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="34076-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="34076-129">-ContinuationToken</span></span>
<span data-ttu-id="34076-130">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="34076-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34076-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34076-131">-DefaultProfile</span></span>
<span data-ttu-id="34076-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34076-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34076-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="34076-133">-MaxCount</span></span>
<span data-ttu-id="34076-134">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="34076-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="34076-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34076-135">-Name</span></span>
<span data-ttu-id="34076-136">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="34076-136">Specifies the container name.</span></span>
<span data-ttu-id="34076-137">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="34076-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="34076-138">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="34076-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="34076-139">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="34076-139">-Prefix</span></span>
<span data-ttu-id="34076-140">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="34076-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="34076-141">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="34076-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="34076-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34076-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34076-143">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="34076-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="34076-144">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="34076-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="34076-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34076-145">CommonParameters</span></span>
<span data-ttu-id="34076-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34076-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34076-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34076-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34076-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34076-148">INPUTS</span></span>

### <span data-ttu-id="34076-149">System. String</span><span class="sxs-lookup"><span data-stu-id="34076-149">System.String</span></span>

### <span data-ttu-id="34076-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34076-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34076-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34076-151">OUTPUTS</span></span>

### <span data-ttu-id="34076-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34076-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="34076-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="34076-153">NOTES</span></span>

## <span data-ttu-id="34076-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34076-154">RELATED LINKS</span></span>

[<span data-ttu-id="34076-155">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34076-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="34076-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34076-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="34076-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="34076-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


