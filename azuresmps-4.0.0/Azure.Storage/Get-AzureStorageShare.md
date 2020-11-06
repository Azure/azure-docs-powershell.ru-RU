---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556232"
---
# <span data-ttu-id="f1b26-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1b26-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="f1b26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1b26-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b26-103">Получает список файловых ресурсов общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f1b26-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="f1b26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1b26-104">SYNTAX</span></span>

### <span data-ttu-id="f1b26-105">MatchingPrefix (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1b26-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f1b26-106">Относящиеся</span><span class="sxs-lookup"><span data-stu-id="f1b26-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f1b26-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1b26-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b26-108">Командлет **Get-AzureStorageShare** получает список общих файловых ресурсов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f1b26-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="f1b26-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1b26-109">EXAMPLES</span></span>

### <span data-ttu-id="f1b26-110">Пример 1: получение общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="f1b26-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="f1b26-111">Эта команда получает доступ к общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f1b26-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f1b26-112">Пример 2: получение всех общих файловых ресурсов, начинающихся со строки</span><span class="sxs-lookup"><span data-stu-id="f1b26-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="f1b26-113">Эта команда получает список всех общих файловых ресурсов, имена которых начинаются с contoso.</span><span class="sxs-lookup"><span data-stu-id="f1b26-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="f1b26-114">Пример 3: получение всех общих файловых ресурсов в указанном контексте</span><span class="sxs-lookup"><span data-stu-id="f1b26-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="f1b26-115">Первая команда использует командлет **New-AzureStorageContext** для создания контекста с помощью *локального* параметра, а затем сохраняет этот объект контекста в переменной $context.</span><span class="sxs-lookup"><span data-stu-id="f1b26-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="f1b26-116">Вторая команда получает файловые ресурсы общего доступа для объекта контекста, хранящегося в $Context.</span><span class="sxs-lookup"><span data-stu-id="f1b26-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="f1b26-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1b26-117">PARAMETERS</span></span>

### <span data-ttu-id="f1b26-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1b26-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f1b26-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f1b26-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f1b26-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f1b26-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f1b26-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f1b26-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f1b26-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f1b26-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f1b26-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f1b26-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f1b26-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f1b26-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f1b26-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f1b26-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f1b26-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f1b26-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f1b26-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f1b26-127">The default value is 10.</span></span>

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

### <span data-ttu-id="f1b26-128">-Context</span><span class="sxs-lookup"><span data-stu-id="f1b26-128">-Context</span></span>
<span data-ttu-id="f1b26-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b26-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f1b26-130">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f1b26-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f1b26-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1b26-131">-Name</span></span>
<span data-ttu-id="f1b26-132">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="f1b26-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="f1b26-133">Этот командлет возвращает общую файловую единицу, указанную в этом параметре, или значение Nothing, если указано несуществующее имя общей файловой панели.</span><span class="sxs-lookup"><span data-stu-id="f1b26-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b26-134">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="f1b26-134">-Prefix</span></span>
<span data-ttu-id="f1b26-135">Указывает префикс для общих файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1b26-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="f1b26-136">Этот командлет получает файловые ресурсы, соответствующие префиксу, указанному в этом параметре, или нет общих файловых ресурсов, если не совпадает ни одного общего файла с указанным префиксом.</span><span class="sxs-lookup"><span data-stu-id="f1b26-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b26-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1b26-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f1b26-138">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b26-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f1b26-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b26-139">CommonParameters</span></span>
<span data-ttu-id="f1b26-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1b26-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b26-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b26-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b26-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1b26-142">INPUTS</span></span>

## <span data-ttu-id="f1b26-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1b26-143">OUTPUTS</span></span>

## <span data-ttu-id="f1b26-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1b26-144">NOTES</span></span>

## <span data-ttu-id="f1b26-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1b26-145">RELATED LINKS</span></span>

[<span data-ttu-id="f1b26-146">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1b26-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="f1b26-147">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1b26-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
