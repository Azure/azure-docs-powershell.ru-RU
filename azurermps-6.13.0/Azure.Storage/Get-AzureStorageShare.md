---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93735213"
---
# <span data-ttu-id="2ec53-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ec53-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="2ec53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ec53-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec53-103">Получает список файловых ресурсов общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2ec53-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ec53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ec53-104">SYNTAX</span></span>

### <span data-ttu-id="2ec53-105">MatchingPrefix (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ec53-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec53-106">Относящиеся</span><span class="sxs-lookup"><span data-stu-id="2ec53-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2ec53-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ec53-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec53-108">Командлет **Get-AzureStorageShare** получает список общих файловых ресурсов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2ec53-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="2ec53-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ec53-109">EXAMPLES</span></span>

### <span data-ttu-id="2ec53-110">Пример 1: получение общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="2ec53-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="2ec53-111">Эта команда получает доступ к общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2ec53-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="2ec53-112">Пример 2: получение всех общих файловых ресурсов, начинающихся со строки</span><span class="sxs-lookup"><span data-stu-id="2ec53-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="2ec53-113">Эта команда получает список всех общих файловых ресурсов, имена которых начинаются с contoso.</span><span class="sxs-lookup"><span data-stu-id="2ec53-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="2ec53-114">Пример 3: получение всех общих файловых ресурсов в указанном контексте</span><span class="sxs-lookup"><span data-stu-id="2ec53-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="2ec53-115">Первая команда использует командлет **New-AzureStorageContext** для создания контекста с помощью *локального* параметра, а затем сохраняет этот объект контекста в переменной $context.</span><span class="sxs-lookup"><span data-stu-id="2ec53-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="2ec53-116">Вторая команда получает файловые ресурсы общего доступа для объекта контекста, хранящегося в $Context.</span><span class="sxs-lookup"><span data-stu-id="2ec53-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="2ec53-117">Пример 4: получение снимка общего файлового файла с определенным именем общего доступа и SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2ec53-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="2ec53-118">Эта команда получает снимок общего файлового файла с определенным именем общего доступа и SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="2ec53-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="2ec53-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ec53-119">PARAMETERS</span></span>

### <span data-ttu-id="2ec53-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ec53-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2ec53-121">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2ec53-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2ec53-122">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="2ec53-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2ec53-123">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2ec53-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2ec53-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2ec53-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2ec53-125">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2ec53-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2ec53-126">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2ec53-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2ec53-127">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="2ec53-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2ec53-128">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="2ec53-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2ec53-129">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="2ec53-129">The default value is 10.</span></span>

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

### <span data-ttu-id="2ec53-130">-Context</span><span class="sxs-lookup"><span data-stu-id="2ec53-130">-Context</span></span>
<span data-ttu-id="2ec53-131">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec53-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2ec53-132">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2ec53-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2ec53-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec53-133">-DefaultProfile</span></span>
<span data-ttu-id="2ec53-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec53-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec53-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ec53-135">-Name</span></span>
<span data-ttu-id="2ec53-136">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="2ec53-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="2ec53-137">Этот командлет возвращает общую файловую единицу, указанную в этом параметре, или значение Nothing, если указано несуществующее имя общей файловой панели.</span><span class="sxs-lookup"><span data-stu-id="2ec53-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec53-138">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="2ec53-138">-Prefix</span></span>
<span data-ttu-id="2ec53-139">Указывает префикс для общих файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ec53-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="2ec53-140">Этот командлет получает файловые ресурсы, соответствующие префиксу, указанному в этом параметре, или нет общих файловых ресурсов, если не совпадает ни одного общего файла с указанным префиксом.</span><span class="sxs-lookup"><span data-stu-id="2ec53-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec53-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ec53-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2ec53-142">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="2ec53-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2ec53-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2ec53-143">-SnapshotTime</span></span>
<span data-ttu-id="2ec53-144">SnapshotTimeный снимок общего файлового файла, который вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="2ec53-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec53-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec53-145">CommonParameters</span></span>
<span data-ttu-id="2ec53-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ec53-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec53-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec53-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec53-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ec53-148">INPUTS</span></span>

### <span data-ttu-id="2ec53-149">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ec53-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2ec53-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ec53-150">OUTPUTS</span></span>

### <span data-ttu-id="2ec53-151">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2ec53-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="2ec53-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ec53-152">NOTES</span></span>

## <span data-ttu-id="2ec53-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ec53-153">RELATED LINKS</span></span>

[<span data-ttu-id="2ec53-154">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ec53-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="2ec53-155">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2ec53-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
