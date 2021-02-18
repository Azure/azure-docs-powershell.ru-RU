---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224940"
---
# <span data-ttu-id="29f58-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="29f58-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="29f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f58-102">SYNOPSIS</span></span>
<span data-ttu-id="29f58-103">Создайте файл или каталог в файловойсистеме.</span><span class="sxs-lookup"><span data-stu-id="29f58-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="29f58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29f58-104">SYNTAX</span></span>

### <span data-ttu-id="29f58-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29f58-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f58-106">Каталог</span><span class="sxs-lookup"><span data-stu-id="29f58-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f58-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29f58-107">DESCRIPTION</span></span>
<span data-ttu-id="29f58-108">Для создания файла или каталога в Filesystem в учетной записи хранилища Azure создается проектлет **New-AzDataLakeGen2Item.**</span><span class="sxs-lookup"><span data-stu-id="29f58-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="29f58-109">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="29f58-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="29f58-110">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="29f58-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="29f58-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29f58-111">EXAMPLES</span></span>

### <span data-ttu-id="29f58-112">Пример 1. Создание каталога с заданным разрешением, Propertiessk, свойств и метаданных</span><span class="sxs-lookup"><span data-stu-id="29f58-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="29f58-113">Эта команда создает каталог с указанными разрешениями, Овском, свойствами и метаданными</span><span class="sxs-lookup"><span data-stu-id="29f58-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="29f58-114">Пример 2. Создайте (выкладывайте) файл озера данных из локального источника, и cmdlet работает в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="29f58-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="29f58-115">Эта команда создает (выкладывайте) файл озера данных из локального источника, и командлет выполняется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="29f58-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="29f58-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29f58-116">PARAMETERS</span></span>

### <span data-ttu-id="29f58-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29f58-117">-AsJob</span></span>
<span data-ttu-id="29f58-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="29f58-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29f58-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29f58-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29f58-120">Общий объем одновременной работы с async.</span><span class="sxs-lookup"><span data-stu-id="29f58-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="29f58-121">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="29f58-121">The default value is 10.</span></span>

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

### <span data-ttu-id="29f58-122">-Контекст</span><span class="sxs-lookup"><span data-stu-id="29f58-122">-Context</span></span>
<span data-ttu-id="29f58-123">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="29f58-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="29f58-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f58-124">-DefaultProfile</span></span>
<span data-ttu-id="29f58-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29f58-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f58-126">-Каталог</span><span class="sxs-lookup"><span data-stu-id="29f58-126">-Directory</span></span>
<span data-ttu-id="29f58-127">Указывает на то, что новый элемент является каталогом, а не файлом.</span><span class="sxs-lookup"><span data-stu-id="29f58-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="29f58-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="29f58-128">-FileSystem</span></span>
<span data-ttu-id="29f58-129">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="29f58-129">FileSystem name</span></span>

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

### <span data-ttu-id="29f58-130">-Force</span><span class="sxs-lookup"><span data-stu-id="29f58-130">-Force</span></span>
<span data-ttu-id="29f58-131">Если он прошел, новый элемент создается без запроса</span><span class="sxs-lookup"><span data-stu-id="29f58-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="29f58-132">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="29f58-132">-Metadata</span></span>
<span data-ttu-id="29f58-133">Определяет метаданные для созданного каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="29f58-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="29f58-134">-Path</span><span class="sxs-lookup"><span data-stu-id="29f58-134">-Path</span></span>
<span data-ttu-id="29f58-135">Путь в указанной Filesystem, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="29f58-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="29f58-136">Может быть файлом или каталогом в формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="29f58-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="29f58-137">-Permission</span><span class="sxs-lookup"><span data-stu-id="29f58-137">-Permission</span></span>
<span data-ttu-id="29f58-138">Задает разрешения на доступ к POSIX для владельца файла, группы владельцев файла и других лиц.</span><span class="sxs-lookup"><span data-stu-id="29f58-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="29f58-139">Каждому классу может быть предоставлено разрешение на чтение, написание и выполнение.</span><span class="sxs-lookup"><span data-stu-id="29f58-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="29f58-140">Символ (rwxrw-rw-) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29f58-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="29f58-141">-Свойство</span><span class="sxs-lookup"><span data-stu-id="29f58-141">-Property</span></span>
<span data-ttu-id="29f58-142">Определяет свойства созданного каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="29f58-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="29f58-143">Поддерживаются такие свойства файла: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="29f58-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="29f58-144">Для каталога поддерживаются такие свойства: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="29f58-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="29f58-145">-Source</span><span class="sxs-lookup"><span data-stu-id="29f58-145">-Source</span></span>
<span data-ttu-id="29f58-146">Укажите путь к локальному источнику файла, который будет добавлен в файл Datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="29f58-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="29f58-147">-Аsk</span><span class="sxs-lookup"><span data-stu-id="29f58-147">-Umask</span></span>
<span data-ttu-id="29f58-148">При создании нового элемента в родительском каталоге нет стандартного ACL, она ограничивает разрешения для файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="29f58-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="29f58-149">Итоговая разрешение предоставляется p & ^u, где p — это разрешение, а вы — sksk.</span><span class="sxs-lookup"><span data-stu-id="29f58-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="29f58-150">Символ (rwxrw-rw-) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="29f58-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="29f58-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29f58-151">-Confirm</span></span>
<span data-ttu-id="29f58-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="29f58-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f58-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f58-153">-WhatIf</span></span>
<span data-ttu-id="29f58-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f58-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f58-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29f58-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f58-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f58-156">CommonParameters</span></span>
<span data-ttu-id="29f58-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f58-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f58-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f58-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f58-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29f58-159">INPUTS</span></span>

### <span data-ttu-id="29f58-160">System.String</span><span class="sxs-lookup"><span data-stu-id="29f58-160">System.String</span></span>

### <span data-ttu-id="29f58-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29f58-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29f58-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29f58-162">OUTPUTS</span></span>

### <span data-ttu-id="29f58-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="29f58-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="29f58-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29f58-164">NOTES</span></span>

## <span data-ttu-id="29f58-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29f58-165">RELATED LINKS</span></span>
