---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080187"
---
# <span data-ttu-id="cc07c-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="cc07c-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="cc07c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc07c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc07c-103">Скачайте файл.</span><span class="sxs-lookup"><span data-stu-id="cc07c-103">Download a file.</span></span>

## <span data-ttu-id="cc07c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc07c-104">SYNTAX</span></span>

### <span data-ttu-id="cc07c-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc07c-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc07c-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="cc07c-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc07c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc07c-107">DESCRIPTION</span></span>
<span data-ttu-id="cc07c-108">Командлет **Get-AzDataLakeGen2ItemContent** загружает файл в файловой системе учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="cc07c-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="cc07c-109">Этот командлет работает только в том случае, если для учетной записи хранения включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="cc07c-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="cc07c-110">Учетную запись такого типа можно создать с помощью командлета New-AzStorageAccount с параметром-EnableHierarchicalNamespace $true.</span><span class="sxs-lookup"><span data-stu-id="cc07c-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="cc07c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc07c-111">EXAMPLES</span></span>

### <span data-ttu-id="cc07c-112">Пример 1: Загрузка файла без запроса</span><span class="sxs-lookup"><span data-stu-id="cc07c-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="cc07c-113">Эта команда загружает файл в локальный файл без запроса.</span><span class="sxs-lookup"><span data-stu-id="cc07c-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="cc07c-114">Пример 2: получение файла, затем конвейер для скачивания файла в локальный файл</span><span class="sxs-lookup"><span data-stu-id="cc07c-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="cc07c-115">Эта команда сначала получает файл, затем конвейер, чтобы скачать файл в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="cc07c-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="cc07c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc07c-116">PARAMETERS</span></span>

### <span data-ttu-id="cc07c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc07c-117">-AsJob</span></span>
<span data-ttu-id="cc07c-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cc07c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc07c-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="cc07c-119">-CheckMd5</span></span>
<span data-ttu-id="cc07c-120">Проверка md5sum</span><span class="sxs-lookup"><span data-stu-id="cc07c-120">check the md5sum</span></span>

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

### <span data-ttu-id="cc07c-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cc07c-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cc07c-122">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="cc07c-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="cc07c-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="cc07c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="cc07c-124">-Context</span><span class="sxs-lookup"><span data-stu-id="cc07c-124">-Context</span></span>
<span data-ttu-id="cc07c-125">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="cc07c-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="cc07c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc07c-126">-DefaultProfile</span></span>
<span data-ttu-id="cc07c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc07c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc07c-128">-Destination</span><span class="sxs-lookup"><span data-stu-id="cc07c-128">-Destination</span></span>
<span data-ttu-id="cc07c-129">Путь к локальному файлу назначения.</span><span class="sxs-lookup"><span data-stu-id="cc07c-129">Destination local file path.</span></span>

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

### <span data-ttu-id="cc07c-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="cc07c-130">-FileSystem</span></span>
<span data-ttu-id="cc07c-131">Имя файловой системы</span><span class="sxs-lookup"><span data-stu-id="cc07c-131">FileSystem name</span></span>

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

### <span data-ttu-id="cc07c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cc07c-132">-Force</span></span>
<span data-ttu-id="cc07c-133">Принудительно перезаписать существующий BLOB-объект или файл</span><span class="sxs-lookup"><span data-stu-id="cc07c-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="cc07c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc07c-134">-InputObject</span></span>
<span data-ttu-id="cc07c-135">Объект элемента Azure Gen2 Item для скачивания.</span><span class="sxs-lookup"><span data-stu-id="cc07c-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="cc07c-136">-Path</span><span class="sxs-lookup"><span data-stu-id="cc07c-136">-Path</span></span>
<span data-ttu-id="cc07c-137">Путь в указанной файловой системе, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cc07c-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="cc07c-138">Может быть файлом или каталогом в формате "Directory/file.txt" или "Directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="cc07c-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="cc07c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc07c-139">-Confirm</span></span>
<span data-ttu-id="cc07c-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc07c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc07c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc07c-141">-WhatIf</span></span>
<span data-ttu-id="cc07c-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc07c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc07c-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc07c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc07c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc07c-144">CommonParameters</span></span>
<span data-ttu-id="cc07c-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc07c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc07c-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc07c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc07c-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc07c-147">INPUTS</span></span>

### <span data-ttu-id="cc07c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cc07c-148">System.String</span></span>

### <span data-ttu-id="cc07c-149">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cc07c-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="cc07c-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc07c-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cc07c-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc07c-151">OUTPUTS</span></span>

### <span data-ttu-id="cc07c-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cc07c-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="cc07c-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc07c-153">NOTES</span></span>

## <span data-ttu-id="cc07c-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc07c-154">RELATED LINKS</span></span>
