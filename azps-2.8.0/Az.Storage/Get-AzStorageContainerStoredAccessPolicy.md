---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 71f00e9e1842eef237a7128d5e20e2ac2116e8a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907082"
---
# <span data-ttu-id="d3232-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3232-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d3232-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3232-102">SYNOPSIS</span></span>
<span data-ttu-id="d3232-103">Получает хранимую политику или политики доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d3232-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3232-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d3232-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3232-105">DESCRIPTION</span></span>
<span data-ttu-id="d3232-106">Командлет **Get-AzStorageContainerStoredAccessPolicy** включает в себя политику и политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d3232-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3232-107">EXAMPLES</span></span>

### <span data-ttu-id="d3232-108">Пример 1: получение политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="d3232-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="d3232-109">Эта команда получает политику доступа с именем Policy22 в контейнере хранения с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="d3232-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="d3232-110">Пример 2: получение всех сохраненных политик доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="d3232-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="d3232-111">Эта команда получает все политики доступа в контейнере хранилища с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="d3232-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="d3232-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3232-112">PARAMETERS</span></span>

### <span data-ttu-id="d3232-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3232-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d3232-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d3232-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d3232-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d3232-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d3232-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3232-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d3232-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d3232-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d3232-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3232-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d3232-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3232-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d3232-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="d3232-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d3232-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="d3232-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d3232-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d3232-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d3232-123">-Container</span><span class="sxs-lookup"><span data-stu-id="d3232-123">-Container</span></span>
<span data-ttu-id="d3232-124">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="d3232-125">-Context</span><span class="sxs-lookup"><span data-stu-id="d3232-125">-Context</span></span>
<span data-ttu-id="d3232-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d3232-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3232-127">-DefaultProfile</span></span>
<span data-ttu-id="d3232-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3232-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d3232-129">-Policy</span></span>
<span data-ttu-id="d3232-130">Указывает политику сохраненных доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="d3232-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="d3232-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3232-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d3232-132">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="d3232-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d3232-133">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3232-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d3232-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3232-134">CommonParameters</span></span>
<span data-ttu-id="d3232-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3232-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3232-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3232-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3232-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3232-137">INPUTS</span></span>

### <span data-ttu-id="d3232-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d3232-138">System.String</span></span>

### <span data-ttu-id="d3232-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3232-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3232-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3232-140">OUTPUTS</span></span>

### <span data-ttu-id="d3232-141">Microsoft. Azure. Storage. BLOB. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="d3232-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="d3232-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3232-142">NOTES</span></span>

## <span data-ttu-id="d3232-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3232-143">RELATED LINKS</span></span>

[<span data-ttu-id="d3232-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3232-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d3232-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3232-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d3232-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3232-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


