---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236982"
---
# <span data-ttu-id="626ff-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="626ff-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="626ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="626ff-102">SYNOPSIS</span></span>
<span data-ttu-id="626ff-103">Экспорт свойств (использование дискового пространства и ACL) для всего дерева по заданному пути на выходном пути</span><span class="sxs-lookup"><span data-stu-id="626ff-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="626ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="626ff-104">SYNTAX</span></span>

### <span data-ttu-id="626ff-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="626ff-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="626ff-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="626ff-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="626ff-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="626ff-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="626ff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ff-108">DESCRIPTION</span></span>
<span data-ttu-id="626ff-109">**Export-AzDataLakeStoreChildItemProperty** используется для составления отчета об использовании пространства ADLS или об использовании ACL для определенного каталога, а также его вложенных папок и файлов.</span><span class="sxs-lookup"><span data-stu-id="626ff-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="626ff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="626ff-110">EXAMPLES</span></span>

### <span data-ttu-id="626ff-111">Пример 1: использование дискового пространства и использование ACL для всех подкаталогов и файлов</span><span class="sxs-lookup"><span data-stu-id="626ff-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="626ff-112">Получение сведений об использовании диска и использовании ACL для всех подкаталогов и файлов в разделе/a.</span><span class="sxs-lookup"><span data-stu-id="626ff-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="626ff-113">IncludeFile обеспечивает получение сведений о том, что они также будут использоваться для файлов</span><span class="sxs-lookup"><span data-stu-id="626ff-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="626ff-114">Пример 2: получение сведений об использовании ACL для всех подкаталогов и файлов с скрытым списком ACL</span><span class="sxs-lookup"><span data-stu-id="626ff-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="626ff-115">Получение сведений об использовании ACL для всех подкаталогов и файлов в разделе/a.</span><span class="sxs-lookup"><span data-stu-id="626ff-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="626ff-116">IncludeFile гарантирует получение сведений о том, что они будут использоваться для файлов.</span><span class="sxs-lookup"><span data-stu-id="626ff-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="626ff-117">HideconsistentAcl в этом случае будет показывать ACL для/a, а не дети, так как все дочерние элементы имеют тот же список ACL, что и/a.</span><span class="sxs-lookup"><span data-stu-id="626ff-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="626ff-118">Этот флаг пропускает вывод ACL для поддерева, если все его ACL совпадают с корневым каталогом.</span><span class="sxs-lookup"><span data-stu-id="626ff-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="626ff-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="626ff-119">PARAMETERS</span></span>

### <span data-ttu-id="626ff-120">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="626ff-120">-Account</span></span>
<span data-ttu-id="626ff-121">Учетная запись Data Lake Store для выполнения операции файловой системы</span><span class="sxs-lookup"><span data-stu-id="626ff-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-122">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="626ff-122">-Concurrency</span></span>
<span data-ttu-id="626ff-123">Указывает количество параллельных файлов или каталогов.</span><span class="sxs-lookup"><span data-stu-id="626ff-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="626ff-124">Значение по умолчанию будет вычислено для наилучшего усилия на основе спецификации системы.</span><span class="sxs-lookup"><span data-stu-id="626ff-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626ff-125">-DefaultProfile</span></span>
<span data-ttu-id="626ff-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="626ff-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="626ff-127">-GetAcl</span></span>
<span data-ttu-id="626ff-128">Извлекает список ACL, начиная с корневого пути.</span><span class="sxs-lookup"><span data-stu-id="626ff-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="626ff-129">-GetDiskUsage</span></span>
<span data-ttu-id="626ff-130">Извлекает использование диска, начиная с корневого пути.</span><span class="sxs-lookup"><span data-stu-id="626ff-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="626ff-131">-HideConsistentAcl</span></span>
<span data-ttu-id="626ff-132">Не показывать поддерево каталогов, если все списки ACL одинаковы во всем поддереве.</span><span class="sxs-lookup"><span data-stu-id="626ff-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="626ff-133">Это упрощает просмотр только тех путей, до которых они отличаются. Например, если все файлы и папки в/a/b совпадают, не выполняйте subtreeunder/a/b и просто выводите значение "истина" в списке "", если параметр ColumnCannot не установлен, так как не удается определить список ACL, не получая списки ACL для файлов.</span><span class="sxs-lookup"><span data-stu-id="626ff-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="626ff-134">-IncludeFile</span></span>
<span data-ttu-id="626ff-135">Отображать статистику на уровне файлов (по умолчанию отображаются только сведения на уровне каталога)</span><span class="sxs-lookup"><span data-stu-id="626ff-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="626ff-136">-MaximumDepth</span></span>
<span data-ttu-id="626ff-137">Максимальная глубина в корневом каталоге, в которой отображаются сведения об использовании диска и ACL</span><span class="sxs-lookup"><span data-stu-id="626ff-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="626ff-138">-OutputPath</span></span>
<span data-ttu-id="626ff-139">Путь к выходному файлу.</span><span class="sxs-lookup"><span data-stu-id="626ff-139">Path to output file.</span></span> <span data-ttu-id="626ff-140">Это может быть локальный путь или ADL путь.</span><span class="sxs-lookup"><span data-stu-id="626ff-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="626ff-141">По умолчанию он является локальным.</span><span class="sxs-lookup"><span data-stu-id="626ff-141">By default it is local.</span></span> <span data-ttu-id="626ff-142">Если указан SaveToAdl, это ADL путь в той же учетной записи</span><span class="sxs-lookup"><span data-stu-id="626ff-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="626ff-143">-PassThru</span></span>
<span data-ttu-id="626ff-144">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="626ff-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-145">-Path</span><span class="sxs-lookup"><span data-stu-id="626ff-145">-Path</span></span>
<span data-ttu-id="626ff-146">Путь в заданной учетной записи Data Lake, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="626ff-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="626ff-147">Может быть файлом или папкой в формате "/Folder/file.txt", где первый символ "/" после DNS указывает на корневой каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="626ff-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="626ff-148">-SaveToAdl</span></span>
<span data-ttu-id="626ff-149">После перепередачи файл дампа сохраняется в ADL.</span><span class="sxs-lookup"><span data-stu-id="626ff-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="626ff-150">Будет DumpFile в этом случае — это путь к ADL</span><span class="sxs-lookup"><span data-stu-id="626ff-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626ff-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="626ff-151">-Confirm</span></span>
<span data-ttu-id="626ff-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="626ff-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626ff-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626ff-153">-WhatIf</span></span>
<span data-ttu-id="626ff-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="626ff-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626ff-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="626ff-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626ff-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626ff-156">CommonParameters</span></span>
<span data-ttu-id="626ff-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="626ff-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626ff-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="626ff-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626ff-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="626ff-159">INPUTS</span></span>

### <span data-ttu-id="626ff-160">System. String</span><span class="sxs-lookup"><span data-stu-id="626ff-160">System.String</span></span>

### <span data-ttu-id="626ff-161">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="626ff-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="626ff-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="626ff-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="626ff-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="626ff-163">System.Int32</span></span>

## <span data-ttu-id="626ff-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ff-164">OUTPUTS</span></span>

### <span data-ttu-id="626ff-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="626ff-165">System.Boolean</span></span>

## <span data-ttu-id="626ff-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="626ff-166">NOTES</span></span>

## <span data-ttu-id="626ff-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="626ff-167">RELATED LINKS</span></span>