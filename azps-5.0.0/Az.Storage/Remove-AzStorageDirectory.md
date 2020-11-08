---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247986"
---
# <span data-ttu-id="dd2c2-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="dd2c2-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="dd2c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2c2-103">Удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-103">Deletes a directory.</span></span>

## <span data-ttu-id="dd2c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd2c2-104">SYNTAX</span></span>

### <span data-ttu-id="dd2c2-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd2c2-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2c2-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2c2-107">Папка</span><span class="sxs-lookup"><span data-stu-id="dd2c2-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd2c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-108">DESCRIPTION</span></span>
<span data-ttu-id="dd2c2-109">Командлет **Remove-AzStorageDirectory** удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="dd2c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2c2-111">Пример 1: Удаление папки</span><span class="sxs-lookup"><span data-stu-id="dd2c2-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="dd2c2-112">Эта команда удаляет папку с именем ContosoWorkingFolder из общей папки с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="dd2c2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="dd2c2-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dd2c2-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dd2c2-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dd2c2-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dd2c2-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dd2c2-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dd2c2-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dd2c2-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dd2c2-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dd2c2-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dd2c2-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dd2c2-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-123">The default value is 10.</span></span>

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

### <span data-ttu-id="dd2c2-124">-Context</span><span class="sxs-lookup"><span data-stu-id="dd2c2-124">-Context</span></span>
<span data-ttu-id="dd2c2-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dd2c2-126">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="dd2c2-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dd2c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2c2-127">-DefaultProfile</span></span>
<span data-ttu-id="dd2c2-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2c2-129">-Каталог</span><span class="sxs-lookup"><span data-stu-id="dd2c2-129">-Directory</span></span>
<span data-ttu-id="dd2c2-130">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="dd2c2-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="dd2c2-131">Этот командлет удаляет папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="dd2c2-132">Чтобы получить каталог, используйте командлет New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="dd2c2-133">Вы также можете использовать командлет **Get-AzStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2c2-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2c2-134">-PassThru</span></span>
<span data-ttu-id="dd2c2-135">Указывает, что при успешном выполнении командлета возвращается значение $True.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="dd2c2-136">Если указать этот параметр и, если командлет завершился сбоем из-за неприемлемого значения параметра _path_ , командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="dd2c2-137">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dd2c2-138">-Path</span><span class="sxs-lookup"><span data-stu-id="dd2c2-138">-Path</span></span>
<span data-ttu-id="dd2c2-139">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="dd2c2-140">Если папка, в которой указан этот параметр, пуста, этот командлет удаляет эту папку.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="dd2c2-141">Если папка не пустая, этот командлет не вносит никаких изменений и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2c2-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dd2c2-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dd2c2-143">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dd2c2-144">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-144">-Share</span></span>
<span data-ttu-id="dd2c2-145">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="dd2c2-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dd2c2-146">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="dd2c2-147">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="dd2c2-148">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-148">This object contains the storage context.</span></span>
<span data-ttu-id="dd2c2-149">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="dd2c2-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="dd2c2-150">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="dd2c2-150">-ShareName</span></span>
<span data-ttu-id="dd2c2-151">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="dd2c2-152">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2c2-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd2c2-153">-Confirm</span></span>
<span data-ttu-id="dd2c2-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2c2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2c2-155">-WhatIf</span></span>
<span data-ttu-id="dd2c2-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2c2-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2c2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2c2-158">CommonParameters</span></span>
<span data-ttu-id="dd2c2-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd2c2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2c2-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2c2-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2c2-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd2c2-161">INPUTS</span></span>

### <span data-ttu-id="dd2c2-162">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="dd2c2-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="dd2c2-163">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="dd2c2-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="dd2c2-164">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2c2-164">System.String</span></span>

### <span data-ttu-id="dd2c2-165">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd2c2-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd2c2-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-166">OUTPUTS</span></span>

### <span data-ttu-id="dd2c2-167">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="dd2c2-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="dd2c2-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd2c2-168">NOTES</span></span>

## <span data-ttu-id="dd2c2-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd2c2-169">RELATED LINKS</span></span>

[<span data-ttu-id="dd2c2-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd2c2-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="dd2c2-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd2c2-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="dd2c2-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="dd2c2-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
