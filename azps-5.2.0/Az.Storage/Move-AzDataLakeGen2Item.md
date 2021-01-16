---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324901"
---
# <span data-ttu-id="2234c-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2234c-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="2234c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2234c-102">SYNOPSIS</span></span>
<span data-ttu-id="2234c-103">Перемещение файла или каталога в другой файл или каталог в той же учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2234c-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="2234c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2234c-104">SYNTAX</span></span>

### <span data-ttu-id="2234c-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2234c-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2234c-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="2234c-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2234c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2234c-107">DESCRIPTION</span></span>
<span data-ttu-id="2234c-108">При **этом файл** или каталог перемещается в другой файл или каталог в той же учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2234c-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="2234c-109">Этот cmdlet работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2234c-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="2234c-110">Учетную запись такого типа можно создать с помощью cmdlet "New-AzStorageAccount" с помощью функции "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="2234c-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="2234c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2234c-111">EXAMPLES</span></span>

### <span data-ttu-id="2234c-112">Пример 1. Перемещение сгиба в той же filesystem</span><span class="sxs-lookup"><span data-stu-id="2234c-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="2234c-113">Эта команда перемещает каталог dir1 в каталог "dir3" в той же filesystem.</span><span class="sxs-lookup"><span data-stu-id="2234c-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="2234c-114">Пример 2. Перемещение файла по конвейеру в другую систему в той же учетной записи хранения без запроса</span><span class="sxs-lookup"><span data-stu-id="2234c-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="2234c-115">Эта команда перемещает файл dir1/file1 в filesystem1 в файл dir2/file2 в "filesystem2" в той же учетной записи хранения без запроса.</span><span class="sxs-lookup"><span data-stu-id="2234c-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="2234c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2234c-116">PARAMETERS</span></span>

### <span data-ttu-id="2234c-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2234c-117">-Context</span></span>
<span data-ttu-id="2234c-118">Контекстный объект хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2234c-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2234c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2234c-119">-DefaultProfile</span></span>
<span data-ttu-id="2234c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2234c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2234c-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="2234c-121">-DestFileSystem</span></span>
<span data-ttu-id="2234c-122">Имя Dest FileSystem</span><span class="sxs-lookup"><span data-stu-id="2234c-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="2234c-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="2234c-123">-DestPath</span></span>
<span data-ttu-id="2234c-124">Путь Dest BLOB</span><span class="sxs-lookup"><span data-stu-id="2234c-124">Dest Blob path</span></span>

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

### <span data-ttu-id="2234c-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2234c-125">-FileSystem</span></span>
<span data-ttu-id="2234c-126">Имя FileSystem</span><span class="sxs-lookup"><span data-stu-id="2234c-126">FileSystem name</span></span>

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

### <span data-ttu-id="2234c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2234c-127">-Force</span></span>
<span data-ttu-id="2234c-128">Принудительное написания назначения.</span><span class="sxs-lookup"><span data-stu-id="2234c-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="2234c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2234c-129">-InputObject</span></span>
<span data-ttu-id="2234c-130">Объект Элемента Azure Datalake Gen2 для перемещения.</span><span class="sxs-lookup"><span data-stu-id="2234c-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="2234c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="2234c-131">-Path</span></span>
<span data-ttu-id="2234c-132">Путь в указанной Filesystem, из которых следует переходить.</span><span class="sxs-lookup"><span data-stu-id="2234c-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="2234c-133">Может быть файлом или каталогом в формате "каталог/file.txt" или "каталог1/каталог2/".</span><span class="sxs-lookup"><span data-stu-id="2234c-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2234c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2234c-134">-Confirm</span></span>
<span data-ttu-id="2234c-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2234c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2234c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2234c-136">-WhatIf</span></span>
<span data-ttu-id="2234c-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2234c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2234c-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2234c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2234c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2234c-139">CommonParameters</span></span>
<span data-ttu-id="2234c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2234c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2234c-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2234c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2234c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2234c-142">INPUTS</span></span>

### <span data-ttu-id="2234c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2234c-143">System.String</span></span>

### <span data-ttu-id="2234c-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2234c-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="2234c-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2234c-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2234c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2234c-146">OUTPUTS</span></span>

### <span data-ttu-id="2234c-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2234c-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="2234c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2234c-148">NOTES</span></span>

## <span data-ttu-id="2234c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2234c-149">RELATED LINKS</span></span>