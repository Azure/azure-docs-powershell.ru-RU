---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: fdcac32a925cad97c256af2db949a08268e0ac3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959331"
---
# <span data-ttu-id="cd761-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd761-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="cd761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd761-102">SYNOPSIS</span></span>
<span data-ttu-id="cd761-103">Обновление файла или каталога по свойствам, метаданным, разрешению, ACL и владельцу.</span><span class="sxs-lookup"><span data-stu-id="cd761-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="cd761-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd761-104">SYNTAX</span></span>

### <span data-ttu-id="cd761-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd761-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd761-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="cd761-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd761-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd761-107">DESCRIPTION</span></span>
<span data-ttu-id="cd761-108">С **помощью cmdlet Update-AzDataLakeGen2Item** файл или каталог обновляется для свойств, метаданных, разрешений, ACL и владельца.</span><span class="sxs-lookup"><span data-stu-id="cd761-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="cd761-109">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="cd761-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="cd761-110">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="cd761-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="cd761-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd761-111">EXAMPLES</span></span>

### <span data-ttu-id="cd761-112">Пример 1. Создание объекта ACL с 3 записью ACL и обновление ACL для всех элементов в Filesystem рекурсивно</span><span class="sxs-lookup"><span data-stu-id="cd761-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="cd761-113">Эта команда сначала создает объект ACL с 3 записью acl (с помощью параметра -InputObject добавить запись к существующему объекту acl), а затем получать все элементы в filesystem и обновлять acl для элементов.</span><span class="sxs-lookup"><span data-stu-id="cd761-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="cd761-114">Пример 2. Обновление всех свойств файла и их показ</span><span class="sxs-lookup"><span data-stu-id="cd761-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="cd761-115">Эта команда обновляет все свойства файла (ACL, разрешение, владельца, группу, метаданные, свойство можно обновлять с помощью любого веб-сайта), а также показывать их в консоли Powershell.</span><span class="sxs-lookup"><span data-stu-id="cd761-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="cd761-116">Пример 3. Добавление записи ACL в каталог</span><span class="sxs-lookup"><span data-stu-id="cd761-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="cd761-117">Эта команда получает ACL из каталога, обновляет/добавляет запись ACL и возвращается в каталог.</span><span class="sxs-lookup"><span data-stu-id="cd761-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="cd761-118">Если запись ACL с тем же значением AccessControlType/EntityId/DefaultScope не существует, будет добавлена новая запись ACL, а также разрешение на обновление существующей записи ACL.</span><span class="sxs-lookup"><span data-stu-id="cd761-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="cd761-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd761-119">PARAMETERS</span></span>

### <span data-ttu-id="cd761-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="cd761-120">-Acl</span></span>
<span data-ttu-id="cd761-121">Задает права на управление доступом к POSIX для файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="cd761-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="cd761-122">Создайте этот объект с помощью New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="cd761-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="cd761-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="cd761-123">-Context</span></span>
<span data-ttu-id="cd761-124">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="cd761-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="cd761-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd761-125">-DefaultProfile</span></span>
<span data-ttu-id="cd761-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd761-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd761-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="cd761-127">-FileSystem</span></span>
<span data-ttu-id="cd761-128">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="cd761-128">FileSystem name</span></span>

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

### <span data-ttu-id="cd761-129">-Group</span><span class="sxs-lookup"><span data-stu-id="cd761-129">-Group</span></span>
<span data-ttu-id="cd761-130">Задает группу владельцев этого BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="cd761-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="cd761-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd761-131">-InputObject</span></span>
<span data-ttu-id="cd761-132">Объект Элемента Azure Datalake Gen2 для обновления</span><span class="sxs-lookup"><span data-stu-id="cd761-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="cd761-133">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="cd761-133">-Metadata</span></span>
<span data-ttu-id="cd761-134">Определяет метаданные для каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="cd761-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="cd761-135">-Владелец</span><span class="sxs-lookup"><span data-stu-id="cd761-135">-Owner</span></span>
<span data-ttu-id="cd761-136">Задает владельца BLOB-сайта.</span><span class="sxs-lookup"><span data-stu-id="cd761-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="cd761-137">-Path</span><span class="sxs-lookup"><span data-stu-id="cd761-137">-Path</span></span>
<span data-ttu-id="cd761-138">Путь в указанной Filesystem, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="cd761-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="cd761-139">Может быть файлом или каталогом в формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="cd761-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="cd761-140">Не укажите этот параметр, чтобы обновить корневой каталог Filesystem.</span><span class="sxs-lookup"><span data-stu-id="cd761-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="cd761-141">-Permission</span><span class="sxs-lookup"><span data-stu-id="cd761-141">-Permission</span></span>
<span data-ttu-id="cd761-142">Задает разрешения на доступ к POSIX для владельца файла, группы владельцев файла и других лиц.</span><span class="sxs-lookup"><span data-stu-id="cd761-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="cd761-143">Каждому классу может быть предоставлено разрешение на чтение, написание и выполнение.</span><span class="sxs-lookup"><span data-stu-id="cd761-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="cd761-144">Поддерживается символ (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="cd761-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="cd761-145">Недопустимый в сочетании с ACL.</span><span class="sxs-lookup"><span data-stu-id="cd761-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="cd761-146">-Свойство</span><span class="sxs-lookup"><span data-stu-id="cd761-146">-Property</span></span>
<span data-ttu-id="cd761-147">Определяет свойства каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="cd761-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="cd761-148">Поддерживаются такие свойства файла: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="cd761-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="cd761-149">Для каталога поддерживаются такие свойства: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="cd761-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="cd761-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd761-150">-Confirm</span></span>
<span data-ttu-id="cd761-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd761-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd761-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd761-152">-WhatIf</span></span>
<span data-ttu-id="cd761-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd761-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd761-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd761-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd761-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd761-155">CommonParameters</span></span>
<span data-ttu-id="cd761-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd761-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd761-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd761-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd761-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd761-158">INPUTS</span></span>

### <span data-ttu-id="cd761-159">System.String</span><span class="sxs-lookup"><span data-stu-id="cd761-159">System.String</span></span>

### <span data-ttu-id="cd761-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd761-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="cd761-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd761-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd761-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd761-162">OUTPUTS</span></span>

### <span data-ttu-id="cd761-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd761-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="cd761-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd761-164">NOTES</span></span>

## <span data-ttu-id="cd761-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd761-165">RELATED LINKS</span></span>
