---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 9055f447093a0e10242824e1e2381523e0b0e81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567034"
---
# <span data-ttu-id="50b62-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="50b62-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="50b62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50b62-102">SYNOPSIS</span></span>
<span data-ttu-id="50b62-103">Удаление файла.</span><span class="sxs-lookup"><span data-stu-id="50b62-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50b62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50b62-104">SYNTAX</span></span>

### <span data-ttu-id="50b62-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50b62-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b62-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="50b62-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b62-107">Папка</span><span class="sxs-lookup"><span data-stu-id="50b62-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b62-108">Файл</span><span class="sxs-lookup"><span data-stu-id="50b62-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50b62-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50b62-109">DESCRIPTION</span></span>
<span data-ttu-id="50b62-110">Командлет **Remove-AzureStorageFile** удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="50b62-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="50b62-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50b62-111">EXAMPLES</span></span>

### <span data-ttu-id="50b62-112">Пример 1: удаление файла из общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="50b62-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="50b62-113">Эта команда удаляет файл с именем ContosoFile22 из общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="50b62-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="50b62-114">Пример 2: получение файла из общей сетевой папке с помощью объекта общего доступа к файлу</span><span class="sxs-lookup"><span data-stu-id="50b62-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="50b62-115">Эта команда использует командлет **Get-AzureStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="50b62-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50b62-116">Текущая команда удаляет файл с именем ContosoFile22 из ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="50b62-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="50b62-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50b62-117">PARAMETERS</span></span>

### <span data-ttu-id="50b62-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="50b62-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="50b62-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="50b62-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="50b62-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="50b62-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="50b62-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="50b62-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="50b62-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="50b62-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="50b62-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="50b62-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="50b62-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="50b62-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="50b62-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="50b62-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="50b62-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="50b62-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="50b62-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="50b62-127">The default value is 10.</span></span>

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

### <span data-ttu-id="50b62-128">-Context</span><span class="sxs-lookup"><span data-stu-id="50b62-128">-Context</span></span>
<span data-ttu-id="50b62-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50b62-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="50b62-130">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="50b62-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="50b62-131">-Каталог</span><span class="sxs-lookup"><span data-stu-id="50b62-131">-Directory</span></span>
<span data-ttu-id="50b62-132">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="50b62-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="50b62-133">Этот командлет удаляет файл из папки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="50b62-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="50b62-134">-Файл</span><span class="sxs-lookup"><span data-stu-id="50b62-134">-File</span></span>
<span data-ttu-id="50b62-135">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="50b62-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="50b62-136">Этот командлет удаляет файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="50b62-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="50b62-137">Чтобы получить объект **CloudFile** , используйте командлет Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="50b62-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50b62-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50b62-138">-PassThru</span></span>
<span data-ttu-id="50b62-139">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="50b62-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="50b62-140">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="50b62-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="50b62-141">-Path</span><span class="sxs-lookup"><span data-stu-id="50b62-141">-Path</span></span>
<span data-ttu-id="50b62-142">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="50b62-142">Specifies the path of a file.</span></span>
<span data-ttu-id="50b62-143">Этот командлет удаляет файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="50b62-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50b62-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="50b62-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="50b62-145">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="50b62-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="50b62-146">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="50b62-146">-Share</span></span>
<span data-ttu-id="50b62-147">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="50b62-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="50b62-148">Этот командлет удаляет файл в параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="50b62-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="50b62-149">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="50b62-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="50b62-150">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="50b62-150">This object contains the storage context.</span></span>
<span data-ttu-id="50b62-151">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="50b62-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="50b62-152">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="50b62-152">-ShareName</span></span>
<span data-ttu-id="50b62-153">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="50b62-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="50b62-154">Этот командлет удаляет файл в параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="50b62-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="50b62-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50b62-155">-Confirm</span></span>
<span data-ttu-id="50b62-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50b62-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b62-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b62-157">-WhatIf</span></span>
<span data-ttu-id="50b62-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50b62-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50b62-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50b62-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b62-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b62-160">CommonParameters</span></span>
<span data-ttu-id="50b62-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50b62-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b62-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b62-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b62-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50b62-163">INPUTS</span></span>

### <span data-ttu-id="50b62-164">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="50b62-164">IStorageContext</span></span>

<span data-ttu-id="50b62-165">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="50b62-165">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="50b62-166">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="50b62-166">CloudFileDirectory</span></span>

<span data-ttu-id="50b62-167">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="50b62-167">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="50b62-168">CloudFile</span><span class="sxs-lookup"><span data-stu-id="50b62-168">CloudFile</span></span>

<span data-ttu-id="50b62-169">Параметр "файл" принимает значение типа "CloudFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="50b62-169">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="50b62-170">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="50b62-170">CloudFileShare</span></span>

<span data-ttu-id="50b62-171">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="50b62-171">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="50b62-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50b62-172">OUTPUTS</span></span>

## <span data-ttu-id="50b62-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="50b62-173">NOTES</span></span>

## <span data-ttu-id="50b62-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50b62-174">RELATED LINKS</span></span>

[<span data-ttu-id="50b62-175">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="50b62-175">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="50b62-176">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="50b62-176">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="50b62-177">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="50b62-177">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
