---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558667"
---
# <span data-ttu-id="bbc9f-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bbc9f-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="bbc9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc9f-103">Удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbc9f-104">SYNTAX</span></span>

### <span data-ttu-id="bbc9f-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbc9f-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbc9f-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbc9f-107">Папка</span><span class="sxs-lookup"><span data-stu-id="bbc9f-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbc9f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-108">DESCRIPTION</span></span>
<span data-ttu-id="bbc9f-109">Командлет **Remove-AzureStorageDirectory** удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="bbc9f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-110">EXAMPLES</span></span>

### <span data-ttu-id="bbc9f-111">Пример 1: Удаление папки</span><span class="sxs-lookup"><span data-stu-id="bbc9f-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="bbc9f-112">Эта команда удаляет папку с именем ContosoWorkingFolder из общей папки с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="bbc9f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-113">PARAMETERS</span></span>

### <span data-ttu-id="bbc9f-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbc9f-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bbc9f-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bbc9f-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bbc9f-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bbc9f-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bbc9f-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bbc9f-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bbc9f-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bbc9f-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bbc9f-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bbc9f-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-123">The default value is 10.</span></span>

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

### <span data-ttu-id="bbc9f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="bbc9f-124">-Context</span></span>
<span data-ttu-id="bbc9f-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bbc9f-126">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc9f-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bbc9f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc9f-127">-DefaultProfile</span></span>
<span data-ttu-id="bbc9f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc9f-129">-Каталог</span><span class="sxs-lookup"><span data-stu-id="bbc9f-129">-Directory</span></span>
<span data-ttu-id="bbc9f-130">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="bbc9f-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bbc9f-131">Этот командлет удаляет папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="bbc9f-132">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bbc9f-133">Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc9f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbc9f-134">-PassThru</span></span>
<span data-ttu-id="bbc9f-135">Указывает, что при успешном выполнении командлета возвращается значение $True.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="bbc9f-136">Если указать этот параметр и, если командлет завершился сбоем из-за неприемлемого значения параметра _path_ , командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="bbc9f-137">Если этот параметр не указан, этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bbc9f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="bbc9f-138">-Path</span></span>
<span data-ttu-id="bbc9f-139">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="bbc9f-140">Если папка, в которой указан этот параметр, пуста, этот командлет удаляет эту папку.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="bbc9f-141">Если папка не пустая, этот командлет не вносит никаких изменений и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="bbc9f-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbc9f-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bbc9f-143">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bbc9f-144">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-144">-Share</span></span>
<span data-ttu-id="bbc9f-145">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="bbc9f-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bbc9f-146">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="bbc9f-147">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="bbc9f-148">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-148">This object contains the storage context.</span></span>
<span data-ttu-id="bbc9f-149">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="bbc9f-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc9f-150">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="bbc9f-150">-ShareName</span></span>
<span data-ttu-id="bbc9f-151">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="bbc9f-152">Этот командлет удаляет папку в общей папке, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbc9f-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbc9f-153">-Confirm</span></span>
<span data-ttu-id="bbc9f-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc9f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc9f-155">-WhatIf</span></span>
<span data-ttu-id="bbc9f-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc9f-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc9f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc9f-158">CommonParameters</span></span>
<span data-ttu-id="bbc9f-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbc9f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc9f-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc9f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc9f-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbc9f-161">INPUTS</span></span>

### <span data-ttu-id="bbc9f-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bbc9f-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="bbc9f-163">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbc9f-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="bbc9f-164">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="bbc9f-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="bbc9f-165">Параметры: Каталог (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbc9f-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="bbc9f-166">System. String</span><span class="sxs-lookup"><span data-stu-id="bbc9f-166">System.String</span></span>

### <span data-ttu-id="bbc9f-167">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbc9f-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbc9f-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-168">OUTPUTS</span></span>

### <span data-ttu-id="bbc9f-169">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="bbc9f-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="bbc9f-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbc9f-170">NOTES</span></span>

## <span data-ttu-id="bbc9f-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbc9f-171">RELATED LINKS</span></span>

[<span data-ttu-id="bbc9f-172">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbc9f-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="bbc9f-173">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbc9f-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bbc9f-174">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bbc9f-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
