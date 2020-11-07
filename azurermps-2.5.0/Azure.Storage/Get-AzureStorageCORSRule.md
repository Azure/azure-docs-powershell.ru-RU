---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: cf9f4b3a6d58754c4b992163625887afcb3439b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913948"
---
# <span data-ttu-id="bfb6d-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bfb6d-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="bfb6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb6d-103">Возвращает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfb6d-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bfb6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb6d-106">Командлет **Get-AzureStorageCORSRule** получает междоменные правила общего разделения ресурсов (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="bfb6d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfb6d-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb6d-108">Пример 1: получение правил CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="bfb6d-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="bfb6d-109">Эта команда получает правила CORS для типа службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="bfb6d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfb6d-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb6d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bfb6d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bfb6d-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bfb6d-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bfb6d-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bfb6d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bfb6d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bfb6d-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bfb6d-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bfb6d-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bfb6d-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bfb6d-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bfb6d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="bfb6d-121">-Context</span></span>
<span data-ttu-id="bfb6d-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bfb6d-123">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bfb6d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb6d-124">-DefaultProfile</span></span>
<span data-ttu-id="bfb6d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb6d-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bfb6d-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bfb6d-127">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bfb6d-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bfb6d-128">-ServiceType</span></span>
<span data-ttu-id="bfb6d-129">Указывает тип службы хранилища Azure, для которого этот командлет получает правила CORS.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="bfb6d-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bfb6d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bfb6d-131">Большом</span><span class="sxs-lookup"><span data-stu-id="bfb6d-131">Blob</span></span> 
- <span data-ttu-id="bfb6d-132">Таблич</span><span class="sxs-lookup"><span data-stu-id="bfb6d-132">Table</span></span> 
- <span data-ttu-id="bfb6d-133">Поместить</span><span class="sxs-lookup"><span data-stu-id="bfb6d-133">Queue</span></span> 
- <span data-ttu-id="bfb6d-134">Файл</span><span class="sxs-lookup"><span data-stu-id="bfb6d-134">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb6d-135">CommonParameters</span></span>
<span data-ttu-id="bfb6d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb6d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb6d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb6d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfb6d-138">INPUTS</span></span>

### <span data-ttu-id="bfb6d-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bfb6d-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bfb6d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb6d-140">OUTPUTS</span></span>

### <span data-ttu-id="bfb6d-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="bfb6d-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="bfb6d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfb6d-142">NOTES</span></span>

## <span data-ttu-id="bfb6d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfb6d-143">RELATED LINKS</span></span>

[<span data-ttu-id="bfb6d-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bfb6d-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="bfb6d-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bfb6d-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


