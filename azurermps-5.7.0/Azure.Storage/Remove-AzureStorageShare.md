---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: c929a7e3e685fd870c57ff942262a0c5ac4a9966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559392"
---
# <span data-ttu-id="927c0-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="927c0-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="927c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="927c0-102">SYNOPSIS</span></span>
<span data-ttu-id="927c0-103">Удаление общей папке.</span><span class="sxs-lookup"><span data-stu-id="927c0-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="927c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="927c0-104">SYNTAX</span></span>

### <span data-ttu-id="927c0-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="927c0-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927c0-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="927c0-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927c0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="927c0-107">DESCRIPTION</span></span>
<span data-ttu-id="927c0-108">Командлет **Remove-AzureStorageShare** удаляет общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="927c0-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="927c0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="927c0-109">EXAMPLES</span></span>

### <span data-ttu-id="927c0-110">Пример 1: Удаление общей сетевой папке</span><span class="sxs-lookup"><span data-stu-id="927c0-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="927c0-111">Эта команда удаляет общую файловую панель с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="927c0-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="927c0-112">Пример 2: Удаление общей файловой и всех ее снимков</span><span class="sxs-lookup"><span data-stu-id="927c0-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="927c0-113">Эта команда удаляет общую папке с именем ContosoShare06 и всех ее снимков.</span><span class="sxs-lookup"><span data-stu-id="927c0-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="927c0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="927c0-114">PARAMETERS</span></span>

### <span data-ttu-id="927c0-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="927c0-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="927c0-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="927c0-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="927c0-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="927c0-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="927c0-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="927c0-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="927c0-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="927c0-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="927c0-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="927c0-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="927c0-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="927c0-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="927c0-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="927c0-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="927c0-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="927c0-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="927c0-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="927c0-124">The default value is 10.</span></span>

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

### <span data-ttu-id="927c0-125">-Context</span><span class="sxs-lookup"><span data-stu-id="927c0-125">-Context</span></span>
<span data-ttu-id="927c0-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="927c0-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="927c0-127">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="927c0-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="927c0-128">-Force</span><span class="sxs-lookup"><span data-stu-id="927c0-128">-Force</span></span>
<span data-ttu-id="927c0-129">Принудительное удаление общего доступа ко всем его снимкам и всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="927c0-129">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="927c0-130">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="927c0-130">-IncludeAllSnapshot</span></span>
<span data-ttu-id="927c0-131">Удаление общего доступа к файлам со всеми моментальными снимками</span><span class="sxs-lookup"><span data-stu-id="927c0-131">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="927c0-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="927c0-132">-Name</span></span>
<span data-ttu-id="927c0-133">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="927c0-133">Specifies the name of the file share.</span></span>
<span data-ttu-id="927c0-134">Этот командлет удаляет общую файловую панель, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="927c0-134">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="927c0-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="927c0-135">-PassThru</span></span>
<span data-ttu-id="927c0-136">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="927c0-136">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="927c0-137">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="927c0-137">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="927c0-138">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="927c0-138">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="927c0-139">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="927c0-139">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="927c0-140">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="927c0-140">-Share</span></span>
<span data-ttu-id="927c0-141">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="927c0-141">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="927c0-142">Этот командлет удаляет объект, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="927c0-142">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="927c0-143">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="927c0-143">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="927c0-144">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="927c0-144">This object contains the storage context.</span></span>
<span data-ttu-id="927c0-145">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="927c0-145">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="927c0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="927c0-146">-Confirm</span></span>
<span data-ttu-id="927c0-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="927c0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927c0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927c0-148">-WhatIf</span></span>
<span data-ttu-id="927c0-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="927c0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927c0-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="927c0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927c0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927c0-151">CommonParameters</span></span>
<span data-ttu-id="927c0-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="927c0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927c0-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927c0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927c0-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="927c0-154">INPUTS</span></span>

### <span data-ttu-id="927c0-155">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="927c0-155">IStorageContext</span></span>

<span data-ttu-id="927c0-156">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="927c0-156">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="927c0-157">Подстрок</span><span class="sxs-lookup"><span data-stu-id="927c0-157">String</span></span>

<span data-ttu-id="927c0-158">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="927c0-158">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="927c0-159">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="927c0-159">CloudFileShare</span></span>

<span data-ttu-id="927c0-160">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="927c0-160">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="927c0-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="927c0-161">OUTPUTS</span></span>

## <span data-ttu-id="927c0-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="927c0-162">NOTES</span></span>

## <span data-ttu-id="927c0-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="927c0-163">RELATED LINKS</span></span>

[<span data-ttu-id="927c0-164">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="927c0-164">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="927c0-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="927c0-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="927c0-166">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="927c0-166">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
