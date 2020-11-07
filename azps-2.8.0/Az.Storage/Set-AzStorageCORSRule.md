---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 3b2347ae13312f079cee1328fe504644e3cf4e15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720317"
---
# <span data-ttu-id="773f6-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="773f6-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="773f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="773f6-102">SYNOPSIS</span></span>
<span data-ttu-id="773f6-103">Задает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="773f6-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="773f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="773f6-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="773f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="773f6-105">DESCRIPTION</span></span>
<span data-ttu-id="773f6-106">Командлет **Set-AzStorageCORSRule** задает правила использования общего ресурса для межисточниковой связи между ресурсами (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="773f6-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="773f6-107">Типы служб хранилища для этого командлета: блоб, таблица, очередь и файл.</span><span class="sxs-lookup"><span data-stu-id="773f6-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="773f6-108">Этот командлет перезапишет существующие правила.</span><span class="sxs-lookup"><span data-stu-id="773f6-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="773f6-109">Чтобы просмотреть текущие правила, используйте командлет Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="773f6-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="773f6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="773f6-110">EXAMPLES</span></span>

### <span data-ttu-id="773f6-111">Пример 1: назначение правил CORS службе больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="773f6-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="773f6-112">Первая команда присваивает массив правил переменной $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="773f6-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="773f6-113">Эта команда использует стандартное расширение в нескольких строках в этом блоке кода.</span><span class="sxs-lookup"><span data-stu-id="773f6-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="773f6-114">Вторая команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="773f6-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="773f6-115">Пример 2: изменение свойств правила CORS для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="773f6-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="773f6-116">Первая команда получает текущие правила CORS для типа больших двоичных объектов с помощью командлета **Get-AzStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="773f6-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="773f6-117">В этой команде правила хранятся в переменной массива $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="773f6-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="773f6-118">Вторая и третья команды изменяют первое правило в $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="773f6-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="773f6-119">Последняя команда назначает правила в $CorsRules типу службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="773f6-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="773f6-120">Измененные правила перезаписывают текущие правила CORS.</span><span class="sxs-lookup"><span data-stu-id="773f6-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="773f6-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="773f6-121">PARAMETERS</span></span>

### <span data-ttu-id="773f6-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="773f6-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="773f6-123">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="773f6-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="773f6-124">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="773f6-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="773f6-125">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="773f6-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="773f6-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="773f6-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="773f6-127">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="773f6-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="773f6-128">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="773f6-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="773f6-129">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="773f6-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="773f6-130">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="773f6-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="773f6-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="773f6-131">The default value is 10.</span></span>

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

### <span data-ttu-id="773f6-132">-Context</span><span class="sxs-lookup"><span data-stu-id="773f6-132">-Context</span></span>
<span data-ttu-id="773f6-133">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="773f6-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="773f6-134">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="773f6-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="773f6-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="773f6-135">-CorsRules</span></span>
<span data-ttu-id="773f6-136">Указывает массив правил CORS.</span><span class="sxs-lookup"><span data-stu-id="773f6-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="773f6-137">Существующие правила можно получить с помощью командлета Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="773f6-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="773f6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773f6-138">-DefaultProfile</span></span>
<span data-ttu-id="773f6-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="773f6-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773f6-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="773f6-140">-PassThru</span></span>
<span data-ttu-id="773f6-141">Указывает на то, что этот командлет возвращает логическое значение, отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="773f6-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="773f6-142">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="773f6-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="773f6-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="773f6-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="773f6-144">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="773f6-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="773f6-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="773f6-145">-ServiceType</span></span>
<span data-ttu-id="773f6-146">Указывает тип службы хранилища Azure, для которого этот командлет назначает правила.</span><span class="sxs-lookup"><span data-stu-id="773f6-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="773f6-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="773f6-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="773f6-148">Большом</span><span class="sxs-lookup"><span data-stu-id="773f6-148">Blob</span></span> 
- <span data-ttu-id="773f6-149">Таблич</span><span class="sxs-lookup"><span data-stu-id="773f6-149">Table</span></span> 
- <span data-ttu-id="773f6-150">Поместить</span><span class="sxs-lookup"><span data-stu-id="773f6-150">Queue</span></span> 
- <span data-ttu-id="773f6-151">Файл</span><span class="sxs-lookup"><span data-stu-id="773f6-151">File</span></span>

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

### <span data-ttu-id="773f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773f6-152">CommonParameters</span></span>
<span data-ttu-id="773f6-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="773f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773f6-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="773f6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773f6-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="773f6-155">INPUTS</span></span>

### <span data-ttu-id="773f6-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="773f6-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="773f6-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="773f6-157">OUTPUTS</span></span>

### <span data-ttu-id="773f6-158">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="773f6-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="773f6-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="773f6-159">NOTES</span></span>

## <span data-ttu-id="773f6-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="773f6-160">RELATED LINKS</span></span>

[<span data-ttu-id="773f6-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="773f6-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="773f6-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="773f6-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="773f6-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="773f6-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


