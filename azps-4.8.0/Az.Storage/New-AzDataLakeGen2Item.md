---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235249"
---
# <span data-ttu-id="7ed48-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7ed48-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="7ed48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed48-103">Создание файла или папки в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="7ed48-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="7ed48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ed48-104">SYNTAX</span></span>

### <span data-ttu-id="7ed48-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ed48-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed48-106">Папка</span><span class="sxs-lookup"><span data-stu-id="7ed48-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed48-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed48-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed48-108">Командлет **New-AzDataLakeGen2Item** создает файл или каталог в файловой системе учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed48-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="7ed48-109">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="7ed48-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="7ed48-110">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="7ed48-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="7ed48-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ed48-111">EXAMPLES</span></span>

### <span data-ttu-id="7ed48-112">Пример 1: создание каталога с указанными разрешениями, umask, свойствами и метаданными</span><span class="sxs-lookup"><span data-stu-id="7ed48-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="7ed48-113">Эта команда создает каталог с указанными разрешениями, umask, свойствами и метаданными.</span><span class="sxs-lookup"><span data-stu-id="7ed48-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="7ed48-114">Пример 2: Create (upload) Data Lake file из локального исходного файла, а командлет выполняется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7ed48-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="7ed48-115">Эта команда создает (отправляет) файл Data Lake из локального исходного файла, а командлет выполняется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7ed48-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="7ed48-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ed48-116">PARAMETERS</span></span>

### <span data-ttu-id="7ed48-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ed48-117">-AsJob</span></span>
<span data-ttu-id="7ed48-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ed48-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ed48-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7ed48-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7ed48-120">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="7ed48-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="7ed48-121">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="7ed48-121">The default value is 10.</span></span>

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

### <span data-ttu-id="7ed48-122">-Context</span><span class="sxs-lookup"><span data-stu-id="7ed48-122">-Context</span></span>
<span data-ttu-id="7ed48-123">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="7ed48-123">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed48-124">-DefaultProfile</span></span>
<span data-ttu-id="7ed48-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed48-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed48-126">-Каталог</span><span class="sxs-lookup"><span data-stu-id="7ed48-126">-Directory</span></span>
<span data-ttu-id="7ed48-127">Указывает, что этот новый элемент является каталогом, а не файлом.</span><span class="sxs-lookup"><span data-stu-id="7ed48-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7ed48-128">-FileSystem</span></span>
<span data-ttu-id="7ed48-129">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="7ed48-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7ed48-130">-Force</span></span>
<span data-ttu-id="7ed48-131">Если передается, новый элемент создается без запроса</span><span class="sxs-lookup"><span data-stu-id="7ed48-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="7ed48-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7ed48-132">-Metadata</span></span>
<span data-ttu-id="7ed48-133">Задает метаданные для созданной папки или файла.</span><span class="sxs-lookup"><span data-stu-id="7ed48-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-134">-Path</span><span class="sxs-lookup"><span data-stu-id="7ed48-134">-Path</span></span>
<span data-ttu-id="7ed48-135">Путь в указанной файловой системе, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="7ed48-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="7ed48-136">Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="7ed48-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-137">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="7ed48-137">-Permission</span></span>
<span data-ttu-id="7ed48-138">Устанавливает разрешения на доступ POSIX для владельца файла, группы владельца файла и других параметров.</span><span class="sxs-lookup"><span data-stu-id="7ed48-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="7ed48-139">Каждому классу может быть предоставлено разрешение "чтение", "запись" или "выполнение".</span><span class="sxs-lookup"><span data-stu-id="7ed48-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="7ed48-140">Символические символы (rwxrw-RW-) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7ed48-140">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-141">-Property</span><span class="sxs-lookup"><span data-stu-id="7ed48-141">-Property</span></span>
<span data-ttu-id="7ed48-142">Задает свойства созданного каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="7ed48-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="7ed48-143">Поддерживаются следующие свойства файла: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="7ed48-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="7ed48-144">Ниже указаны поддерживаемые свойства для каталога: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="7ed48-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-145">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="7ed48-145">-Source</span></span>
<span data-ttu-id="7ed48-146">Укажите путь к локальному исходному файлу, который будет отправляться в файл Gen2.</span><span class="sxs-lookup"><span data-stu-id="7ed48-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="7ed48-147">-Umask</span></span>
<span data-ttu-id="7ed48-148">Когда вы создаете новый элемент и родительский каталог не имеет ACL по умолчанию, umask ограничивает разрешения для создаваемого файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="7ed48-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="7ed48-149">Результирующее разрешение задается p & ^ u, где p — это разрешение, и ты umask.</span><span class="sxs-lookup"><span data-stu-id="7ed48-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="7ed48-150">Символические символы (rwxrw-RW-) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7ed48-150">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed48-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ed48-151">-Confirm</span></span>
<span data-ttu-id="7ed48-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ed48-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed48-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed48-153">-WhatIf</span></span>
<span data-ttu-id="7ed48-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ed48-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed48-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ed48-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed48-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed48-156">CommonParameters</span></span>
<span data-ttu-id="7ed48-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ed48-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed48-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed48-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed48-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ed48-159">INPUTS</span></span>

### <span data-ttu-id="7ed48-160">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed48-160">System.String</span></span>

### <span data-ttu-id="7ed48-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ed48-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7ed48-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed48-162">OUTPUTS</span></span>

### <span data-ttu-id="7ed48-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7ed48-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="7ed48-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ed48-164">NOTES</span></span>

## <span data-ttu-id="7ed48-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ed48-165">RELATED LINKS</span></span>
