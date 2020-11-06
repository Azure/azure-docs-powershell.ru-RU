---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: bc83da1cd177585b76d68eb0b55cdd15120ff22e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565074"
---
# <span data-ttu-id="c0c14-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c0c14-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="c0c14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0c14-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c14-103">Создание каталога.</span><span class="sxs-lookup"><span data-stu-id="c0c14-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0c14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0c14-104">SYNTAX</span></span>

### <span data-ttu-id="c0c14-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0c14-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c14-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="c0c14-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c0c14-107">Папка</span><span class="sxs-lookup"><span data-stu-id="c0c14-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c0c14-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0c14-108">DESCRIPTION</span></span>
<span data-ttu-id="c0c14-109">Командлет **New-AzureStorageDirectory** создает каталог.</span><span class="sxs-lookup"><span data-stu-id="c0c14-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="c0c14-110">Этот командлет возвращает объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c0c14-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="c0c14-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0c14-111">EXAMPLES</span></span>

### <span data-ttu-id="c0c14-112">Пример 1: создание папки в общей папке</span><span class="sxs-lookup"><span data-stu-id="c0c14-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c0c14-113">Эта команда создает папку с именем ContosoWorkingFolder в общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c0c14-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c0c14-114">Пример 2: создание папки в общей папке, указанной в объекте "общий доступ к файлам"</span><span class="sxs-lookup"><span data-stu-id="c0c14-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c0c14-115">Эта команда использует командлет **Get-AzureStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем передает его в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0c14-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0c14-116">Текущий командлет создает папку с именем ContosoWorkingFolder в ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c0c14-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="c0c14-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0c14-117">PARAMETERS</span></span>

### <span data-ttu-id="c0c14-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0c14-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0c14-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c0c14-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0c14-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="c0c14-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0c14-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0c14-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0c14-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0c14-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0c14-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c0c14-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0c14-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c0c14-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0c14-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="c0c14-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0c14-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="c0c14-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0c14-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c0c14-127">The default value is 10.</span></span>

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

### <span data-ttu-id="c0c14-128">-Context</span><span class="sxs-lookup"><span data-stu-id="c0c14-128">-Context</span></span>
<span data-ttu-id="c0c14-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c14-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0c14-130">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c14-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c14-131">-Каталог</span><span class="sxs-lookup"><span data-stu-id="c0c14-131">-Directory</span></span>
<span data-ttu-id="c0c14-132">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c0c14-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c0c14-133">Этот командлет создает папку в том месте, где указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c0c14-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="c0c14-134">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="c0c14-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c0c14-135">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="c0c14-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c14-136">-Path</span><span class="sxs-lookup"><span data-stu-id="c0c14-136">-Path</span></span>
<span data-ttu-id="c0c14-137">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="c0c14-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="c0c14-138">Этот командлет создает папку для пути, который указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0c14-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c14-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0c14-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0c14-140">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="c0c14-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0c14-141">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="c0c14-141">-Share</span></span>
<span data-ttu-id="c0c14-142">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c0c14-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c0c14-143">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c0c14-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="c0c14-144">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c0c14-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="c0c14-145">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c0c14-145">This object contains the storage context.</span></span>
<span data-ttu-id="c0c14-146">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="c0c14-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c14-147">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c0c14-147">-ShareName</span></span>
<span data-ttu-id="c0c14-148">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="c0c14-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="c0c14-149">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c0c14-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c14-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c14-150">CommonParameters</span></span>
<span data-ttu-id="c0c14-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0c14-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c14-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c14-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c14-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0c14-153">INPUTS</span></span>

### <span data-ttu-id="c0c14-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0c14-154">IStorageContext</span></span>

<span data-ttu-id="c0c14-155">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0c14-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c0c14-156">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c0c14-156">CloudFileDirectory</span></span>

<span data-ttu-id="c0c14-157">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0c14-157">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="c0c14-158">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c0c14-158">String</span></span>

<span data-ttu-id="c0c14-159">Параметр "путь" принимает значение типа "String" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0c14-159">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c0c14-160">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c0c14-160">CloudFileShare</span></span>

<span data-ttu-id="c0c14-161">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0c14-161">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="c0c14-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0c14-162">OUTPUTS</span></span>

## <span data-ttu-id="c0c14-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0c14-163">NOTES</span></span>

## <span data-ttu-id="c0c14-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0c14-164">RELATED LINKS</span></span>

[<span data-ttu-id="c0c14-165">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c0c14-165">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c0c14-166">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0c14-166">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c0c14-167">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0c14-167">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c0c14-168">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c0c14-168">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="c0c14-169">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c0c14-169">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
