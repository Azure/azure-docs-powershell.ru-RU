---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505644"
---
# <span data-ttu-id="0970e-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="0970e-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="0970e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0970e-102">SYNOPSIS</span></span>
<span data-ttu-id="0970e-103">Задает правила CORS для типа службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="0970e-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="0970e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0970e-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0970e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0970e-105">DESCRIPTION</span></span>
<span data-ttu-id="0970e-106">**Cmdlet Set-AzStorageCORSRule** задает правила совместного доступа к ресурсам (CORS) для типа службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0970e-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="0970e-107">Для этого cmdlet могут быть службы хранилища BLOB-файлов, Table, Queue и File.</span><span class="sxs-lookup"><span data-stu-id="0970e-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="0970e-108">Этот cmdlet переописает существующие правила.</span><span class="sxs-lookup"><span data-stu-id="0970e-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="0970e-109">Чтобы увидеть текущие правила, используйте Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="0970e-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="0970e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0970e-110">EXAMPLES</span></span>

### <span data-ttu-id="0970e-111">Пример 1. Назначение правил CORS службе BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="0970e-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="0970e-112">Первая команда назначает массив правил переменной $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="0970e-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="0970e-113">Эта команда использует стандартное расширение над несколькими строками в этом блоке кода.</span><span class="sxs-lookup"><span data-stu-id="0970e-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="0970e-114">Вторая команда назначает правила в $CorsRules типу службы BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="0970e-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="0970e-115">Пример 2. Изменение свойств правила CORS для службы BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="0970e-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="0970e-116">Первая команда получает текущие правила CORS для типа BLOB-типов с помощью командлета **Get-AzStorageCORSRule.**</span><span class="sxs-lookup"><span data-stu-id="0970e-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="0970e-117">Команда сохраняет правила в переменной $CorsRules массива.</span><span class="sxs-lookup"><span data-stu-id="0970e-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="0970e-118">Вторая и третья команды изменяют первое правило в $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="0970e-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="0970e-119">Конечная команда назначает правила в $CorsRules типу службы BLOB-типов.</span><span class="sxs-lookup"><span data-stu-id="0970e-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="0970e-120">Измененные правила переописыют текущие правила CORS.</span><span class="sxs-lookup"><span data-stu-id="0970e-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="0970e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0970e-121">PARAMETERS</span></span>

### <span data-ttu-id="0970e-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0970e-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0970e-123">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0970e-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0970e-124">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="0970e-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0970e-125">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0970e-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0970e-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0970e-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0970e-127">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0970e-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0970e-128">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0970e-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0970e-129">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="0970e-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0970e-130">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="0970e-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0970e-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0970e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="0970e-132">-Контекст</span><span class="sxs-lookup"><span data-stu-id="0970e-132">-Context</span></span>
<span data-ttu-id="0970e-133">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0970e-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0970e-134">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0970e-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0970e-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="0970e-135">-CorsRules</span></span>
<span data-ttu-id="0970e-136">Определяет массив правил КОРС.</span><span class="sxs-lookup"><span data-stu-id="0970e-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="0970e-137">Вы можете восстановить существующие правила с помощью Get-AzStorageCORSRule-управления.</span><span class="sxs-lookup"><span data-stu-id="0970e-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="0970e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0970e-138">-DefaultProfile</span></span>
<span data-ttu-id="0970e-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0970e-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0970e-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0970e-140">-PassThru</span></span>
<span data-ttu-id="0970e-141">Указывает на то, что этот cmdlet возвращает boolean, который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="0970e-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="0970e-142">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0970e-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0970e-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0970e-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0970e-144">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="0970e-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0970e-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0970e-145">-ServiceType</span></span>
<span data-ttu-id="0970e-146">Задает тип службы хранилища Azure, для которой этот cmdlet назначает правила.</span><span class="sxs-lookup"><span data-stu-id="0970e-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="0970e-147">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="0970e-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0970e-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="0970e-148">Blob</span></span> 
- <span data-ttu-id="0970e-149">Таблица</span><span class="sxs-lookup"><span data-stu-id="0970e-149">Table</span></span> 
- <span data-ttu-id="0970e-150">Очередь</span><span class="sxs-lookup"><span data-stu-id="0970e-150">Queue</span></span> 
- <span data-ttu-id="0970e-151">Файл</span><span class="sxs-lookup"><span data-stu-id="0970e-151">File</span></span>

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

### <span data-ttu-id="0970e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0970e-152">CommonParameters</span></span>
<span data-ttu-id="0970e-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0970e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0970e-154">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0970e-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0970e-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0970e-155">INPUTS</span></span>

### <span data-ttu-id="0970e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0970e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0970e-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0970e-157">OUTPUTS</span></span>

### <span data-ttu-id="0970e-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="0970e-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="0970e-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0970e-159">NOTES</span></span>

## <span data-ttu-id="0970e-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0970e-160">RELATED LINKS</span></span>

[<span data-ttu-id="0970e-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="0970e-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="0970e-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0970e-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0970e-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="0970e-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


