---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245800"
---
# <span data-ttu-id="f3efd-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f3efd-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="f3efd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3efd-102">SYNOPSIS</span></span>
<span data-ttu-id="f3efd-103">Удаление общей папке.</span><span class="sxs-lookup"><span data-stu-id="f3efd-103">Deletes a file share.</span></span>

## <span data-ttu-id="f3efd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3efd-104">SYNTAX</span></span>

### <span data-ttu-id="f3efd-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3efd-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3efd-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="f3efd-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3efd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3efd-107">DESCRIPTION</span></span>
<span data-ttu-id="f3efd-108">Командлет **Remove-AzStorageShare** удаляет общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="f3efd-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="f3efd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3efd-109">EXAMPLES</span></span>

### <span data-ttu-id="f3efd-110">Пример 1: Удаление общей сетевой папке</span><span class="sxs-lookup"><span data-stu-id="f3efd-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="f3efd-111">Эта команда удаляет общую файловую панель с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f3efd-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f3efd-112">Пример 2: Удаление общей файловой и всех ее снимков</span><span class="sxs-lookup"><span data-stu-id="f3efd-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="f3efd-113">Эта команда удаляет общую папке с именем ContosoShare06 и всех ее снимков.</span><span class="sxs-lookup"><span data-stu-id="f3efd-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="f3efd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3efd-114">PARAMETERS</span></span>

### <span data-ttu-id="f3efd-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f3efd-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f3efd-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f3efd-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f3efd-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f3efd-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f3efd-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f3efd-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f3efd-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f3efd-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f3efd-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f3efd-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f3efd-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f3efd-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f3efd-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f3efd-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f3efd-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f3efd-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f3efd-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f3efd-124">The default value is 10.</span></span>

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

### <span data-ttu-id="f3efd-125">-Context</span><span class="sxs-lookup"><span data-stu-id="f3efd-125">-Context</span></span>
<span data-ttu-id="f3efd-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f3efd-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f3efd-127">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f3efd-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3efd-128">-DefaultProfile</span></span>
<span data-ttu-id="f3efd-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3efd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3efd-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f3efd-130">-Force</span></span>
<span data-ttu-id="f3efd-131">Принудительное удаление общего доступа ко всем его снимкам и всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="f3efd-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="f3efd-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="f3efd-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="f3efd-133">Удаление общего доступа к файлам со всеми моментальными снимками</span><span class="sxs-lookup"><span data-stu-id="f3efd-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="f3efd-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3efd-134">-Name</span></span>
<span data-ttu-id="f3efd-135">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="f3efd-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="f3efd-136">Этот командлет удаляет общую файловую панель, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="f3efd-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3efd-137">-PassThru</span></span>
<span data-ttu-id="f3efd-138">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="f3efd-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f3efd-139">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f3efd-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f3efd-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f3efd-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f3efd-141">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="f3efd-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f3efd-142">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="f3efd-142">-Share</span></span>
<span data-ttu-id="f3efd-143">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="f3efd-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f3efd-144">Этот командлет удаляет объект, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f3efd-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="f3efd-145">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="f3efd-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="f3efd-146">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="f3efd-146">This object contains the storage context.</span></span>
<span data-ttu-id="f3efd-147">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="f3efd-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3efd-148">-Confirm</span></span>
<span data-ttu-id="f3efd-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3efd-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3efd-150">-WhatIf</span></span>
<span data-ttu-id="f3efd-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3efd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3efd-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3efd-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3efd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3efd-153">CommonParameters</span></span>
<span data-ttu-id="f3efd-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3efd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3efd-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3efd-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3efd-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3efd-156">INPUTS</span></span>

### <span data-ttu-id="f3efd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f3efd-157">System.String</span></span>

### <span data-ttu-id="f3efd-158">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f3efd-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="f3efd-159">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3efd-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f3efd-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3efd-160">OUTPUTS</span></span>

### <span data-ttu-id="f3efd-161">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="f3efd-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="f3efd-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3efd-162">NOTES</span></span>

## <span data-ttu-id="f3efd-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3efd-163">RELATED LINKS</span></span>

[<span data-ttu-id="f3efd-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f3efd-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="f3efd-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3efd-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f3efd-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f3efd-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)