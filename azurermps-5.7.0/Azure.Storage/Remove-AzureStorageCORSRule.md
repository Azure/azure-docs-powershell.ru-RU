---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
ms.openlocfilehash: 873cee6ce1f724fb925ae743133ecfb9a1a5210a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561960"
---
# <span data-ttu-id="c0d51-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c0d51-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="c0d51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0d51-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d51-103">Удаляет CORS для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="c0d51-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0d51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0d51-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0d51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d51-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d51-106">Командлет **Remove-AzureStorageCORSRule** удаляет межисточниковый доступ к ресурсам (CORS) для службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d51-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="c0d51-107">Этот командлет удаляет все правила CORS в типе службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="c0d51-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="c0d51-108">Типы служб хранилища для этого командлета: блоб, таблица, очередь и файл.</span><span class="sxs-lookup"><span data-stu-id="c0d51-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="c0d51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0d51-109">EXAMPLES</span></span>

### <span data-ttu-id="c0d51-110">Пример 1: удаление правил CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="c0d51-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="c0d51-111">Эта команда удаляет правила CORS для типа службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="c0d51-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="c0d51-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0d51-112">PARAMETERS</span></span>

### <span data-ttu-id="c0d51-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0d51-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0d51-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c0d51-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0d51-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="c0d51-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0d51-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0d51-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0d51-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0d51-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0d51-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c0d51-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0d51-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c0d51-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0d51-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="c0d51-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0d51-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="c0d51-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0d51-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c0d51-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c0d51-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c0d51-123">-Context</span></span>
<span data-ttu-id="c0d51-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d51-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c0d51-125">Чтобы получить контекст хранилища, New-AzureStorageContext командлет.</span><span class="sxs-lookup"><span data-stu-id="c0d51-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c0d51-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0d51-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0d51-127">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="c0d51-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0d51-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c0d51-128">-ServiceType</span></span>
<span data-ttu-id="c0d51-129">Указывает тип службы хранилища Azure, для которого этот командлет удаляет правила.</span><span class="sxs-lookup"><span data-stu-id="c0d51-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="c0d51-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c0d51-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0d51-131">Большом</span><span class="sxs-lookup"><span data-stu-id="c0d51-131">Blob</span></span> 
- <span data-ttu-id="c0d51-132">Таблич</span><span class="sxs-lookup"><span data-stu-id="c0d51-132">Table</span></span> 
- <span data-ttu-id="c0d51-133">Поместить</span><span class="sxs-lookup"><span data-stu-id="c0d51-133">Queue</span></span> 
- <span data-ttu-id="c0d51-134">Файл</span><span class="sxs-lookup"><span data-stu-id="c0d51-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d51-135">CommonParameters</span></span>
<span data-ttu-id="c0d51-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0d51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d51-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d51-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d51-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0d51-138">INPUTS</span></span>

### <span data-ttu-id="c0d51-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0d51-139">IStorageContext</span></span>

<span data-ttu-id="c0d51-140">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0d51-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="c0d51-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d51-141">OUTPUTS</span></span>

## <span data-ttu-id="c0d51-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0d51-142">NOTES</span></span>

## <span data-ttu-id="c0d51-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0d51-143">RELATED LINKS</span></span>

[<span data-ttu-id="c0d51-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c0d51-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="c0d51-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c0d51-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


