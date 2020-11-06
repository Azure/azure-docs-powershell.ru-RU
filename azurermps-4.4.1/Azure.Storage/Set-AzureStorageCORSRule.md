---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568381"
---
# <span data-ttu-id="a34b2-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a34b2-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="a34b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a34b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a34b2-103">Задает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a34b2-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a34b2-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a34b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a34b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a34b2-106">Командлет **Set-AzureStorageCORSRule** задает правила использования общего ресурса для межисточниковой связи между ресурсами (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a34b2-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="a34b2-107">Типы служб хранилища для этого командлета: блоб, таблица, очередь и файл.</span><span class="sxs-lookup"><span data-stu-id="a34b2-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="a34b2-108">Этот командлет перезапишет существующие правила.</span><span class="sxs-lookup"><span data-stu-id="a34b2-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="a34b2-109">Чтобы просмотреть текущие правила, используйте командлет Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="a34b2-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="a34b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a34b2-110">EXAMPLES</span></span>

### <span data-ttu-id="a34b2-111">Пример 1: назначение правил CORS службе больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="a34b2-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="a34b2-112">Первая команда присваивает массив правил переменной $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="a34b2-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="a34b2-113">Эта команда использует стандартное расширение в нескольких строках в этом блоке кода.</span><span class="sxs-lookup"><span data-stu-id="a34b2-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="a34b2-114">Вторая команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="a34b2-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="a34b2-115">Пример 2: изменение свойств правила CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="a34b2-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="a34b2-116">Первая команда получает текущие правила CORS для типа больших двоичных объектов с помощью командлета **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="a34b2-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="a34b2-117">В этой команде правила хранятся в переменной массива $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="a34b2-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="a34b2-118">Вторая и третья команды изменяют первое правило в $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="a34b2-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="a34b2-119">Последняя команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="a34b2-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="a34b2-120">Измененные правила перезаписывают текущие правила CORS.</span><span class="sxs-lookup"><span data-stu-id="a34b2-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="a34b2-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a34b2-121">PARAMETERS</span></span>

### <span data-ttu-id="a34b2-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a34b2-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a34b2-123">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a34b2-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a34b2-124">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="a34b2-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a34b2-125">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a34b2-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a34b2-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a34b2-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a34b2-127">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a34b2-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a34b2-128">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a34b2-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a34b2-129">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="a34b2-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a34b2-130">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="a34b2-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a34b2-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a34b2-131">The default value is 10.</span></span>

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

### <span data-ttu-id="a34b2-132">-Context</span><span class="sxs-lookup"><span data-stu-id="a34b2-132">-Context</span></span>
<span data-ttu-id="a34b2-133">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a34b2-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a34b2-134">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a34b2-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a34b2-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="a34b2-135">-CorsRules</span></span>
<span data-ttu-id="a34b2-136">Указывает массив правил CORS.</span><span class="sxs-lookup"><span data-stu-id="a34b2-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="a34b2-137">Существующие правила можно получить с помощью командлета Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="a34b2-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34b2-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a34b2-138">-PassThru</span></span>
<span data-ttu-id="a34b2-139">Указывает на то, что этот командлет возвращает логическое значение, отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="a34b2-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="a34b2-140">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a34b2-140">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34b2-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a34b2-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a34b2-142">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="a34b2-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a34b2-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a34b2-143">-ServiceType</span></span>
<span data-ttu-id="a34b2-144">Указывает тип службы хранилища Azure, для которого этот командлет назначает правила.</span><span class="sxs-lookup"><span data-stu-id="a34b2-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="a34b2-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a34b2-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a34b2-146">Большом</span><span class="sxs-lookup"><span data-stu-id="a34b2-146">Blob</span></span> 
- <span data-ttu-id="a34b2-147">Таблич</span><span class="sxs-lookup"><span data-stu-id="a34b2-147">Table</span></span> 
- <span data-ttu-id="a34b2-148">Поместить</span><span class="sxs-lookup"><span data-stu-id="a34b2-148">Queue</span></span> 
- <span data-ttu-id="a34b2-149">Файл</span><span class="sxs-lookup"><span data-stu-id="a34b2-149">File</span></span>

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

### <span data-ttu-id="a34b2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34b2-150">CommonParameters</span></span>
<span data-ttu-id="a34b2-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a34b2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34b2-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34b2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34b2-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a34b2-153">INPUTS</span></span>

### <span data-ttu-id="a34b2-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a34b2-154">IStorageContext</span></span>

<span data-ttu-id="a34b2-155">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a34b2-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a34b2-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a34b2-156">OUTPUTS</span></span>

### <span data-ttu-id="a34b2-157">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="a34b2-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="a34b2-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="a34b2-158">NOTES</span></span>

## <span data-ttu-id="a34b2-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a34b2-159">RELATED LINKS</span></span>

[<span data-ttu-id="a34b2-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a34b2-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="a34b2-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a34b2-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a34b2-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a34b2-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


