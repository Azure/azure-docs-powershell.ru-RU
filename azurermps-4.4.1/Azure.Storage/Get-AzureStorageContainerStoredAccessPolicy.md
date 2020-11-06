---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570191"
---
# <span data-ttu-id="eb1bf-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb1bf-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="eb1bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1bf-103">Получает хранимую политику или политики доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb1bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb1bf-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="eb1bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1bf-106">Командлет **Get-AzureStorageContainerStoredAccessPolicy** включает в себя политику и политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="eb1bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb1bf-107">EXAMPLES</span></span>

### <span data-ttu-id="eb1bf-108">Пример 1: получение политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="eb1bf-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="eb1bf-109">Эта команда получает политику доступа с именем Policy22 в контейнере хранения с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="eb1bf-110">Пример 2: получение всех сохраненных политик доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="eb1bf-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="eb1bf-111">Эта команда получает все политики доступа в контейнере хранилища с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="eb1bf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb1bf-112">PARAMETERS</span></span>

### <span data-ttu-id="eb1bf-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eb1bf-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eb1bf-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eb1bf-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eb1bf-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eb1bf-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eb1bf-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eb1bf-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eb1bf-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eb1bf-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eb1bf-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eb1bf-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-122">The default value is 10.</span></span>

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

### <span data-ttu-id="eb1bf-123">-Container</span><span class="sxs-lookup"><span data-stu-id="eb1bf-123">-Container</span></span>
<span data-ttu-id="eb1bf-124">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1bf-125">-Context</span><span class="sxs-lookup"><span data-stu-id="eb1bf-125">-Context</span></span>
<span data-ttu-id="eb1bf-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="eb1bf-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="eb1bf-127">-Policy</span></span>
<span data-ttu-id="eb1bf-128">Указывает политику сохраненных доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1bf-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eb1bf-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eb1bf-130">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="eb1bf-131">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="eb1bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1bf-132">CommonParameters</span></span>
<span data-ttu-id="eb1bf-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1bf-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1bf-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb1bf-135">INPUTS</span></span>

### <span data-ttu-id="eb1bf-136">Подстрок</span><span class="sxs-lookup"><span data-stu-id="eb1bf-136">String</span></span>

<span data-ttu-id="eb1bf-137">Параметр "контейнер" принимает значение типа "String" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="eb1bf-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb1bf-138">IStorageContext</span></span>

<span data-ttu-id="eb1bf-139">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb1bf-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="eb1bf-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb1bf-140">OUTPUTS</span></span>

### <span data-ttu-id="eb1bf-141">Microsoft. WindowsAzure. Storage. BLOB. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="eb1bf-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="eb1bf-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb1bf-142">NOTES</span></span>

## <span data-ttu-id="eb1bf-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb1bf-143">RELATED LINKS</span></span>

[<span data-ttu-id="eb1bf-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb1bf-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="eb1bf-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb1bf-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="eb1bf-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb1bf-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


