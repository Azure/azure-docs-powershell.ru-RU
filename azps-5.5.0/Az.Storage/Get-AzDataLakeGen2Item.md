---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231665"
---
# <span data-ttu-id="1a029-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1a029-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="1a029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a029-102">SYNOPSIS</span></span>
<span data-ttu-id="1a029-103">Получает сведения о файле или каталоге в файловойсистеме.</span><span class="sxs-lookup"><span data-stu-id="1a029-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="1a029-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a029-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a029-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a029-105">DESCRIPTION</span></span>
<span data-ttu-id="1a029-106">Для получения сведений о файле или каталоге в Filesystem учетной записи хранилища Azure можно получить сведения о файле или каталоге **Get-AzDataLakeGen2Item.**</span><span class="sxs-lookup"><span data-stu-id="1a029-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="1a029-107">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="1a029-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="1a029-108">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="1a029-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="1a029-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a029-109">EXAMPLES</span></span>

### <span data-ttu-id="1a029-110">Пример 1. Получите каталог от Filesystem и откажите подробные сведения</span><span class="sxs-lookup"><span data-stu-id="1a029-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
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
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="1a029-111">Эта команда получает каталог из Filesystem и показывает подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="1a029-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="1a029-112">Пример 2. Получить файл от Filesystem</span><span class="sxs-lookup"><span data-stu-id="1a029-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="1a029-113">Эта команда получает сведения о файле от Filesystem.</span><span class="sxs-lookup"><span data-stu-id="1a029-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="1a029-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a029-114">PARAMETERS</span></span>

### <span data-ttu-id="1a029-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="1a029-115">-Context</span></span>
<span data-ttu-id="1a029-116">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1a029-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1a029-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a029-117">-DefaultProfile</span></span>
<span data-ttu-id="1a029-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a029-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a029-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="1a029-119">-FileSystem</span></span>
<span data-ttu-id="1a029-120">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="1a029-120">FileSystem name</span></span>

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

### <span data-ttu-id="1a029-121">-Path</span><span class="sxs-lookup"><span data-stu-id="1a029-121">-Path</span></span>
<span data-ttu-id="1a029-122">Путь в указанной Filesystem, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="1a029-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="1a029-123">Может быть файлом или каталогом в формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="1a029-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="1a029-124">Не укажите этот параметр, чтобы получить корневой каталог Filesystem.</span><span class="sxs-lookup"><span data-stu-id="1a029-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a029-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a029-125">CommonParameters</span></span>
<span data-ttu-id="1a029-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a029-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a029-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a029-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a029-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a029-128">INPUTS</span></span>

### <span data-ttu-id="1a029-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1a029-129">System.String</span></span>

### <span data-ttu-id="1a029-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a029-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a029-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a029-131">OUTPUTS</span></span>

### <span data-ttu-id="1a029-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1a029-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="1a029-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a029-133">NOTES</span></span>

## <span data-ttu-id="1a029-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a029-134">RELATED LINKS</span></span>
