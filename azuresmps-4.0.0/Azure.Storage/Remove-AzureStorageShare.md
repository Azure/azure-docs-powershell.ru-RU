---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555780"
---
# <span data-ttu-id="fb82b-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb82b-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="fb82b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb82b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb82b-103">Удаление общей папке.</span><span class="sxs-lookup"><span data-stu-id="fb82b-103">Deletes a file share.</span></span>

## <span data-ttu-id="fb82b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb82b-104">SYNTAX</span></span>

### <span data-ttu-id="fb82b-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb82b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb82b-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="fb82b-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb82b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb82b-107">DESCRIPTION</span></span>
<span data-ttu-id="fb82b-108">Командлет **Remove-AzureStorageShare** удаляет общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="fb82b-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="fb82b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb82b-109">EXAMPLES</span></span>

### <span data-ttu-id="fb82b-110">Пример 1: Удаление общей сетевой папке</span><span class="sxs-lookup"><span data-stu-id="fb82b-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="fb82b-111">Эта команда удаляет общую файловую панель с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fb82b-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="fb82b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb82b-112">PARAMETERS</span></span>

### <span data-ttu-id="fb82b-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fb82b-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fb82b-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="fb82b-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fb82b-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="fb82b-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fb82b-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fb82b-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fb82b-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fb82b-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fb82b-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fb82b-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fb82b-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fb82b-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fb82b-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="fb82b-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fb82b-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="fb82b-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fb82b-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="fb82b-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fb82b-123">-Context</span><span class="sxs-lookup"><span data-stu-id="fb82b-123">-Context</span></span>
<span data-ttu-id="fb82b-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fb82b-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fb82b-125">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="fb82b-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fb82b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="fb82b-126">-Force</span></span>
<span data-ttu-id="fb82b-127">Принудительное удаление общего доступа и всего содержимого</span><span class="sxs-lookup"><span data-stu-id="fb82b-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="fb82b-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb82b-128">-Name</span></span>
<span data-ttu-id="fb82b-129">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="fb82b-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="fb82b-130">Этот командлет удаляет общую файловую панель, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="fb82b-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb82b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb82b-131">-PassThru</span></span>
<span data-ttu-id="fb82b-132">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="fb82b-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fb82b-133">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fb82b-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fb82b-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fb82b-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fb82b-135">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="fb82b-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fb82b-136">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="fb82b-136">-Share</span></span>
<span data-ttu-id="fb82b-137">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="fb82b-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fb82b-138">Этот командлет удаляет объект, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fb82b-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="fb82b-139">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="fb82b-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="fb82b-140">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb82b-140">This object contains the storage context.</span></span>
<span data-ttu-id="fb82b-141">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="fb82b-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fb82b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb82b-142">-Confirm</span></span>
<span data-ttu-id="fb82b-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb82b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb82b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb82b-144">-WhatIf</span></span>
<span data-ttu-id="fb82b-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb82b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb82b-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb82b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb82b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb82b-147">CommonParameters</span></span>
<span data-ttu-id="fb82b-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb82b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb82b-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb82b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb82b-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb82b-150">INPUTS</span></span>

## <span data-ttu-id="fb82b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb82b-151">OUTPUTS</span></span>

## <span data-ttu-id="fb82b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb82b-152">NOTES</span></span>

## <span data-ttu-id="fb82b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb82b-153">RELATED LINKS</span></span>

[<span data-ttu-id="fb82b-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb82b-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="fb82b-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb82b-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fb82b-156">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb82b-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
