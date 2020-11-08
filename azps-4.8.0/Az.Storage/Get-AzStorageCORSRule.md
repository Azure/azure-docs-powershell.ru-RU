---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077527"
---
# <span data-ttu-id="a8592-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8592-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="a8592-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8592-102">SYNOPSIS</span></span>
<span data-ttu-id="a8592-103">Возвращает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a8592-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="a8592-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8592-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a8592-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8592-105">DESCRIPTION</span></span>
<span data-ttu-id="a8592-106">Командлет **Get-AzStorageCORSRule** получает междоменные правила общего разделения ресурсов (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a8592-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="a8592-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8592-107">EXAMPLES</span></span>

### <span data-ttu-id="a8592-108">Пример 1: получение правил CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="a8592-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="a8592-109">Эта команда получает правила CORS для типа службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="a8592-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="a8592-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8592-110">PARAMETERS</span></span>

### <span data-ttu-id="a8592-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8592-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a8592-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a8592-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a8592-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="a8592-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a8592-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a8592-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a8592-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a8592-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a8592-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a8592-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a8592-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a8592-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a8592-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="a8592-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a8592-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="a8592-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a8592-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a8592-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a8592-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a8592-121">-Context</span></span>
<span data-ttu-id="a8592-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a8592-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a8592-123">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a8592-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8592-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8592-124">-DefaultProfile</span></span>
<span data-ttu-id="a8592-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8592-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8592-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8592-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a8592-127">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="a8592-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a8592-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a8592-128">-ServiceType</span></span>
<span data-ttu-id="a8592-129">Указывает тип службы хранилища Azure, для которого этот командлет получает правила CORS.</span><span class="sxs-lookup"><span data-stu-id="a8592-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="a8592-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a8592-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8592-131">Большом</span><span class="sxs-lookup"><span data-stu-id="a8592-131">Blob</span></span> 
- <span data-ttu-id="a8592-132">Таблич</span><span class="sxs-lookup"><span data-stu-id="a8592-132">Table</span></span> 
- <span data-ttu-id="a8592-133">Поместить</span><span class="sxs-lookup"><span data-stu-id="a8592-133">Queue</span></span> 
- <span data-ttu-id="a8592-134">Файл</span><span class="sxs-lookup"><span data-stu-id="a8592-134">File</span></span>

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

### <span data-ttu-id="a8592-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8592-135">CommonParameters</span></span>
<span data-ttu-id="a8592-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8592-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8592-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8592-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8592-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8592-138">INPUTS</span></span>

### <span data-ttu-id="a8592-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8592-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a8592-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8592-140">OUTPUTS</span></span>

### <span data-ttu-id="a8592-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="a8592-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="a8592-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8592-142">NOTES</span></span>

## <span data-ttu-id="a8592-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8592-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8592-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8592-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="a8592-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8592-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


