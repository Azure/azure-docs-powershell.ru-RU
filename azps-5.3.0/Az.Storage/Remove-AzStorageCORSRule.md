---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517041"
---
# <span data-ttu-id="4e226-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4e226-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="4e226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e226-102">SYNOPSIS</span></span>
<span data-ttu-id="4e226-103">Удаляет CORS для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="4e226-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="4e226-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e226-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4e226-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e226-105">DESCRIPTION</span></span>
<span data-ttu-id="4e226-106">Для службы хранилища Azure общий доступ к ресурсам в разных источниках удаляется с использованием cmdlet **Remove-AzStorageCORSRule.**</span><span class="sxs-lookup"><span data-stu-id="4e226-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="4e226-107">Этот cmdlet удаляет все правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="4e226-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="4e226-108">Для этого cmdlet могут быть службы хранилища BLOB-файлов, Table, Queue и File.</span><span class="sxs-lookup"><span data-stu-id="4e226-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="4e226-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e226-109">EXAMPLES</span></span>

### <span data-ttu-id="4e226-110">Пример 1. Удаление правил CORS для службы BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="4e226-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="4e226-111">Эта команда удаляет правила CORS для типа службы BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="4e226-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="4e226-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e226-112">PARAMETERS</span></span>

### <span data-ttu-id="4e226-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e226-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4e226-114">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4e226-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4e226-115">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="4e226-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4e226-116">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4e226-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4e226-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4e226-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4e226-118">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4e226-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4e226-119">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4e226-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4e226-120">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="4e226-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4e226-121">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="4e226-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4e226-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4e226-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4e226-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4e226-123">-Context</span></span>
<span data-ttu-id="4e226-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e226-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4e226-125">Чтобы получить контекст хранилища, New-AzStorageContext его.</span><span class="sxs-lookup"><span data-stu-id="4e226-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4e226-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e226-126">-DefaultProfile</span></span>
<span data-ttu-id="4e226-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e226-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e226-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e226-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4e226-129">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="4e226-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4e226-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4e226-130">-ServiceType</span></span>
<span data-ttu-id="4e226-131">Указывает тип службы хранилища Azure, для которой этот cmdlet удаляет правила.</span><span class="sxs-lookup"><span data-stu-id="4e226-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="4e226-132">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="4e226-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e226-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="4e226-133">Blob</span></span> 
- <span data-ttu-id="4e226-134">Таблица</span><span class="sxs-lookup"><span data-stu-id="4e226-134">Table</span></span> 
- <span data-ttu-id="4e226-135">Очередь</span><span class="sxs-lookup"><span data-stu-id="4e226-135">Queue</span></span> 
- <span data-ttu-id="4e226-136">Файл</span><span class="sxs-lookup"><span data-stu-id="4e226-136">File</span></span>

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

### <span data-ttu-id="4e226-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e226-137">CommonParameters</span></span>
<span data-ttu-id="4e226-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e226-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e226-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e226-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e226-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e226-140">INPUTS</span></span>

### <span data-ttu-id="4e226-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e226-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e226-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e226-142">OUTPUTS</span></span>

### <span data-ttu-id="4e226-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="4e226-143">System.Void</span></span>

## <span data-ttu-id="4e226-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e226-144">NOTES</span></span>

## <span data-ttu-id="4e226-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e226-145">RELATED LINKS</span></span>

[<span data-ttu-id="4e226-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4e226-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="4e226-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4e226-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


