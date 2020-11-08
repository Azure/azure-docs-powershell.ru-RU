---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245781"
---
# <span data-ttu-id="e8bd0-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="e8bd0-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="e8bd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bd0-103">Создает или обновляет объект ACL элемента Gen2, который можно использовать в командлете Update-AzDataLakeGen2Item.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="e8bd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8bd0-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="e8bd0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bd0-106">Командлет **Set-AzDataLakeGen2ItemAclObject** создает и ОБНОВЛЯЕТ объект ACL элемента Gen2, который можно использовать в командлете Update-AzDataLakeGen2Item.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="e8bd0-107">Если новая запись ACL с тем же AccessControlType/EntityId/DefaultScope не существует в входных данных ACL, будет создана новая запись списка ACL, а в другом — разрешение на обновление существующей записи ACL.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="e8bd0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8bd0-108">EXAMPLES</span></span>

### <span data-ttu-id="e8bd0-109">Пример 1: создание объекта ACL с 3 записью ACL и обновление списка ACL в каталоге</span><span class="sxs-lookup"><span data-stu-id="e8bd0-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="e8bd0-110">Эта команда создает объект ACL с 3 записями ACL (используйте параметр-InputObject для добавления записи ACL в существующий объект ACL) и обновляет список ACL в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="e8bd0-111">Пример 2: создание объекта ACL с четырьмя записями ACL и обновление разрешений существующей записи ACL</span><span class="sxs-lookup"><span data-stu-id="e8bd0-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="e8bd0-112">Эта команда сначала создает объект ACL с четырьмя записями ACL, а затем повторно запускает командлет с различными разрешениями, но же AccessControlType/EntityId/DefaultScope существующей записи ACL.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="e8bd0-113">После этого разрешение записи ACL будет Обновлено, но новая запись ACL не будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="e8bd0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8bd0-114">PARAMETERS</span></span>

### <span data-ttu-id="e8bd0-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="e8bd0-115">-AccessControlType</span></span>
<span data-ttu-id="e8bd0-116">Существует четыре типа: "пользователь" предоставляет права владельцам или именованным пользователям, "Группа" предоставляет права для группы владельца или именованной группы, "маска" ограничивает права, предоставленные именованным пользователям и членам групп, а "другой" предоставляет права всем пользователям, не найденным в других записях.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd0-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="e8bd0-117">-DefaultScope</span></span>
<span data-ttu-id="e8bd0-118">Установите этот параметр, чтобы указать, что ACE входит в ACL по умолчанию для каталога; в противном случае область является неявной и ACE принадлежит к ACL Access.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="e8bd0-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="e8bd0-119">-EntityId</span></span>
<span data-ttu-id="e8bd0-120">Идентификатор пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-120">The user or group identifier.</span></span>
<span data-ttu-id="e8bd0-121">Оно опущено для записей AccessControlType "маска" и "другое".</span><span class="sxs-lookup"><span data-stu-id="e8bd0-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="e8bd0-122">Идентификатор пользователя или группы также не указывается для владельца и группы-владельца.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="e8bd0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8bd0-123">-InputObject</span></span>
<span data-ttu-id="e8bd0-124">При вводе объекта PSPathAccessControlEntry добавит \[ \] новый список ACL в качестве нового элемента входного \[ \] объекта PSPathAccessControlEntry.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="e8bd0-125">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="e8bd0-125">-Permission</span></span>
<span data-ttu-id="e8bd0-126">Поле разрешения является 3-символьной последовательностью, где первый символ "r" для предоставления доступа на чтение, второй символ — "w" для предоставления доступа на запись, а третий — "x" для предоставления разрешения на выполнение.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="e8bd0-127">Если доступ не предоставлен, знак "-" используется для того, чтобы отметить, что разрешение запрещено.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bd0-128">CommonParameters</span></span>
<span data-ttu-id="e8bd0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bd0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bd0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bd0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8bd0-131">INPUTS</span></span>

### <span data-ttu-id="e8bd0-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8bd0-132">None</span></span>

## <span data-ttu-id="e8bd0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8bd0-133">OUTPUTS</span></span>

### <span data-ttu-id="e8bd0-134">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="e8bd0-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="e8bd0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8bd0-135">NOTES</span></span>

## <span data-ttu-id="e8bd0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8bd0-136">RELATED LINKS</span></span>
