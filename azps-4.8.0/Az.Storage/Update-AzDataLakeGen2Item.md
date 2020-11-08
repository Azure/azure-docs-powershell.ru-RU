---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236515"
---
# <span data-ttu-id="a6473-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6473-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="a6473-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6473-102">SYNOPSIS</span></span>
<span data-ttu-id="a6473-103">Обновление файлов и каталогов в свойствах, метаданных, разрешениях, списках ACL и владельцах.</span><span class="sxs-lookup"><span data-stu-id="a6473-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="a6473-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6473-104">SYNTAX</span></span>

### <span data-ttu-id="a6473-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6473-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6473-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="a6473-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6473-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6473-107">DESCRIPTION</span></span>
<span data-ttu-id="a6473-108">Командлет **Update-AzDataLakeGen2Item** обновляет файл или каталог в свойствах, метаданных, разрешениях, списках ACL и владельцах.</span><span class="sxs-lookup"><span data-stu-id="a6473-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="a6473-109">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a6473-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="a6473-110">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="a6473-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="a6473-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6473-111">EXAMPLES</span></span>

### <span data-ttu-id="a6473-112">Пример 1: создание объекта ACL с 3 записью ACL и рекурсивное обновление ACL для всех элементов в файловой системе</span><span class="sxs-lookup"><span data-stu-id="a6473-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="a6473-113">Эта команда сначала создает объект ACL с 3 записью ACL (используйте параметр-InputObject для добавления записи ACL в существующий объект ACL), а затем получает все элементы в файловой системе и обновляет список ACL для элементов.</span><span class="sxs-lookup"><span data-stu-id="a6473-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="a6473-114">Пример 2: обновление всех свойств файла и отображение</span><span class="sxs-lookup"><span data-stu-id="a6473-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="a6473-115">Эта команда обновляет все свойства файла (ACL, разрешения, владелец, группа, метаданные, свойство может обновляться с помощью любого conbination) и отображает их в консоли PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6473-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="a6473-116">Пример 3: Добавление записи ACL в каталог</span><span class="sxs-lookup"><span data-stu-id="a6473-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="a6473-117">Эта команда возвращает ACL из каталога, обновляет/добавляет запись ACL и передается в каталог.</span><span class="sxs-lookup"><span data-stu-id="a6473-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="a6473-118">Если элемент ACL с тем же AccessControlType/EntityId/DefaultScope не существует, будет добавлена новая запись списка ACL, а в другом — разрешение на обновление существующей записи ACL.</span><span class="sxs-lookup"><span data-stu-id="a6473-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="a6473-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6473-119">PARAMETERS</span></span>

### <span data-ttu-id="a6473-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="a6473-120">-Acl</span></span>
<span data-ttu-id="a6473-121">Устанавливает права на управление доступом POSIX для файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="a6473-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="a6473-122">Создайте этот объект с помощью New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="a6473-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6473-123">-Context</span><span class="sxs-lookup"><span data-stu-id="a6473-123">-Context</span></span>
<span data-ttu-id="a6473-124">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="a6473-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a6473-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6473-125">-DefaultProfile</span></span>
<span data-ttu-id="a6473-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6473-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6473-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="a6473-127">-FileSystem</span></span>
<span data-ttu-id="a6473-128">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="a6473-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6473-129">-Группа</span><span class="sxs-lookup"><span data-stu-id="a6473-129">-Group</span></span>
<span data-ttu-id="a6473-130">Задает группу владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="a6473-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="a6473-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6473-131">-InputObject</span></span>
<span data-ttu-id="a6473-132">Объект Azure Gen2 Item для обновления</span><span class="sxs-lookup"><span data-stu-id="a6473-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6473-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a6473-133">-Metadata</span></span>
<span data-ttu-id="a6473-134">Задает метаданные для каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="a6473-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="a6473-135">-Владелец</span><span class="sxs-lookup"><span data-stu-id="a6473-135">-Owner</span></span>
<span data-ttu-id="a6473-136">Задает владельца большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="a6473-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="a6473-137">-Path</span><span class="sxs-lookup"><span data-stu-id="a6473-137">-Path</span></span>
<span data-ttu-id="a6473-138">Путь в указанной файловой системе, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="a6473-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="a6473-139">Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="a6473-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="a6473-140">Не указывать этот параметр. Обновите корневой каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a6473-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6473-141">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="a6473-141">-Permission</span></span>
<span data-ttu-id="a6473-142">Устанавливает разрешения на доступ POSIX для владельца файла, группы владельца файла и других параметров.</span><span class="sxs-lookup"><span data-stu-id="a6473-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="a6473-143">Каждому классу может быть предоставлено разрешение "чтение", "запись" или "выполнение".</span><span class="sxs-lookup"><span data-stu-id="a6473-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="a6473-144">Символические символы (rwxrw-RW-) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6473-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="a6473-145">Недопустимый в сочетании с ACL.</span><span class="sxs-lookup"><span data-stu-id="a6473-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="a6473-146">-Property</span><span class="sxs-lookup"><span data-stu-id="a6473-146">-Property</span></span>
<span data-ttu-id="a6473-147">Задает свойства для каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="a6473-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="a6473-148">Поддерживаются следующие свойства файла: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="a6473-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="a6473-149">Ниже указаны поддерживаемые свойства для каталога: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="a6473-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="a6473-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6473-150">-Confirm</span></span>
<span data-ttu-id="a6473-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6473-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6473-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6473-152">-WhatIf</span></span>
<span data-ttu-id="a6473-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6473-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6473-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6473-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6473-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6473-155">CommonParameters</span></span>
<span data-ttu-id="a6473-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6473-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6473-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6473-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6473-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6473-158">INPUTS</span></span>

### <span data-ttu-id="a6473-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a6473-159">System.String</span></span>

### <span data-ttu-id="a6473-160">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6473-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="a6473-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6473-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6473-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6473-162">OUTPUTS</span></span>

### <span data-ttu-id="a6473-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="a6473-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="a6473-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6473-164">NOTES</span></span>

## <span data-ttu-id="a6473-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6473-165">RELATED LINKS</span></span>
