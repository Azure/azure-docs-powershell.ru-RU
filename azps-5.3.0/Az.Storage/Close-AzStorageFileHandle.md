---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420140"
---
# <span data-ttu-id="02ea2-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="02ea2-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="02ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="02ea2-103">Закрывается обработка файлов из файловой папки, каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="02ea2-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="02ea2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02ea2-104">SYNTAX</span></span>

### <span data-ttu-id="02ea2-105">ShareNameCloseAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02ea2-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ea2-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="02ea2-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ea2-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="02ea2-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ea2-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="02ea2-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ea2-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="02ea2-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ea2-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="02ea2-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02ea2-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02ea2-111">DESCRIPTION</span></span>
<span data-ttu-id="02ea2-112">Для **закрытия azStorageFileHandle** будут закрыты все файлы, хранимые в папке, каталоге или файле.</span><span class="sxs-lookup"><span data-stu-id="02ea2-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="02ea2-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02ea2-113">EXAMPLES</span></span>

### <span data-ttu-id="02ea2-114">Пример 1. Перечисляются все папки текущей учетной записи хранения, и все их обработки закроются рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="02ea2-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="02ea2-115">Эта команда содержит список всех файловых акций текущей учетной записи хранения и закроет все их обработки рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="02ea2-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="02ea2-116">Пример 2. Закройте все обработки файлов в рекурсивной папке файлов и откажите количество закрытых х обрабатываемого файла</span><span class="sxs-lookup"><span data-stu-id="02ea2-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="02ea2-117">Эта команда закрывает все файлы, хранимые в каталоге, и показывает количество закрытых файлов.</span><span class="sxs-lookup"><span data-stu-id="02ea2-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="02ea2-118">Пример 3. Закрыть все файлы, которые были открыты 1 день назад в каталоге файлов</span><span class="sxs-lookup"><span data-stu-id="02ea2-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="02ea2-119">Эта команда перечислены рекурсивно все обрабатывающие файлы в каталоге файлов, отфильтровыв их, которые были открыты 1 день назад, а затем закройте их.</span><span class="sxs-lookup"><span data-stu-id="02ea2-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="02ea2-120">Пример 4. Закроем все обрабатываемые папки в файле</span><span class="sxs-lookup"><span data-stu-id="02ea2-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="02ea2-121">Эта команда закрывает все хранимые в файле файлы.</span><span class="sxs-lookup"><span data-stu-id="02ea2-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="02ea2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02ea2-122">PARAMETERS</span></span>

### <span data-ttu-id="02ea2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ea2-123">-AsJob</span></span>
<span data-ttu-id="02ea2-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="02ea2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02ea2-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02ea2-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02ea2-126">Максимальное время выполнения каждого запроса на стороне клиента в секундах.</span><span class="sxs-lookup"><span data-stu-id="02ea2-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="02ea2-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="02ea2-127">-CloseAll</span></span>
<span data-ttu-id="02ea2-128">Принудительно закроем все файлы.</span><span class="sxs-lookup"><span data-stu-id="02ea2-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="02ea2-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02ea2-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02ea2-130">Общее количество одновременной работы с async.</span><span class="sxs-lookup"><span data-stu-id="02ea2-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="02ea2-131">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="02ea2-131">The default value is 10.</span></span>

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

### <span data-ttu-id="02ea2-132">-Контекст</span><span class="sxs-lookup"><span data-stu-id="02ea2-132">-Context</span></span>
<span data-ttu-id="02ea2-133">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="02ea2-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="02ea2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ea2-134">-DefaultProfile</span></span>
<span data-ttu-id="02ea2-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02ea2-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ea2-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="02ea2-136">-Directory</span></span>
<span data-ttu-id="02ea2-137">Объект CloudFileDirectory указал базовую папку, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="02ea2-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02ea2-138">-File</span><span class="sxs-lookup"><span data-stu-id="02ea2-138">-File</span></span>
<span data-ttu-id="02ea2-139">Объект CloudFile указал, что файл закрыт.</span><span class="sxs-lookup"><span data-stu-id="02ea2-139">CloudFile object indicated the file to close handle.</span></span>

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

### <span data-ttu-id="02ea2-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="02ea2-140">-FileHandle</span></span>
<span data-ttu-id="02ea2-141">Файл, который нужно закрыть.</span><span class="sxs-lookup"><span data-stu-id="02ea2-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="02ea2-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02ea2-142">-PassThru</span></span>
<span data-ttu-id="02ea2-143">Возвращает количество закрытых файлов.</span><span class="sxs-lookup"><span data-stu-id="02ea2-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="02ea2-144">-Path</span><span class="sxs-lookup"><span data-stu-id="02ea2-144">-Path</span></span>
<span data-ttu-id="02ea2-145">Путь к существующему файлу или каталогу.</span><span class="sxs-lookup"><span data-stu-id="02ea2-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="02ea2-146">-Рекурсивное</span><span class="sxs-lookup"><span data-stu-id="02ea2-146">-Recursive</span></span>
<span data-ttu-id="02ea2-147">Список обрабатывает рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="02ea2-147">List handles Recursively.</span></span>
<span data-ttu-id="02ea2-148">Работает только в каталоге файлов.</span><span class="sxs-lookup"><span data-stu-id="02ea2-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="02ea2-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02ea2-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02ea2-150">Время с часовой стрелкой для каждого запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="02ea2-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="02ea2-151">-Share</span><span class="sxs-lookup"><span data-stu-id="02ea2-151">-Share</span></span>
<span data-ttu-id="02ea2-152">Объект CloudFileShare указал папку, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="02ea2-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02ea2-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="02ea2-153">-ShareName</span></span>
<span data-ttu-id="02ea2-154">Имя папки, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="02ea2-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="02ea2-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02ea2-155">-Confirm</span></span>
<span data-ttu-id="02ea2-156">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="02ea2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ea2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ea2-157">-WhatIf</span></span>
<span data-ttu-id="02ea2-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ea2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ea2-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02ea2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ea2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ea2-160">CommonParameters</span></span>
<span data-ttu-id="02ea2-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ea2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ea2-162">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ea2-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ea2-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02ea2-163">INPUTS</span></span>

### <span data-ttu-id="02ea2-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="02ea2-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="02ea2-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="02ea2-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="02ea2-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="02ea2-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02ea2-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02ea2-167">OUTPUTS</span></span>

### <span data-ttu-id="02ea2-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="02ea2-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="02ea2-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02ea2-169">NOTES</span></span>

## <span data-ttu-id="02ea2-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02ea2-170">RELATED LINKS</span></span>
