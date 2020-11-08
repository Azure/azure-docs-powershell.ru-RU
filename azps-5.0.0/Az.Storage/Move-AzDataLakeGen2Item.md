---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249755"
---
# <span data-ttu-id="ed47e-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ed47e-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="ed47e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed47e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47e-103">Перемещение файла или каталога в другой файл или каталог в одной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ed47e-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="ed47e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed47e-104">SYNTAX</span></span>

### <span data-ttu-id="ed47e-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed47e-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed47e-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="ed47e-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed47e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed47e-107">DESCRIPTION</span></span>
<span data-ttu-id="ed47e-108">Командлет **Move-AzDataLakeGen2Item** перемещает файл или каталог в другой файл или каталог в одной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ed47e-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="ed47e-109">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ed47e-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="ed47e-110">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="ed47e-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="ed47e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed47e-111">EXAMPLES</span></span>

### <span data-ttu-id="ed47e-112">Пример 1: перемещение сгиба в той же файловой системе</span><span class="sxs-lookup"><span data-stu-id="ed47e-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="ed47e-113">С помощью этой команды вы можете переместить каталог "dir1" в каталог "dir3" в той же файловой системе.</span><span class="sxs-lookup"><span data-stu-id="ed47e-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="ed47e-114">Пример 2. Перемещение файла по конвейеру в другую файловую систему в той же учетной записи хранения без запроса</span><span class="sxs-lookup"><span data-stu-id="ed47e-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="ed47e-115">Эта команда перемещение файла "dir1/file1" в "filesystem1" в файл "Dir2/File2" в разделе "filesystem2" в той же учетной записи хранения без запроса.</span><span class="sxs-lookup"><span data-stu-id="ed47e-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="ed47e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed47e-116">PARAMETERS</span></span>

### <span data-ttu-id="ed47e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ed47e-117">-Context</span></span>
<span data-ttu-id="ed47e-118">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="ed47e-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ed47e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47e-119">-DefaultProfile</span></span>
<span data-ttu-id="ed47e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed47e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed47e-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="ed47e-121">-DestFileSystem</span></span>
<span data-ttu-id="ed47e-122">Имя файловой системы для dest</span><span class="sxs-lookup"><span data-stu-id="ed47e-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="ed47e-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="ed47e-123">-DestPath</span></span>
<span data-ttu-id="ed47e-124">Путь к BLOB-объекту приемника</span><span class="sxs-lookup"><span data-stu-id="ed47e-124">Dest Blob path</span></span>

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

### <span data-ttu-id="ed47e-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="ed47e-125">-FileSystem</span></span>
<span data-ttu-id="ed47e-126">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="ed47e-126">FileSystem name</span></span>

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

### <span data-ttu-id="ed47e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ed47e-127">-Force</span></span>
<span data-ttu-id="ed47e-128">Принудительно запишите конечную точку.</span><span class="sxs-lookup"><span data-stu-id="ed47e-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="ed47e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed47e-129">-InputObject</span></span>
<span data-ttu-id="ed47e-130">Объект элемента Azure Gen2 Item для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ed47e-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="ed47e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="ed47e-131">-Path</span></span>
<span data-ttu-id="ed47e-132">Путь в указанной файловой системе, с которого следует переместиться.</span><span class="sxs-lookup"><span data-stu-id="ed47e-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="ed47e-133">Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="ed47e-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="ed47e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed47e-134">-Confirm</span></span>
<span data-ttu-id="ed47e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed47e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed47e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed47e-136">-WhatIf</span></span>
<span data-ttu-id="ed47e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed47e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed47e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed47e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed47e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47e-139">CommonParameters</span></span>
<span data-ttu-id="ed47e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed47e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed47e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed47e-142">INPUTS</span></span>

### <span data-ttu-id="ed47e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ed47e-143">System.String</span></span>

### <span data-ttu-id="ed47e-144">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ed47e-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="ed47e-145">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed47e-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed47e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed47e-146">OUTPUTS</span></span>

### <span data-ttu-id="ed47e-147">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="ed47e-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="ed47e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed47e-148">NOTES</span></span>

## <span data-ttu-id="ed47e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed47e-149">RELATED LINKS</span></span>
