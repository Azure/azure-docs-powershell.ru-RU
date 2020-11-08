---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 90980ec0e6f71d57a8277abaf411f621140e7126
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066928"
---
# <span data-ttu-id="f13a9-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f13a9-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="f13a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f13a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f13a9-103">Удаление файла.</span><span class="sxs-lookup"><span data-stu-id="f13a9-103">Deletes a file.</span></span>

## <span data-ttu-id="f13a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f13a9-104">SYNTAX</span></span>

### <span data-ttu-id="f13a9-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f13a9-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13a9-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="f13a9-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13a9-107">Папка</span><span class="sxs-lookup"><span data-stu-id="f13a9-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f13a9-108">Файл</span><span class="sxs-lookup"><span data-stu-id="f13a9-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f13a9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f13a9-109">DESCRIPTION</span></span>
<span data-ttu-id="f13a9-110">Командлет **Remove-AzStorageFile** удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="f13a9-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="f13a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f13a9-111">EXAMPLES</span></span>

### <span data-ttu-id="f13a9-112">Пример 1: удаление файла из общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="f13a9-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="f13a9-113">Эта команда удаляет файл с именем ContosoFile22 из общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f13a9-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f13a9-114">Пример 2: получение файла из общей сетевой папке с помощью объекта общего доступа к файлу</span><span class="sxs-lookup"><span data-stu-id="f13a9-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="f13a9-115">Эта команда использует командлет **Get-AzStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f13a9-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f13a9-116">Текущая команда удаляет файл с именем ContosoFile22 из ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f13a9-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="f13a9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f13a9-117">PARAMETERS</span></span>

### <span data-ttu-id="f13a9-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f13a9-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f13a9-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f13a9-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f13a9-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f13a9-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f13a9-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f13a9-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f13a9-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f13a9-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f13a9-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f13a9-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f13a9-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f13a9-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f13a9-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f13a9-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f13a9-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f13a9-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f13a9-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f13a9-127">The default value is 10.</span></span>

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

### <span data-ttu-id="f13a9-128">-Context</span><span class="sxs-lookup"><span data-stu-id="f13a9-128">-Context</span></span>
<span data-ttu-id="f13a9-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f13a9-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f13a9-130">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f13a9-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f13a9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13a9-131">-DefaultProfile</span></span>
<span data-ttu-id="f13a9-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f13a9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f13a9-133">-Каталог</span><span class="sxs-lookup"><span data-stu-id="f13a9-133">-Directory</span></span>
<span data-ttu-id="f13a9-134">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="f13a9-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f13a9-135">Этот командлет удаляет файл из папки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f13a9-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a9-136">-Файл</span><span class="sxs-lookup"><span data-stu-id="f13a9-136">-File</span></span>
<span data-ttu-id="f13a9-137">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="f13a9-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="f13a9-138">Этот командлет удаляет файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f13a9-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="f13a9-139">Чтобы получить объект **CloudFile** , используйте командлет Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="f13a9-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a9-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f13a9-140">-PassThru</span></span>
<span data-ttu-id="f13a9-141">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="f13a9-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f13a9-142">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f13a9-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f13a9-143">-Path</span><span class="sxs-lookup"><span data-stu-id="f13a9-143">-Path</span></span>
<span data-ttu-id="f13a9-144">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="f13a9-144">Specifies the path of a file.</span></span>
<span data-ttu-id="f13a9-145">Этот командлет удаляет файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f13a9-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f13a9-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f13a9-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f13a9-147">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="f13a9-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f13a9-148">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="f13a9-148">-Share</span></span>
<span data-ttu-id="f13a9-149">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="f13a9-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f13a9-150">Этот командлет удаляет файл в параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="f13a9-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="f13a9-151">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="f13a9-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="f13a9-152">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="f13a9-152">This object contains the storage context.</span></span>
<span data-ttu-id="f13a9-153">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="f13a9-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a9-154">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f13a9-154">-ShareName</span></span>
<span data-ttu-id="f13a9-155">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="f13a9-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="f13a9-156">Этот командлет удаляет файл в параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="f13a9-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="f13a9-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f13a9-157">-Confirm</span></span>
<span data-ttu-id="f13a9-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f13a9-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13a9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13a9-159">-WhatIf</span></span>
<span data-ttu-id="f13a9-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f13a9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f13a9-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f13a9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13a9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13a9-162">CommonParameters</span></span>
<span data-ttu-id="f13a9-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f13a9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13a9-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f13a9-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13a9-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f13a9-165">INPUTS</span></span>

### <span data-ttu-id="f13a9-166">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f13a9-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="f13a9-167">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="f13a9-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="f13a9-168">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f13a9-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f13a9-169">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f13a9-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f13a9-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f13a9-170">OUTPUTS</span></span>

### <span data-ttu-id="f13a9-171">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f13a9-171">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="f13a9-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="f13a9-172">NOTES</span></span>

## <span data-ttu-id="f13a9-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f13a9-173">RELATED LINKS</span></span>

[<span data-ttu-id="f13a9-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f13a9-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f13a9-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f13a9-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="f13a9-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f13a9-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
