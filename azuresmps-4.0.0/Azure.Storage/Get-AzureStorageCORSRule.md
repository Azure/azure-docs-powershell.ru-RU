---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556275"
---
# <span data-ttu-id="5de96-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5de96-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="5de96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5de96-102">SYNOPSIS</span></span>
<span data-ttu-id="5de96-103">Возвращает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="5de96-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="5de96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5de96-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5de96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5de96-105">DESCRIPTION</span></span>
<span data-ttu-id="5de96-106">Командлет **Get-AzureStorageCORSRule** получает междоменные правила общего разделения ресурсов (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5de96-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="5de96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5de96-107">EXAMPLES</span></span>

### <span data-ttu-id="5de96-108">Пример 1: получение правил CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="5de96-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="5de96-109">Эта команда получает правила CORS для типа службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="5de96-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="5de96-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5de96-110">PARAMETERS</span></span>

### <span data-ttu-id="5de96-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5de96-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5de96-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5de96-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5de96-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5de96-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5de96-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5de96-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5de96-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5de96-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5de96-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5de96-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5de96-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5de96-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5de96-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="5de96-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5de96-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="5de96-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5de96-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="5de96-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5de96-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5de96-121">-Context</span></span>
<span data-ttu-id="5de96-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5de96-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5de96-123">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5de96-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5de96-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5de96-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5de96-125">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="5de96-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5de96-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5de96-126">-ServiceType</span></span>
<span data-ttu-id="5de96-127">Указывает тип службы хранилища Azure, для которого этот командлет получает правила CORS.</span><span class="sxs-lookup"><span data-stu-id="5de96-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="5de96-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5de96-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5de96-129">Большом</span><span class="sxs-lookup"><span data-stu-id="5de96-129">Blob</span></span> 
- <span data-ttu-id="5de96-130">Таблич</span><span class="sxs-lookup"><span data-stu-id="5de96-130">Table</span></span> 
- <span data-ttu-id="5de96-131">Поместить</span><span class="sxs-lookup"><span data-stu-id="5de96-131">Queue</span></span> 
- <span data-ttu-id="5de96-132">Файл</span><span class="sxs-lookup"><span data-stu-id="5de96-132">File</span></span>

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

### <span data-ttu-id="5de96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de96-133">CommonParameters</span></span>
<span data-ttu-id="5de96-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5de96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de96-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de96-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de96-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5de96-136">INPUTS</span></span>

## <span data-ttu-id="5de96-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5de96-137">OUTPUTS</span></span>

###  
<span data-ttu-id="5de96-138">Этот командлет возвращает массив объектов **PSCORSRule** , которые представляют правила CORS, в настоящее время находящиеся в службе.</span><span class="sxs-lookup"><span data-stu-id="5de96-138">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="5de96-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5de96-139">NOTES</span></span>

## <span data-ttu-id="5de96-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5de96-140">RELATED LINKS</span></span>

[<span data-ttu-id="5de96-141">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5de96-141">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="5de96-142">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5de96-142">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


