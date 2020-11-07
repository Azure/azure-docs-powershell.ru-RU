---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732888"
---
# <span data-ttu-id="4d097-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4d097-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="4d097-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d097-102">SYNOPSIS</span></span>
<span data-ttu-id="4d097-103">Удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="4d097-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d097-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d097-104">SYNTAX</span></span>

### <span data-ttu-id="4d097-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d097-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d097-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="4d097-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d097-107">Папка</span><span class="sxs-lookup"><span data-stu-id="4d097-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d097-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d097-108">DESCRIPTION</span></span>
<span data-ttu-id="4d097-109">Командлет **Remove-AzureStorageDirectory** удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="4d097-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="4d097-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d097-110">EXAMPLES</span></span>

### <span data-ttu-id="4d097-111">Пример 1: Удаление папки</span><span class="sxs-lookup"><span data-stu-id="4d097-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4d097-112">Эта команда удаляет папку с именем ContosoWorkingFolder из общей папки с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4d097-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4d097-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d097-113">PARAMETERS</span></span>

### <span data-ttu-id="4d097-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4d097-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4d097-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4d097-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4d097-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="4d097-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4d097-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d097-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4d097-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4d097-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4d097-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4d097-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4d097-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4d097-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4d097-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="4d097-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4d097-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="4d097-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4d097-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4d097-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4d097-124">-Context</span><span class="sxs-lookup"><span data-stu-id="4d097-124">-Context</span></span>
<span data-ttu-id="4d097-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4d097-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4d097-126">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4d097-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4d097-127">-Каталог</span><span class="sxs-lookup"><span data-stu-id="4d097-127">-Directory</span></span>
<span data-ttu-id="4d097-128">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="4d097-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4d097-129">Этот командлет удаляет папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="4d097-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="4d097-130">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="4d097-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4d097-131">Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="4d097-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="4d097-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d097-132">-PassThru</span></span>
<span data-ttu-id="4d097-133">Указывает, что при успешном выполнении командлета возвращается значение $True.</span><span class="sxs-lookup"><span data-stu-id="4d097-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="4d097-134">Если указать этот параметр и, если командлет завершился сбоем из-за неприемлемого значения параметра _path_ , командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d097-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="4d097-135">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4d097-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4d097-136">-Path</span><span class="sxs-lookup"><span data-stu-id="4d097-136">-Path</span></span>
<span data-ttu-id="4d097-137">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="4d097-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="4d097-138">Если папка, в которой указан этот параметр, пуста, этот командлет удаляет эту папку.</span><span class="sxs-lookup"><span data-stu-id="4d097-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="4d097-139">Если папка не пустая, этот командлет не вносит никаких изменений и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d097-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d097-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4d097-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4d097-141">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="4d097-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4d097-142">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="4d097-142">-Share</span></span>
<span data-ttu-id="4d097-143">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="4d097-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4d097-144">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4d097-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="4d097-145">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="4d097-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4d097-146">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="4d097-146">This object contains the storage context.</span></span>
<span data-ttu-id="4d097-147">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="4d097-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4d097-148">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="4d097-148">-ShareName</span></span>
<span data-ttu-id="4d097-149">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="4d097-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="4d097-150">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4d097-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d097-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d097-151">-Confirm</span></span>
<span data-ttu-id="4d097-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d097-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d097-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d097-153">-WhatIf</span></span>
<span data-ttu-id="4d097-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d097-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d097-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d097-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d097-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d097-156">CommonParameters</span></span>
<span data-ttu-id="4d097-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d097-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d097-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d097-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d097-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d097-159">INPUTS</span></span>

### <span data-ttu-id="4d097-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4d097-160">IStorageContext</span></span>

<span data-ttu-id="4d097-161">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4d097-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4d097-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4d097-162">CloudFileDirectory</span></span>

<span data-ttu-id="4d097-163">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4d097-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="4d097-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4d097-164">CloudFileShare</span></span>

<span data-ttu-id="4d097-165">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4d097-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="4d097-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d097-166">OUTPUTS</span></span>

## <span data-ttu-id="4d097-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d097-167">NOTES</span></span>

## <span data-ttu-id="4d097-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d097-168">RELATED LINKS</span></span>

[<span data-ttu-id="4d097-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4d097-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4d097-170">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4d097-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4d097-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4d097-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
