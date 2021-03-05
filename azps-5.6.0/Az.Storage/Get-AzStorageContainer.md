---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981528"
---
# <span data-ttu-id="c7808-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7808-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="c7808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7808-102">SYNOPSIS</span></span>
<span data-ttu-id="c7808-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7808-103">Lists the storage containers.</span></span>

## <span data-ttu-id="c7808-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7808-104">SYNTAX</span></span>

### <span data-ttu-id="c7808-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7808-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c7808-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="c7808-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c7808-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7808-107">DESCRIPTION</span></span>
<span data-ttu-id="c7808-108">С **помощью cmdlet get-AzStorageContainer** выведет список контейнеров хранилища, связанных с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="c7808-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c7808-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7808-109">EXAMPLES</span></span>

### <span data-ttu-id="c7808-110">Пример 1. Получить BLOB-клиент хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="c7808-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="c7808-111">В этом примере используется поддиавный знак для возврата списка всех контейнеров с именем, которое начинается с контейнера.</span><span class="sxs-lookup"><span data-stu-id="c7808-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="c7808-112">Пример 2. Получите контейнер хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="c7808-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="c7808-113">В этом примере параметр *Prefix* используется для возврата списка всех контейнеров с именем, которое начинается с контейнера.</span><span class="sxs-lookup"><span data-stu-id="c7808-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="c7808-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7808-114">PARAMETERS</span></span>

### <span data-ttu-id="c7808-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7808-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7808-116">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c7808-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7808-117">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="c7808-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7808-118">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c7808-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7808-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7808-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7808-120">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="c7808-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7808-121">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="c7808-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7808-122">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="c7808-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7808-123">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="c7808-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7808-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c7808-124">The default value is 10.</span></span>

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

### <span data-ttu-id="c7808-125">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c7808-125">-Context</span></span>
<span data-ttu-id="c7808-126">Определяет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7808-126">Specifies the storage context.</span></span>
<span data-ttu-id="c7808-127">Для этого можно использовать New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="c7808-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c7808-128">Разрешения контейнера не будут восстановлены при использовании контекста хранилища, созданного из токена SAS, так как для этого требуются разрешения на использование ключа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c7808-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="c7808-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c7808-129">-ContinuationToken</span></span>
<span data-ttu-id="c7808-130">Указывает маркер продолжения для списка BLOB-приложений.</span><span class="sxs-lookup"><span data-stu-id="c7808-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="c7808-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7808-131">-DefaultProfile</span></span>
<span data-ttu-id="c7808-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7808-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7808-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c7808-133">-MaxCount</span></span>
<span data-ttu-id="c7808-134">Указывает максимальное количество объектов, возвращаемых этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7808-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="c7808-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c7808-135">-Name</span></span>
<span data-ttu-id="c7808-136">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="c7808-136">Specifies the container name.</span></span>
<span data-ttu-id="c7808-137">Если имя контейнера пустое, в нем будет указан список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c7808-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="c7808-138">В противном случае будут перечислены все контейнеры, которые соответствуют указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="c7808-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="c7808-139">-Префикс</span><span class="sxs-lookup"><span data-stu-id="c7808-139">-Prefix</span></span>
<span data-ttu-id="c7808-140">Указывает префикс, используемый в имени нужного контейнера или контейнера.</span><span class="sxs-lookup"><span data-stu-id="c7808-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="c7808-141">С помощью этого можно найти все контейнеры, которые начинаются с одной и той же строки, например "мой" или "тест".</span><span class="sxs-lookup"><span data-stu-id="c7808-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="c7808-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7808-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7808-143">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c7808-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c7808-144">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c7808-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c7808-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7808-145">CommonParameters</span></span>
<span data-ttu-id="c7808-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7808-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7808-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7808-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7808-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7808-148">INPUTS</span></span>

### <span data-ttu-id="c7808-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c7808-149">System.String</span></span>

### <span data-ttu-id="c7808-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7808-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7808-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7808-151">OUTPUTS</span></span>

### <span data-ttu-id="c7808-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7808-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c7808-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7808-153">NOTES</span></span>

## <span data-ttu-id="c7808-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7808-154">RELATED LINKS</span></span>

[<span data-ttu-id="c7808-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7808-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="c7808-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7808-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="c7808-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c7808-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


