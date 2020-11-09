---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315914"
---
# <span data-ttu-id="ebb1f-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ebb1f-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="ebb1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb1f-103">Закрывает дескрипторы файлов, папки или файла.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="ebb1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebb1f-104">SYNTAX</span></span>

### <span data-ttu-id="ebb1f-105">ShareNameCloseAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebb1f-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebb1f-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="ebb1f-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb1f-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="ebb1f-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb1f-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="ebb1f-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb1f-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="ebb1f-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb1f-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="ebb1f-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebb1f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-111">DESCRIPTION</span></span>
<span data-ttu-id="ebb1f-112">Командлет **Close-AzStorageFileHandle** закрывает дескрипторы файлов в общей папке, папке или файле.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="ebb1f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-113">EXAMPLES</span></span>

### <span data-ttu-id="ebb1f-114">Пример 1: выводит список всех общих папок для текущей учетной записи хранения и рекурсивно закрывает все дескрипторы файлов в общих файловых ресурсах.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="ebb1f-115">Эта команда выведет список всех общих папок для текущей учетной записи хранения и повторно закроет все дескрипторы файлов общих папок.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="ebb1f-116">Пример 2: повторное закрытие всех дескрипторов файлов в каталоге файлов и отображение счетчика закрытых дескрипторов файлов</span><span class="sxs-lookup"><span data-stu-id="ebb1f-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="ebb1f-117">Эта команда закрывает все дескрипторы файлов в каталоге файлов и отображает счетчик закрытых дескрипторов файлов.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="ebb1f-118">Пример 3: закрытие всех дескрипторов файлов, открытых на один день назад в каталоге файлов</span><span class="sxs-lookup"><span data-stu-id="ebb1f-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="ebb1f-119">Эта команда перечисляет все дескрипторы файлов в каталоге файлов рекурсивно, отфильтровывает маркеры, открытые 1 день назад, а затем закрывая их.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="ebb1f-120">Пример 4: закрытие всех дескрипторов файлов в файле</span><span class="sxs-lookup"><span data-stu-id="ebb1f-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="ebb1f-121">Эта команда закрывает все дескрипторы файлов в файле.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="ebb1f-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-122">PARAMETERS</span></span>

### <span data-ttu-id="ebb1f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebb1f-123">-AsJob</span></span>
<span data-ttu-id="ebb1f-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ebb1f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebb1f-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebb1f-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ebb1f-126">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="ebb1f-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="ebb1f-127">-CloseAll</span></span>
<span data-ttu-id="ebb1f-128">Принудительно закрывайте все дескрипторы файлов.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ebb1f-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ebb1f-130">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="ebb1f-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-131">The default value is 10.</span></span>

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

### <span data-ttu-id="ebb1f-132">-Context</span><span class="sxs-lookup"><span data-stu-id="ebb1f-132">-Context</span></span>
<span data-ttu-id="ebb1f-133">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="ebb1f-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb1f-134">-DefaultProfile</span></span>
<span data-ttu-id="ebb1f-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebb1f-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="ebb1f-136">-Directory</span></span>
<span data-ttu-id="ebb1f-137">Объект CloudFileDirectory, на котором указана базовая папка с файлами и каталогами.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-138">-Файл</span><span class="sxs-lookup"><span data-stu-id="ebb1f-138">-File</span></span>
<span data-ttu-id="ebb1f-139">Объект CloudFile, на котором указывает файл для закрытия дескриптора.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="ebb1f-140">-FileHandle</span></span>
<span data-ttu-id="ebb1f-141">Дескриптор файла, который нужно закрыть.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebb1f-142">-PassThru</span></span>
<span data-ttu-id="ebb1f-143">Возвращают количество закрытых дескрипторов файлов.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="ebb1f-144">-Path</span><span class="sxs-lookup"><span data-stu-id="ebb1f-144">-Path</span></span>
<span data-ttu-id="ebb1f-145">Путь к существующему файлу или каталогу.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="ebb1f-146">-Recursive</span></span>
<span data-ttu-id="ebb1f-147">Рекурсивные дескрипторы списка.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-147">List handles Recursively.</span></span>
<span data-ttu-id="ebb1f-148">Работает только в каталогах файлов.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ebb1f-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ebb1f-150">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="ebb1f-151">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-151">-Share</span></span>
<span data-ttu-id="ebb1f-152">Объект CloudFileShare, на котором указан общий доступ к файлам и каталогам.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-153">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="ebb1f-153">-ShareName</span></span>
<span data-ttu-id="ebb1f-154">Имя общей папки, в которой будут перечислены файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebb1f-155">-Confirm</span></span>
<span data-ttu-id="ebb1f-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebb1f-157">-WhatIf</span></span>
<span data-ttu-id="ebb1f-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebb1f-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb1f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb1f-160">CommonParameters</span></span>
<span data-ttu-id="ebb1f-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebb1f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb1f-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb1f-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb1f-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebb1f-163">INPUTS</span></span>

### <span data-ttu-id="ebb1f-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ebb1f-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="ebb1f-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ebb1f-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="ebb1f-166">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ebb1f-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ebb1f-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-167">OUTPUTS</span></span>

### <span data-ttu-id="ebb1f-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="ebb1f-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="ebb1f-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebb1f-169">NOTES</span></span>

## <span data-ttu-id="ebb1f-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebb1f-170">RELATED LINKS</span></span>
