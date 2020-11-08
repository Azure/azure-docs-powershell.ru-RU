---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073158"
---
# <span data-ttu-id="6e477-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e477-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="6e477-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e477-102">SYNOPSIS</span></span>
<span data-ttu-id="6e477-103">Получает хранимую политику или политики доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="6e477-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e477-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6e477-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e477-105">DESCRIPTION</span></span>
<span data-ttu-id="6e477-106">Командлет **Get-AzStorageContainerStoredAccessPolicy** включает в себя политику и политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="6e477-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e477-107">EXAMPLES</span></span>

### <span data-ttu-id="6e477-108">Пример 1: получение политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="6e477-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="6e477-109">Эта команда получает политику доступа с именем Policy22 в контейнере хранения с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="6e477-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="6e477-110">Пример 2: получение всех сохраненных политик доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="6e477-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="6e477-111">Эта команда получает все политики доступа в контейнере хранилища с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="6e477-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="6e477-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e477-112">PARAMETERS</span></span>

### <span data-ttu-id="6e477-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e477-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e477-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6e477-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6e477-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6e477-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6e477-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e477-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6e477-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e477-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e477-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6e477-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6e477-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6e477-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6e477-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="6e477-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6e477-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="6e477-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6e477-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6e477-122">The default value is 10.</span></span>

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

### <span data-ttu-id="6e477-123">-Container</span><span class="sxs-lookup"><span data-stu-id="6e477-123">-Container</span></span>
<span data-ttu-id="6e477-124">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e477-125">-Context</span><span class="sxs-lookup"><span data-stu-id="6e477-125">-Context</span></span>
<span data-ttu-id="6e477-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="6e477-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e477-127">-DefaultProfile</span></span>
<span data-ttu-id="6e477-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e477-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="6e477-129">-Policy</span></span>
<span data-ttu-id="6e477-130">Указывает политику сохраненных доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="6e477-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e477-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e477-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e477-132">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="6e477-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6e477-133">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e477-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6e477-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e477-134">CommonParameters</span></span>
<span data-ttu-id="6e477-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e477-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e477-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e477-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e477-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e477-137">INPUTS</span></span>

### <span data-ttu-id="6e477-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6e477-138">System.String</span></span>

### <span data-ttu-id="6e477-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e477-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e477-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e477-140">OUTPUTS</span></span>

### <span data-ttu-id="6e477-141">Microsoft. Azure. Storage. BLOB. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="6e477-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="6e477-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e477-142">NOTES</span></span>

## <span data-ttu-id="6e477-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e477-143">RELATED LINKS</span></span>

[<span data-ttu-id="6e477-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e477-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e477-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e477-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e477-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e477-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


