---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555911"
---
# <span data-ttu-id="a8d0a-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a8d0a-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="a8d0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d0a-103">Создание каталога.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-103">Creates a directory.</span></span>

## <span data-ttu-id="a8d0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8d0a-104">SYNTAX</span></span>

### <span data-ttu-id="a8d0a-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8d0a-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8d0a-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a8d0a-107">Папка</span><span class="sxs-lookup"><span data-stu-id="a8d0a-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a8d0a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-108">DESCRIPTION</span></span>
<span data-ttu-id="a8d0a-109">Командлет **New-AzureStorageDirectory** создает каталог.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="a8d0a-110">Этот командлет возвращает объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="a8d0a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-111">EXAMPLES</span></span>

### <span data-ttu-id="a8d0a-112">Пример 1: создание папки в общей папке</span><span class="sxs-lookup"><span data-stu-id="a8d0a-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a8d0a-113">Эта команда создает папку с именем ContosoWorkingFolder в общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a8d0a-114">Пример 2: создание папки в общей папке, указанной в объекте "общий доступ к файлам"</span><span class="sxs-lookup"><span data-stu-id="a8d0a-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a8d0a-115">Эта команда использует командлет **Get-AzureStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем передает его в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8d0a-116">Текущий командлет создает папку с именем ContosoWorkingFolder в ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="a8d0a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-117">PARAMETERS</span></span>

### <span data-ttu-id="a8d0a-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8d0a-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a8d0a-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a8d0a-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a8d0a-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a8d0a-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a8d0a-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a8d0a-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a8d0a-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a8d0a-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a8d0a-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a8d0a-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-127">The default value is 10.</span></span>

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

### <span data-ttu-id="a8d0a-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a8d0a-128">-Context</span></span>
<span data-ttu-id="a8d0a-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a8d0a-130">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a8d0a-131">-Каталог</span><span class="sxs-lookup"><span data-stu-id="a8d0a-131">-Directory</span></span>
<span data-ttu-id="a8d0a-132">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a8d0a-133">Этот командлет создает папку в том месте, где указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="a8d0a-134">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="a8d0a-135">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="a8d0a-136">-Path</span><span class="sxs-lookup"><span data-stu-id="a8d0a-136">-Path</span></span>
<span data-ttu-id="a8d0a-137">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="a8d0a-138">Этот командлет создает папку для пути, который указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a8d0a-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8d0a-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a8d0a-140">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a8d0a-141">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-141">-Share</span></span>
<span data-ttu-id="a8d0a-142">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a8d0a-143">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="a8d0a-144">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a8d0a-145">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-145">This object contains the storage context.</span></span>
<span data-ttu-id="a8d0a-146">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a8d0a-147">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="a8d0a-147">-ShareName</span></span>
<span data-ttu-id="a8d0a-148">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="a8d0a-149">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8d0a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d0a-150">CommonParameters</span></span>
<span data-ttu-id="a8d0a-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8d0a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d0a-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d0a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d0a-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8d0a-153">INPUTS</span></span>

## <span data-ttu-id="a8d0a-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-154">OUTPUTS</span></span>

## <span data-ttu-id="a8d0a-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8d0a-155">NOTES</span></span>

## <span data-ttu-id="a8d0a-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8d0a-156">RELATED LINKS</span></span>

[<span data-ttu-id="a8d0a-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="a8d0a-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="a8d0a-158">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8d0a-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a8d0a-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8d0a-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a8d0a-160">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a8d0a-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="a8d0a-161">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a8d0a-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
