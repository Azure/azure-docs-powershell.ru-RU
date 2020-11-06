---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
ms.openlocfilehash: 21293b8262a10c5710ed132413658c3c1cfbd254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558660"
---
# <span data-ttu-id="7561c-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7561c-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="7561c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7561c-102">SYNOPSIS</span></span>
<span data-ttu-id="7561c-103">Задает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="7561c-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7561c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7561c-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7561c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7561c-105">DESCRIPTION</span></span>
<span data-ttu-id="7561c-106">Командлет **Set-AzureStorageCORSRule** задает правила использования общего ресурса для межисточниковой связи между ресурсами (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7561c-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="7561c-107">Типы служб хранилища для этого командлета: блоб, таблица, очередь и файл.</span><span class="sxs-lookup"><span data-stu-id="7561c-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="7561c-108">Этот командлет перезапишет существующие правила.</span><span class="sxs-lookup"><span data-stu-id="7561c-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="7561c-109">Чтобы просмотреть текущие правила, используйте командлет Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="7561c-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="7561c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7561c-110">EXAMPLES</span></span>

### <span data-ttu-id="7561c-111">Пример 1: назначение правил CORS службе больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="7561c-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="7561c-112">Первая команда присваивает массив правил переменной $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="7561c-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="7561c-113">Эта команда использует стандартное расширение в нескольких строках в этом блоке кода.</span><span class="sxs-lookup"><span data-stu-id="7561c-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="7561c-114">Вторая команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="7561c-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="7561c-115">Пример 2: изменение свойств правила CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="7561c-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="7561c-116">Первая команда получает текущие правила CORS для типа больших двоичных объектов с помощью командлета **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="7561c-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="7561c-117">В этой команде правила хранятся в переменной массива $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="7561c-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="7561c-118">Вторая и третья команды изменяют первое правило в $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="7561c-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="7561c-119">Последняя команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="7561c-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="7561c-120">Измененные правила перезаписывают текущие правила CORS.</span><span class="sxs-lookup"><span data-stu-id="7561c-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="7561c-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7561c-121">PARAMETERS</span></span>

### <span data-ttu-id="7561c-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7561c-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7561c-123">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="7561c-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7561c-124">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="7561c-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7561c-125">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7561c-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7561c-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7561c-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7561c-127">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="7561c-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7561c-128">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="7561c-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7561c-129">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="7561c-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7561c-130">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="7561c-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7561c-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="7561c-131">The default value is 10.</span></span>

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

### <span data-ttu-id="7561c-132">-Context</span><span class="sxs-lookup"><span data-stu-id="7561c-132">-Context</span></span>
<span data-ttu-id="7561c-133">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7561c-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7561c-134">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7561c-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7561c-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="7561c-135">-CorsRules</span></span>
<span data-ttu-id="7561c-136">Указывает массив правил CORS.</span><span class="sxs-lookup"><span data-stu-id="7561c-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="7561c-137">Существующие правила можно получить с помощью командлета Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="7561c-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7561c-138">-DefaultProfile</span></span>
<span data-ttu-id="7561c-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7561c-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7561c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7561c-140">-PassThru</span></span>
<span data-ttu-id="7561c-141">Указывает на то, что этот командлет возвращает логическое значение, отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="7561c-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="7561c-142">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7561c-142">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561c-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7561c-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7561c-144">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="7561c-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7561c-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7561c-145">-ServiceType</span></span>
<span data-ttu-id="7561c-146">Указывает тип службы хранилища Azure, для которого этот командлет назначает правила.</span><span class="sxs-lookup"><span data-stu-id="7561c-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="7561c-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7561c-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7561c-148">Большом</span><span class="sxs-lookup"><span data-stu-id="7561c-148">Blob</span></span> 
- <span data-ttu-id="7561c-149">Таблич</span><span class="sxs-lookup"><span data-stu-id="7561c-149">Table</span></span> 
- <span data-ttu-id="7561c-150">Поместить</span><span class="sxs-lookup"><span data-stu-id="7561c-150">Queue</span></span> 
- <span data-ttu-id="7561c-151">Файл</span><span class="sxs-lookup"><span data-stu-id="7561c-151">File</span></span>

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

### <span data-ttu-id="7561c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7561c-152">CommonParameters</span></span>
<span data-ttu-id="7561c-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7561c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7561c-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7561c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7561c-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7561c-155">INPUTS</span></span>

### <span data-ttu-id="7561c-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7561c-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7561c-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7561c-157">OUTPUTS</span></span>

### <span data-ttu-id="7561c-158">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="7561c-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="7561c-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="7561c-159">NOTES</span></span>

## <span data-ttu-id="7561c-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7561c-160">RELATED LINKS</span></span>

[<span data-ttu-id="7561c-161">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7561c-161">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="7561c-162">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7561c-162">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7561c-163">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7561c-163">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


