---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: f76a399d9d2e592bbea10a9e304d8f6875eea227
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318254"
---
# <span data-ttu-id="08552-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="08552-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="08552-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08552-102">SYNOPSIS</span></span>
<span data-ttu-id="08552-103">С помощью этой команды можно вручную инициировать обнаружение изменений в пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="08552-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="08552-104">Она может быть назначена всему общему доступу, вложенной папке или набору файлов.</span><span class="sxs-lookup"><span data-stu-id="08552-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="08552-105">Может быть обнаружено не более 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="08552-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="08552-106">Если вы задаете область изменений, ограничьте выполнение этой команды на части пространства имен, поэтому обнаружение изменений может завершиться быстро и в пределах числа элементов 10 000.</span><span class="sxs-lookup"><span data-stu-id="08552-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="08552-107">Командлет Invoke-AzStorageSyncChangeDetection не обнаруживает следующие изменения в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="08552-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="08552-108">Удаленные файлы.</span><span class="sxs-lookup"><span data-stu-id="08552-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="08552-109">Файлы, перемещаемые из общего доступа.</span><span class="sxs-lookup"><span data-stu-id="08552-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="08552-110">Файлы, которые будут удалены и созданы с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="08552-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="08552-111">Эти изменения будут обнаружены при запуске [задания обнаружения изменений](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) .</span><span class="sxs-lookup"><span data-stu-id="08552-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) runs.</span></span>

## <span data-ttu-id="08552-112">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08552-112">SYNTAX</span></span>

### <span data-ttu-id="08552-113">StringAndDirectoryParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08552-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08552-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="08552-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08552-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="08552-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08552-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="08552-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08552-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="08552-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08552-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="08552-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08552-119">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08552-119">DESCRIPTION</span></span>
<span data-ttu-id="08552-120">Периодически служба синхронизации файлов (Azure File Sync) проверяет пространство имен в синхронизированной общей папке Azure, чтобы изменения, которые были внесены в общий файловый объект, не были синхронизованы. Цель состоит в том, чтобы определить эти изменения и в конечном итоге синхронизировать их с подключенными серверами.</span><span class="sxs-lookup"><span data-stu-id="08552-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="08552-121">С помощью этой команды можно вручную инициировать обнаружение изменений в пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="08552-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="08552-122">Она может быть назначена всему общему доступу, вложенной папке или набору файлов.</span><span class="sxs-lookup"><span data-stu-id="08552-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="08552-123">Если вы задаете область изменений, ограничьте выполнение этой команды на части пространства имен, поэтому обнаружение изменений может завершиться быстро и в течение ограничения числа элементов в 10 000.</span><span class="sxs-lookup"><span data-stu-id="08552-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="08552-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08552-124">EXAMPLES</span></span>

### <span data-ttu-id="08552-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08552-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="08552-126">В этом примере обнаружение изменений выполняется в каталогах данных и "Reporting\Templates" в папке синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="08552-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="08552-127">Все пути относятся к корню пространства имен в службе общего доступа к файлам Azure.</span><span class="sxs-lookup"><span data-stu-id="08552-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="08552-128">Пример 2</span><span class="sxs-lookup"><span data-stu-id="08552-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="08552-129">В этом примере выполняется обнаружение изменений для набора файлов, которые были известны вызывающему объекту, для которого была изменена команда.</span><span class="sxs-lookup"><span data-stu-id="08552-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="08552-130">Цель состоит в том, что служба синхронизации файлов Azure обнаруживает и синхронизирует эти изменения тоже.</span><span class="sxs-lookup"><span data-stu-id="08552-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="08552-131">Пример 3</span><span class="sxs-lookup"><span data-stu-id="08552-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="08552-132">В этом примере выполняется обнаружение изменений для каталога "примеры" и рекурсивно обнаруживаются изменения в подкаталогах.</span><span class="sxs-lookup"><span data-stu-id="08552-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="08552-133">Имейте в виду, что командлет завершится сбоем, если путь содержат более 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="08552-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="08552-134">Если путь содержат более 10 000 элементов, выполните команду для вложенных частей пространства имен.</span><span class="sxs-lookup"><span data-stu-id="08552-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="08552-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08552-135">PARAMETERS</span></span>

### <span data-ttu-id="08552-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08552-136">-AsJob</span></span>
<span data-ttu-id="08552-137">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="08552-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08552-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08552-138">-DefaultProfile</span></span>
<span data-ttu-id="08552-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08552-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08552-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="08552-140">-DirectoryPath</span></span>
<span data-ttu-id="08552-141">Каталог, в котором будет проводиться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="08552-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08552-142">-InputObject</span></span>
<span data-ttu-id="08552-143">Объект CloudEndpoint, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="08552-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08552-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08552-144">-Name</span></span>
<span data-ttu-id="08552-145">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="08552-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="08552-146">Имя — это идентификатор GUID, а не понятное имя, отображаемое на портале.</span><span class="sxs-lookup"><span data-stu-id="08552-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="08552-147">Чтобы получить CloudEndpointName, используйте командлет Get-AzStorageSyncCloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="08552-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08552-148">-PassThru</span></span>
<span data-ttu-id="08552-149">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="08552-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="08552-150">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="08552-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="08552-151">-Path</span><span class="sxs-lookup"><span data-stu-id="08552-151">-Path</span></span>
<span data-ttu-id="08552-152">Путь, по которому будет выполняться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="08552-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-153">-Recursive</span><span class="sxs-lookup"><span data-stu-id="08552-153">-Recursive</span></span>
<span data-ttu-id="08552-154">Указывает, является ли обнаружение изменений в каталоге рекурсивным.</span><span class="sxs-lookup"><span data-stu-id="08552-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08552-155">-ResourceGroupName</span></span>
<span data-ttu-id="08552-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08552-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08552-157">-ResourceId</span></span>
<span data-ttu-id="08552-158">Идентификатор ресурса CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="08552-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08552-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="08552-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="08552-160">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="08552-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="08552-161">-SyncGroupName</span></span>
<span data-ttu-id="08552-162">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="08552-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08552-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08552-163">-Confirm</span></span>
<span data-ttu-id="08552-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08552-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08552-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08552-165">-WhatIf</span></span>
<span data-ttu-id="08552-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08552-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08552-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08552-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08552-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08552-168">CommonParameters</span></span>
<span data-ttu-id="08552-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08552-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08552-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08552-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08552-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08552-171">INPUTS</span></span>

### <span data-ttu-id="08552-172">System. String</span><span class="sxs-lookup"><span data-stu-id="08552-172">System.String</span></span>

### <span data-ttu-id="08552-173">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="08552-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="08552-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08552-174">OUTPUTS</span></span>

### <span data-ttu-id="08552-175">System. void</span><span class="sxs-lookup"><span data-stu-id="08552-175">System.Void</span></span>

## <span data-ttu-id="08552-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="08552-176">NOTES</span></span>

## <span data-ttu-id="08552-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08552-177">RELATED LINKS</span></span>
