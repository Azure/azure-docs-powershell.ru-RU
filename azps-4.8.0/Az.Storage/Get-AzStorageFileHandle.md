---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236550"
---
# <span data-ttu-id="2c329-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2c329-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="2c329-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c329-102">SYNOPSIS</span></span>
<span data-ttu-id="2c329-103">Выводит список дескрипторов файлов общего доступа, каталогов файлов и файлов.</span><span class="sxs-lookup"><span data-stu-id="2c329-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="2c329-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c329-104">SYNTAX</span></span>

### <span data-ttu-id="2c329-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c329-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2c329-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="2c329-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2c329-107">Папка</span><span class="sxs-lookup"><span data-stu-id="2c329-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2c329-108">Файл</span><span class="sxs-lookup"><span data-stu-id="2c329-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="2c329-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c329-109">DESCRIPTION</span></span>
<span data-ttu-id="2c329-110">Командлет **Get-AzStorageFileHandle** содержит список файлов, которые хранятся в общей папке, папке или файле.</span><span class="sxs-lookup"><span data-stu-id="2c329-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="2c329-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c329-111">EXAMPLES</span></span>

### <span data-ttu-id="2c329-112">Пример 1: рекурсивный список всех дескрипторов файлов в общей папке и сортировка по ClientIp и OpenTime</span><span class="sxs-lookup"><span data-stu-id="2c329-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
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

<span data-ttu-id="2c329-113">Эта команда выводит список дескрипторов файлов в общей папке и сортирует вывод по ClientIp, а затем по OpenTime.</span><span class="sxs-lookup"><span data-stu-id="2c329-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="2c329-114">Пример 2: рекурсивный список первых двух дескрипторов файлов в каталоге файлов</span><span class="sxs-lookup"><span data-stu-id="2c329-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="2c329-115">Эта команда перечисляет первые 2 дескриптора файлов в каталоге файлов рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="2c329-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="2c329-116">Пример 3: список 3-го для обработки файла</span><span class="sxs-lookup"><span data-stu-id="2c329-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="2c329-117">Эта команда выводит список 3-го файла для обработки файла.</span><span class="sxs-lookup"><span data-stu-id="2c329-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="2c329-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c329-118">PARAMETERS</span></span>

### <span data-ttu-id="2c329-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c329-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2c329-120">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="2c329-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="2c329-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c329-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c329-122">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="2c329-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="2c329-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="2c329-123">The default value is 10.</span></span>

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

### <span data-ttu-id="2c329-124">-Context</span><span class="sxs-lookup"><span data-stu-id="2c329-124">-Context</span></span>
<span data-ttu-id="2c329-125">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2c329-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2c329-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c329-126">-DefaultProfile</span></span>
<span data-ttu-id="2c329-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c329-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c329-128">-Каталог</span><span class="sxs-lookup"><span data-stu-id="2c329-128">-Directory</span></span>
<span data-ttu-id="2c329-129">Объект CloudFileDirectory, на котором указана базовая папка с файлами и каталогами.</span><span class="sxs-lookup"><span data-stu-id="2c329-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="2c329-130">-Файл</span><span class="sxs-lookup"><span data-stu-id="2c329-130">-File</span></span>
<span data-ttu-id="2c329-131">Объект CloudFile, который указывает файл для списка дескрипторов файлов.</span><span class="sxs-lookup"><span data-stu-id="2c329-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="2c329-132">-Path</span><span class="sxs-lookup"><span data-stu-id="2c329-132">-Path</span></span>
<span data-ttu-id="2c329-133">Путь к существующему файлу или каталогу.</span><span class="sxs-lookup"><span data-stu-id="2c329-133">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="2c329-134">-Recursive</span><span class="sxs-lookup"><span data-stu-id="2c329-134">-Recursive</span></span>
<span data-ttu-id="2c329-135">Рекурсивные дескрипторы списка.</span><span class="sxs-lookup"><span data-stu-id="2c329-135">List handles Recursively.</span></span>
<span data-ttu-id="2c329-136">Работает только в каталогах файлов.</span><span class="sxs-lookup"><span data-stu-id="2c329-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="2c329-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c329-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2c329-138">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="2c329-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="2c329-139">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="2c329-139">-Share</span></span>
<span data-ttu-id="2c329-140">Объект CloudFileShare, на котором указан общий доступ к файлам и каталогам.</span><span class="sxs-lookup"><span data-stu-id="2c329-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="2c329-141">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="2c329-141">-ShareName</span></span>
<span data-ttu-id="2c329-142">Имя общей папки, в которой будут перечислены файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="2c329-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="2c329-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2c329-143">-IncludeTotalCount</span></span>
<span data-ttu-id="2c329-144">Показывает количество объектов в наборе данных (целое число), за которыми следуют объекты.</span><span class="sxs-lookup"><span data-stu-id="2c329-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="2c329-145">Если командлет не может определить общее число, возвращается "неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="2c329-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="2c329-146">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="2c329-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="2c329-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="2c329-147">-Skip</span></span>
<span data-ttu-id="2c329-148">Пропускает первые "n" объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="2c329-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="2c329-149">-First</span><span class="sxs-lookup"><span data-stu-id="2c329-149">-First</span></span>
<span data-ttu-id="2c329-150">Возвращает только первые объекты "n".</span><span class="sxs-lookup"><span data-stu-id="2c329-150">Gets only the first 'n' objects.</span></span>

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

### <span data-ttu-id="2c329-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c329-151">CommonParameters</span></span>
<span data-ttu-id="2c329-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c329-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c329-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c329-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c329-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c329-154">INPUTS</span></span>

### <span data-ttu-id="2c329-155">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2c329-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2c329-156">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2c329-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="2c329-157">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c329-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c329-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c329-158">OUTPUTS</span></span>

### <span data-ttu-id="2c329-159">Microsoft. Azure. Storage. File. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="2c329-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="2c329-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c329-160">NOTES</span></span>

## <span data-ttu-id="2c329-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c329-161">RELATED LINKS</span></span>
