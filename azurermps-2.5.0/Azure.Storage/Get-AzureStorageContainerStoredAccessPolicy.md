---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0b734acb6d1a0d491a0b9e6397f7ae9af2645b35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913519"
---
# <span data-ttu-id="d1938-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1938-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d1938-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1938-102">SYNOPSIS</span></span>
<span data-ttu-id="d1938-103">Получает хранимую политику или политики доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1938-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1938-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d1938-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1938-105">DESCRIPTION</span></span>
<span data-ttu-id="d1938-106">Командлет **Get-AzureStorageContainerStoredAccessPolicy** включает в себя политику и политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d1938-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1938-107">EXAMPLES</span></span>

### <span data-ttu-id="d1938-108">Пример 1: получение политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="d1938-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="d1938-109">Эта команда получает политику доступа с именем Policy22 в контейнере хранения с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="d1938-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="d1938-110">Пример 2: получение всех сохраненных политик доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="d1938-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="d1938-111">Эта команда получает все политики доступа в контейнере хранилища с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="d1938-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="d1938-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1938-112">PARAMETERS</span></span>

### <span data-ttu-id="d1938-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1938-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d1938-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d1938-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d1938-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d1938-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d1938-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d1938-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d1938-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d1938-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d1938-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d1938-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d1938-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d1938-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d1938-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="d1938-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d1938-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="d1938-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d1938-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d1938-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d1938-123">-Container</span><span class="sxs-lookup"><span data-stu-id="d1938-123">-Container</span></span>
<span data-ttu-id="d1938-124">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="d1938-125">-Context</span><span class="sxs-lookup"><span data-stu-id="d1938-125">-Context</span></span>
<span data-ttu-id="d1938-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d1938-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1938-127">-DefaultProfile</span></span>
<span data-ttu-id="d1938-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1938-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d1938-129">-Policy</span></span>
<span data-ttu-id="d1938-130">Указывает политику сохраненных доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="d1938-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="d1938-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1938-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d1938-132">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="d1938-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d1938-133">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d1938-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d1938-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1938-134">CommonParameters</span></span>
<span data-ttu-id="d1938-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1938-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1938-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1938-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1938-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1938-137">INPUTS</span></span>

### <span data-ttu-id="d1938-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d1938-138">System.String</span></span>

### <span data-ttu-id="d1938-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1938-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1938-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1938-140">OUTPUTS</span></span>

### <span data-ttu-id="d1938-141">Microsoft. WindowsAzure. Storage. BLOB. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="d1938-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="d1938-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1938-142">NOTES</span></span>

## <span data-ttu-id="d1938-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1938-143">RELATED LINKS</span></span>

[<span data-ttu-id="d1938-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1938-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d1938-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1938-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d1938-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1938-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


