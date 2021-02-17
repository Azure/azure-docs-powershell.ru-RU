---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221881"
---
# <span data-ttu-id="e4019-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e4019-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="e4019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4019-102">SYNOPSIS</span></span>
<span data-ttu-id="e4019-103">В этом списке перечислены его хим обработки: папка или каталог файлов.</span><span class="sxs-lookup"><span data-stu-id="e4019-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="e4019-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4019-104">SYNTAX</span></span>

### <span data-ttu-id="e4019-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4019-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e4019-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="e4019-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e4019-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="e4019-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e4019-108">Файл</span><span class="sxs-lookup"><span data-stu-id="e4019-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e4019-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4019-109">DESCRIPTION</span></span>
<span data-ttu-id="e4019-110">В этом списке вы можете выбрать один из химпроиматоров **Get-AzStorageFileHandle.**</span><span class="sxs-lookup"><span data-stu-id="e4019-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="e4019-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4019-111">EXAMPLES</span></span>

### <span data-ttu-id="e4019-112">Пример 1. Рекурсивно перечислить все обрабатывающие файлы в папке, а затем отсортировать их по ClientIp и OpenTime</span><span class="sxs-lookup"><span data-stu-id="e4019-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="e4019-113">Эта команда содержит данные об обработке файлов в папке и сортировать выходные данные по ClientIp, а затем по OpenTime.</span><span class="sxs-lookup"><span data-stu-id="e4019-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="e4019-114">Пример 2. Рекурсивно перечислить первые 2 обработки файлов в каталоге файлов</span><span class="sxs-lookup"><span data-stu-id="e4019-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="e4019-115">В этой команде перечислены первые 2 рекурсивно обрабатываемого файла в каталоге файлов.</span><span class="sxs-lookup"><span data-stu-id="e4019-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="e4019-116">Пример 3. Список 3-го по шестой обработки файла</span><span class="sxs-lookup"><span data-stu-id="e4019-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="e4019-117">Эта команда со списком 3-го по шестой по счету в файле.</span><span class="sxs-lookup"><span data-stu-id="e4019-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="e4019-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4019-118">PARAMETERS</span></span>

### <span data-ttu-id="e4019-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e4019-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e4019-120">Максимальное время выполнения каждого запроса на стороне клиента в секундах.</span><span class="sxs-lookup"><span data-stu-id="e4019-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="e4019-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e4019-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e4019-122">Общий объем одновременной работы с async.</span><span class="sxs-lookup"><span data-stu-id="e4019-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="e4019-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e4019-123">The default value is 10.</span></span>

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

### <span data-ttu-id="e4019-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e4019-124">-Context</span></span>
<span data-ttu-id="e4019-125">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="e4019-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e4019-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4019-126">-DefaultProfile</span></span>
<span data-ttu-id="e4019-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4019-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4019-128">-Каталог</span><span class="sxs-lookup"><span data-stu-id="e4019-128">-Directory</span></span>
<span data-ttu-id="e4019-129">Объект CloudFileDirectory указал базовую папку, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="e4019-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="e4019-130">-File</span><span class="sxs-lookup"><span data-stu-id="e4019-130">-File</span></span>
<span data-ttu-id="e4019-131">Объект CloudFile указал файл в списке "Обработка файлов".</span><span class="sxs-lookup"><span data-stu-id="e4019-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4019-132">-Path</span><span class="sxs-lookup"><span data-stu-id="e4019-132">-Path</span></span>
<span data-ttu-id="e4019-133">Путь к существующему файлу или каталогу.</span><span class="sxs-lookup"><span data-stu-id="e4019-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4019-134">-Рекурсивное</span><span class="sxs-lookup"><span data-stu-id="e4019-134">-Recursive</span></span>
<span data-ttu-id="e4019-135">Список обрабатывает рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="e4019-135">List handles Recursively.</span></span>
<span data-ttu-id="e4019-136">Работает только в каталоге файлов.</span><span class="sxs-lookup"><span data-stu-id="e4019-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="e4019-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e4019-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e4019-138">Время с часовой стрелкой для каждого запроса на сервере.</span><span class="sxs-lookup"><span data-stu-id="e4019-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="e4019-139">-Share</span><span class="sxs-lookup"><span data-stu-id="e4019-139">-Share</span></span>
<span data-ttu-id="e4019-140">Объект CloudFileShare указал папку, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="e4019-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="e4019-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e4019-141">-ShareName</span></span>
<span data-ttu-id="e4019-142">Имя папки, в которой будут указаны файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="e4019-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="e4019-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e4019-143">-IncludeTotalCount</span></span>
<span data-ttu-id="e4019-144">Отчет о количестве объектов в наборе данных (integer), за которым следуют объекты.</span><span class="sxs-lookup"><span data-stu-id="e4019-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="e4019-145">Если не удается определить общее количество, возвращается "Неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="e4019-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="e4019-146">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="e4019-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e4019-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="e4019-147">-Skip</span></span>
<span data-ttu-id="e4019-148">Игнорирует первые "n" объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="e4019-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4019-149">-First</span><span class="sxs-lookup"><span data-stu-id="e4019-149">-First</span></span>
<span data-ttu-id="e4019-150">Возвращает только первые "n" объектов.</span><span class="sxs-lookup"><span data-stu-id="e4019-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4019-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4019-151">CommonParameters</span></span>
<span data-ttu-id="e4019-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4019-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4019-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4019-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4019-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4019-154">INPUTS</span></span>

### <span data-ttu-id="e4019-155">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e4019-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e4019-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e4019-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e4019-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4019-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e4019-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4019-158">OUTPUTS</span></span>

### <span data-ttu-id="e4019-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="e4019-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="e4019-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4019-160">NOTES</span></span>

## <span data-ttu-id="e4019-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4019-161">RELATED LINKS</span></span>
