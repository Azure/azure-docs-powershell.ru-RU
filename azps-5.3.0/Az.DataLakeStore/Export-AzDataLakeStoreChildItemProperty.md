---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504610"
---
# <span data-ttu-id="69ffd-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="69ffd-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="69ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="69ffd-103">Экспорт свойств (использование диска и ACL) для всего дерева из указанного пути на выходной путь.</span><span class="sxs-lookup"><span data-stu-id="69ffd-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="69ffd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69ffd-104">SYNTAX</span></span>

### <span data-ttu-id="69ffd-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="69ffd-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69ffd-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="69ffd-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ffd-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="69ffd-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69ffd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69ffd-108">DESCRIPTION</span></span>
<span data-ttu-id="69ffd-109">**Export-AzDataLakeStoreChildItemProperty** используется для отчетов об использовании пространства ADLS или /и ACL для данного каталога, а также о его подкадрах и файлах.</span><span class="sxs-lookup"><span data-stu-id="69ffd-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="69ffd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69ffd-110">EXAMPLES</span></span>

### <span data-ttu-id="69ffd-111">Пример 1. Использование дисков и ACL для всех поднаправлений и файлов</span><span class="sxs-lookup"><span data-stu-id="69ffd-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="69ffd-112">Получите данные об использовании диска и использовании ACL для всех поднаправлений и файлов в папке /a.</span><span class="sxs-lookup"><span data-stu-id="69ffd-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="69ffd-113">IncludeFile гарантирует также, что для файлов сообщается об использовании</span><span class="sxs-lookup"><span data-stu-id="69ffd-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="69ffd-114">Пример 2. Использование ACL для всех поднаправлений и файлов с согласованным скрытым ACL</span><span class="sxs-lookup"><span data-stu-id="69ffd-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="69ffd-115">Получите использование ACL для всех поднаправленных библиотек и файлов в /a.</span><span class="sxs-lookup"><span data-stu-id="69ffd-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="69ffd-116">IncludeFile гарантирует, что для файлов также будет фикс данных об использовании.</span><span class="sxs-lookup"><span data-stu-id="69ffd-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="69ffd-117">HideconsistentAcl в этом случае будет показывать acl из /a, а не дети, так как все дети с таким же acl, как /a.</span><span class="sxs-lookup"><span data-stu-id="69ffd-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="69ffd-118">Этот флажок пропускает выход из подпотока, если все это и есть acls, то же самое, что и корневой.</span><span class="sxs-lookup"><span data-stu-id="69ffd-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="69ffd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69ffd-119">PARAMETERS</span></span>

### <span data-ttu-id="69ffd-120">-Account</span><span class="sxs-lookup"><span data-stu-id="69ffd-120">-Account</span></span>
<span data-ttu-id="69ffd-121">Учетная запись Data Lake Store для выполнения операции filesystem в</span><span class="sxs-lookup"><span data-stu-id="69ffd-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="69ffd-122">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="69ffd-122">-Concurrency</span></span>
<span data-ttu-id="69ffd-123">Количество файлов и каталогов, обработанных параллельно.</span><span class="sxs-lookup"><span data-stu-id="69ffd-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="69ffd-124">Значение по умолчанию будет вычисляться как наилучшее решение на основе спецификации системы.</span><span class="sxs-lookup"><span data-stu-id="69ffd-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="69ffd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ffd-125">-DefaultProfile</span></span>
<span data-ttu-id="69ffd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69ffd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ffd-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="69ffd-127">-GetAcl</span></span>
<span data-ttu-id="69ffd-128">Извлекает acl, начиная с корневого пути.</span><span class="sxs-lookup"><span data-stu-id="69ffd-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="69ffd-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="69ffd-129">-GetDiskUsage</span></span>
<span data-ttu-id="69ffd-130">Извлекает использование диска, начиная с корневого пути.</span><span class="sxs-lookup"><span data-stu-id="69ffd-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="69ffd-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="69ffd-131">-HideConsistentAcl</span></span>
<span data-ttu-id="69ffd-132">Не показывать подпоток каталога, если ALS одинаковы во всем подпотоке.</span><span class="sxs-lookup"><span data-stu-id="69ffd-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="69ffd-133">Это упрощает просмотр только путей, до которых отличаются ALS. Например, если все файлы и папки в /a/b одинаковы, не отобразить поддерев /a/b, а просто вычесть /a/b со столбцом "Истина" в столбце "Согласованная ACLCannot", если этот столбец не зафикс, так как не удалось определить согласованную папку ACL без иска для файлов.</span><span class="sxs-lookup"><span data-stu-id="69ffd-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="69ffd-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="69ffd-134">-IncludeFile</span></span>
<span data-ttu-id="69ffd-135">Статистика на уровне файлов (по умолчанию — только сведения на уровне каталога)</span><span class="sxs-lookup"><span data-stu-id="69ffd-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="69ffd-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="69ffd-136">-MaximumDepth</span></span>
<span data-ttu-id="69ffd-137">Максимальная глубина от корневого каталога до отображения использования диска или acl</span><span class="sxs-lookup"><span data-stu-id="69ffd-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="69ffd-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="69ffd-138">-OutputPath</span></span>
<span data-ttu-id="69ffd-139">Путь к выходной файлу.</span><span class="sxs-lookup"><span data-stu-id="69ffd-139">Path to output file.</span></span> <span data-ttu-id="69ffd-140">Может быть локальным или Adl Path.</span><span class="sxs-lookup"><span data-stu-id="69ffd-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="69ffd-141">По умолчанию он локальный.</span><span class="sxs-lookup"><span data-stu-id="69ffd-141">By default it is local.</span></span> <span data-ttu-id="69ffd-142">Если задан путь SaveToAdl, это путь ADL в той же учетной записи</span><span class="sxs-lookup"><span data-stu-id="69ffd-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="69ffd-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ffd-143">-PassThru</span></span>
<span data-ttu-id="69ffd-144">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="69ffd-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="69ffd-145">-Path</span><span class="sxs-lookup"><span data-stu-id="69ffd-145">-Path</span></span>
<span data-ttu-id="69ffd-146">Путь в указанной учетной записи Data Lake, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="69ffd-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="69ffd-147">Может быть файлом или папкой в формате '/folder/file.txt', где первая после DNS "/" указывает корневую папку файловой системы.</span><span class="sxs-lookup"><span data-stu-id="69ffd-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="69ffd-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="69ffd-148">-SaveToAdl</span></span>
<span data-ttu-id="69ffd-149">Если он прошел, файл дампов сохраняется в ADL.</span><span class="sxs-lookup"><span data-stu-id="69ffd-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="69ffd-150">В этом случае ДампФайл будет путем ADL</span><span class="sxs-lookup"><span data-stu-id="69ffd-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="69ffd-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69ffd-151">-Confirm</span></span>
<span data-ttu-id="69ffd-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69ffd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ffd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ffd-153">-WhatIf</span></span>
<span data-ttu-id="69ffd-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69ffd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ffd-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="69ffd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ffd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ffd-156">CommonParameters</span></span>
<span data-ttu-id="69ffd-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ffd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ffd-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ffd-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ffd-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69ffd-159">INPUTS</span></span>

### <span data-ttu-id="69ffd-160">System.String</span><span class="sxs-lookup"><span data-stu-id="69ffd-160">System.String</span></span>

### <span data-ttu-id="69ffd-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="69ffd-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="69ffd-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69ffd-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="69ffd-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="69ffd-163">System.Int32</span></span>

## <span data-ttu-id="69ffd-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69ffd-164">OUTPUTS</span></span>

### <span data-ttu-id="69ffd-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69ffd-165">System.Boolean</span></span>

## <span data-ttu-id="69ffd-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69ffd-166">NOTES</span></span>

## <span data-ttu-id="69ffd-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69ffd-167">RELATED LINKS</span></span>
