---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073134"
---
# <span data-ttu-id="33677-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="33677-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="33677-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33677-102">SYNOPSIS</span></span>
<span data-ttu-id="33677-103">С помощью этой команды можно вручную инициировать обнаружение изменений в пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="33677-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="33677-104">Она может быть назначена всему общему доступу, вложенной папке или набору файлов.</span><span class="sxs-lookup"><span data-stu-id="33677-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="33677-105">Может быть обнаружено не более 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="33677-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="33677-106">Если вы задаете область изменений, ограничьте выполнение этой команды на части пространства имен, поэтому обнаружение изменений может завершиться быстро и в пределах числа элементов 10 000.</span><span class="sxs-lookup"><span data-stu-id="33677-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="33677-107">Командлет Invoke-AzStorageSyncChangeDetection не будет определять файлы, удаленные в службе общего доступа к файлам Azure.</span><span class="sxs-lookup"><span data-stu-id="33677-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="33677-108">Если файлы удаляются в общей папке Azure, они будут обнаружены при запуске [задания обнаружения изменений](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) .</span><span class="sxs-lookup"><span data-stu-id="33677-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="33677-109">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33677-109">SYNTAX</span></span>

### <span data-ttu-id="33677-110">StringAndDirectoryParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33677-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33677-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="33677-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33677-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="33677-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33677-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="33677-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33677-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="33677-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33677-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="33677-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33677-116">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33677-116">DESCRIPTION</span></span>
<span data-ttu-id="33677-117">Периодически служба синхронизации файлов (Azure File Sync) проверяет пространство имен в синхронизированной общей папке Azure, чтобы изменения, которые были внесены в общий файловый объект, не были синхронизованы. Цель состоит в том, чтобы определить эти изменения и в конечном итоге синхронизировать их с подключенными серверами.</span><span class="sxs-lookup"><span data-stu-id="33677-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="33677-118">С помощью этой команды можно вручную инициировать обнаружение изменений в пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="33677-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="33677-119">Она может быть назначена всему общему доступу, вложенной папке или набору файлов.</span><span class="sxs-lookup"><span data-stu-id="33677-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="33677-120">Если вы задаете область изменений, ограничьте выполнение этой команды на части пространства имен, поэтому обнаружение изменений может завершиться быстро и в течение 10 000 изменится.</span><span class="sxs-lookup"><span data-stu-id="33677-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="33677-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33677-121">EXAMPLES</span></span>

### <span data-ttu-id="33677-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33677-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="33677-123">В этом примере обнаружение изменений выполняется в каталогах данных и "Reporting\Templates" в папке синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="33677-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="33677-124">Все пути относятся к корню пространства имен в службе общего доступа к файлам Azure.</span><span class="sxs-lookup"><span data-stu-id="33677-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="33677-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="33677-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="33677-126">В этом примере выполняется обнаружение изменений для набора файлов, которые были известны вызывающему объекту, для которого была изменена команда.</span><span class="sxs-lookup"><span data-stu-id="33677-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="33677-127">Цель состоит в том, что служба синхронизации файлов Azure обнаруживает и синхронизирует эти изменения тоже.</span><span class="sxs-lookup"><span data-stu-id="33677-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="33677-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="33677-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="33677-129">В этом примере выполняется обнаружение изменений для каталога "примеры" и рекурсивно обнаруживаются изменения в подкаталогах.</span><span class="sxs-lookup"><span data-stu-id="33677-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="33677-130">Имейте в виду, что эта команда может обнаружить до 10 000 изменений, прежде чем она будет автоматически прервана.</span><span class="sxs-lookup"><span data-stu-id="33677-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="33677-131">Если вы подозреваете, что более чем 10 000 изменится, выполните команду для вложенных частей пространства имен.</span><span class="sxs-lookup"><span data-stu-id="33677-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="33677-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33677-132">PARAMETERS</span></span>

### <span data-ttu-id="33677-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33677-133">-AsJob</span></span>
<span data-ttu-id="33677-134">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33677-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33677-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33677-135">-DefaultProfile</span></span>
<span data-ttu-id="33677-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33677-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33677-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="33677-137">-DirectoryPath</span></span>
<span data-ttu-id="33677-138">Каталог, в котором будет проводиться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="33677-138">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="33677-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33677-139">-InputObject</span></span>
<span data-ttu-id="33677-140">Объект CloudEndpoint, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="33677-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="33677-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33677-141">-Name</span></span>
<span data-ttu-id="33677-142">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="33677-142">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="33677-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33677-143">-PassThru</span></span>
<span data-ttu-id="33677-144">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="33677-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="33677-145">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="33677-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="33677-146">-Path</span><span class="sxs-lookup"><span data-stu-id="33677-146">-Path</span></span>
<span data-ttu-id="33677-147">Путь, по которому будет выполняться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="33677-147">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="33677-148">-Recursive</span><span class="sxs-lookup"><span data-stu-id="33677-148">-Recursive</span></span>
<span data-ttu-id="33677-149">Указывает, является ли обнаружение изменений в каталоге рекурсивным.</span><span class="sxs-lookup"><span data-stu-id="33677-149">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="33677-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33677-150">-ResourceGroupName</span></span>
<span data-ttu-id="33677-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33677-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="33677-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33677-152">-ResourceId</span></span>
<span data-ttu-id="33677-153">Идентификатор ресурса CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="33677-153">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="33677-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="33677-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="33677-155">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="33677-155">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="33677-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="33677-156">-SyncGroupName</span></span>
<span data-ttu-id="33677-157">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="33677-157">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="33677-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33677-158">-Confirm</span></span>
<span data-ttu-id="33677-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33677-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33677-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33677-160">-WhatIf</span></span>
<span data-ttu-id="33677-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33677-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33677-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33677-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33677-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33677-163">CommonParameters</span></span>
<span data-ttu-id="33677-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33677-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33677-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33677-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33677-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33677-166">INPUTS</span></span>

### <span data-ttu-id="33677-167">System. String</span><span class="sxs-lookup"><span data-stu-id="33677-167">System.String</span></span>

### <span data-ttu-id="33677-168">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33677-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="33677-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33677-169">OUTPUTS</span></span>

### <span data-ttu-id="33677-170">System. void</span><span class="sxs-lookup"><span data-stu-id="33677-170">System.Void</span></span>

## <span data-ttu-id="33677-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="33677-171">NOTES</span></span>

## <span data-ttu-id="33677-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33677-172">RELATED LINKS</span></span>
