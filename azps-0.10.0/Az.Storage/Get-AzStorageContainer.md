---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 16365ea4f5c2826c173525b90e52fd2103d5d7dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910773"
---
# <span data-ttu-id="af704-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af704-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="af704-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af704-102">SYNOPSIS</span></span>
<span data-ttu-id="af704-103">Список контейнеров хранилища.</span><span class="sxs-lookup"><span data-stu-id="af704-103">Lists the storage containers.</span></span>

## <span data-ttu-id="af704-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af704-104">SYNTAX</span></span>

### <span data-ttu-id="af704-105">ContainerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af704-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="af704-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="af704-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="af704-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af704-107">DESCRIPTION</span></span>
<span data-ttu-id="af704-108">Командлет **Get-AzStorageContainer** перечисляет контейнеры хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="af704-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="af704-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af704-109">EXAMPLES</span></span>

### <span data-ttu-id="af704-110">Пример 1: получение блоба хранилища Azure по имени</span><span class="sxs-lookup"><span data-stu-id="af704-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="af704-111">В этом примере используется подстановочный знак для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="af704-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="af704-112">Пример 2: получение контейнера хранилища Azure по префиксу имени контейнера</span><span class="sxs-lookup"><span data-stu-id="af704-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="af704-113">В этом примере параметр *prefix* используется для возврата списка всех контейнеров с именем, которое начинается с Container.</span><span class="sxs-lookup"><span data-stu-id="af704-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="af704-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af704-114">PARAMETERS</span></span>

### <span data-ttu-id="af704-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af704-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="af704-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="af704-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="af704-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="af704-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="af704-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="af704-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="af704-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="af704-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="af704-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="af704-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="af704-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="af704-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="af704-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="af704-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="af704-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="af704-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="af704-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="af704-124">The default value is 10.</span></span>

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

### <span data-ttu-id="af704-125">-Context</span><span class="sxs-lookup"><span data-stu-id="af704-125">-Context</span></span>
<span data-ttu-id="af704-126">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="af704-126">Specifies the storage context.</span></span>
<span data-ttu-id="af704-127">Чтобы создать его, можно использовать командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="af704-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="af704-128">Командлет завершится сбоем, если вы используете контекст хранения, созданный из маркера SAS, так как он будет запрашивать разрешения контейнера, требующие разрешения ключа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="af704-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="af704-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="af704-129">-ContinuationToken</span></span>
<span data-ttu-id="af704-130">Указывает маркер продолжения для списка больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="af704-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af704-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af704-131">-DefaultProfile</span></span>
<span data-ttu-id="af704-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af704-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af704-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="af704-133">-MaxCount</span></span>
<span data-ttu-id="af704-134">Задает максимальное количество объектов, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="af704-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="af704-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af704-135">-Name</span></span>
<span data-ttu-id="af704-136">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="af704-136">Specifies the container name.</span></span>
<span data-ttu-id="af704-137">Если имя контейнера пусто, командлет выводит список всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="af704-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="af704-138">В противном случае выводится список всех контейнеров, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="af704-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="af704-139">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="af704-139">-Prefix</span></span>
<span data-ttu-id="af704-140">Задает префикс, используемый в имени контейнера или контейнеров, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="af704-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="af704-141">Вы можете использовать этот параметр, чтобы найти все контейнеры, которые начинаются с одной строки, например "My" или "тест".</span><span class="sxs-lookup"><span data-stu-id="af704-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="af704-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af704-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="af704-143">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="af704-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="af704-144">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="af704-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="af704-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af704-145">CommonParameters</span></span>
<span data-ttu-id="af704-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af704-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af704-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af704-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af704-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af704-148">INPUTS</span></span>

### <span data-ttu-id="af704-149">System. String</span><span class="sxs-lookup"><span data-stu-id="af704-149">System.String</span></span>

### <span data-ttu-id="af704-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="af704-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="af704-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af704-151">OUTPUTS</span></span>

### <span data-ttu-id="af704-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af704-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="af704-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="af704-153">NOTES</span></span>

## <span data-ttu-id="af704-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af704-154">RELATED LINKS</span></span>

[<span data-ttu-id="af704-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af704-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="af704-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af704-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="af704-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="af704-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


