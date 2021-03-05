---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002648"
---
# <span data-ttu-id="ddd63-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="ddd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd63-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd63-103">Возвращает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="ddd63-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="ddd63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ddd63-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ddd63-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd63-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd63-106">Для типа службы хранилища Azure с использованием cmdlet **Get-AzStorageCORSRule** задаются правила совместного использования ресурсов (CORS) в разных источниках.</span><span class="sxs-lookup"><span data-stu-id="ddd63-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="ddd63-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd63-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd63-108">Пример 1. Получить правила CORS для службы BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="ddd63-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="ddd63-109">Эта команда получает правила CORS для типа службы BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="ddd63-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="ddd63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddd63-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd63-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ddd63-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ddd63-112">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ddd63-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ddd63-113">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="ddd63-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ddd63-114">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ddd63-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ddd63-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ddd63-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ddd63-116">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="ddd63-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ddd63-117">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ddd63-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ddd63-118">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="ddd63-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ddd63-119">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="ddd63-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ddd63-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ddd63-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ddd63-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ddd63-121">-Context</span></span>
<span data-ttu-id="ddd63-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd63-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ddd63-123">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ddd63-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ddd63-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd63-124">-DefaultProfile</span></span>
<span data-ttu-id="ddd63-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd63-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd63-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ddd63-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ddd63-127">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="ddd63-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ddd63-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ddd63-128">-ServiceType</span></span>
<span data-ttu-id="ddd63-129">Указывает тип службы хранилища Azure, для которой этот cmdlet получает правила CORS.</span><span class="sxs-lookup"><span data-stu-id="ddd63-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="ddd63-130">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ddd63-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd63-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="ddd63-131">Blob</span></span> 
- <span data-ttu-id="ddd63-132">Таблица</span><span class="sxs-lookup"><span data-stu-id="ddd63-132">Table</span></span> 
- <span data-ttu-id="ddd63-133">Очередь</span><span class="sxs-lookup"><span data-stu-id="ddd63-133">Queue</span></span> 
- <span data-ttu-id="ddd63-134">Файл</span><span class="sxs-lookup"><span data-stu-id="ddd63-134">File</span></span>

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

### <span data-ttu-id="ddd63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd63-135">CommonParameters</span></span>
<span data-ttu-id="ddd63-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd63-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd63-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd63-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddd63-138">INPUTS</span></span>

### <span data-ttu-id="ddd63-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ddd63-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ddd63-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddd63-140">OUTPUTS</span></span>

### <span data-ttu-id="ddd63-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="ddd63-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ddd63-142">NOTES</span></span>

## <span data-ttu-id="ddd63-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd63-143">RELATED LINKS</span></span>

[<span data-ttu-id="ddd63-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="ddd63-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ddd63-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


