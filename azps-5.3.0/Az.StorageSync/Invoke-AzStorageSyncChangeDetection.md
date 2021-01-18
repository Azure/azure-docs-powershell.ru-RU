---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505627"
---
# <span data-ttu-id="59694-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="59694-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="59694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59694-102">SYNOPSIS</span></span>
<span data-ttu-id="59694-103">Эту команду можно использовать для инициалов обнаружения изменений пространства имен вручную.</span><span class="sxs-lookup"><span data-stu-id="59694-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="59694-104">Его можно настроить для всей папки, вемеской папки или набора файлов.</span><span class="sxs-lookup"><span data-stu-id="59694-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="59694-105">Можно обнаружить не более 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="59694-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="59694-106">Если известна область изменений, ограничьте выполнение этой команды частями пространства имен, чтобы обнаружение изменений можно было быстро завершить в пределах 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="59694-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="59694-107">С Invoke-AzStorageSyncChangeDetection-файлами Azure не будут обнаружены следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="59694-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="59694-108">Удаленные файлы.</span><span class="sxs-lookup"><span data-stu-id="59694-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="59694-109">Файлы, которые перемещаются из папки "Поделиться".</span><span class="sxs-lookup"><span data-stu-id="59694-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="59694-110">Файлы, которые были удалены и созданы с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="59694-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="59694-111">Эти изменения будут обнаружены при запуске задания [обнаружения](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) изменений.</span><span class="sxs-lookup"><span data-stu-id="59694-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="59694-112">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59694-112">SYNTAX</span></span>

### <span data-ttu-id="59694-113">StringAndDirectoryParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59694-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59694-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="59694-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59694-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="59694-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59694-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="59694-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59694-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="59694-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59694-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="59694-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59694-119">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59694-119">DESCRIPTION</span></span>
<span data-ttu-id="59694-120">Время от времени служба Azure File Sync проверяет пространство имен в синхронизированной папке файлов Azure на наличие изменений, вносях в нее другими средствами, кроме синхронизации. Их нужно идентифицировать и в конечном итоге синхронизировать с подключенными серверами.</span><span class="sxs-lookup"><span data-stu-id="59694-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="59694-121">Эту команду можно использовать для инициалов обнаружения изменений пространства имен вручную.</span><span class="sxs-lookup"><span data-stu-id="59694-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="59694-122">Его можно настроить для всей папки, вемеской папки или набора файлов.</span><span class="sxs-lookup"><span data-stu-id="59694-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="59694-123">Если известна область изменений, ограничьте выполнение этой команды частями пространства имен, чтобы обнаружение изменений можно было быстро завершить в пределах 10 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="59694-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="59694-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59694-124">EXAMPLES</span></span>

### <span data-ttu-id="59694-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59694-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="59694-126">В этом примере обнаружение изменений в каталогах Data (Данные) и Reporting\Templates (Отчеты\Шаблоны) синхронизируются с файлами Azure.</span><span class="sxs-lookup"><span data-stu-id="59694-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="59694-127">Все пути находятся относительно корня пространства имен для файловой папки Azure.</span><span class="sxs-lookup"><span data-stu-id="59694-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="59694-128">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59694-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="59694-129">В этом примере для набора файлов, которые известны вызываемой команде, будет запускаться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="59694-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="59694-130">Необходимо, чтобы синхронизация файлов Azure также выявляла и синхронизировала эти изменения.</span><span class="sxs-lookup"><span data-stu-id="59694-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="59694-131">Пример 3</span><span class="sxs-lookup"><span data-stu-id="59694-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="59694-132">В этом примере обнаружение изменений запускается для каталога Examples и будет рекурсивно обнаруживать изменения в поднаправленных каталогах.</span><span class="sxs-lookup"><span data-stu-id="59694-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="59694-133">Имейте в виду, что если путь содержит более 10 000 элементов, он не будет работать.</span><span class="sxs-lookup"><span data-stu-id="59694-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="59694-134">Если путь содержит более 10 000 элементов, запустите команду в подгруппах пространства имен.</span><span class="sxs-lookup"><span data-stu-id="59694-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="59694-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59694-135">PARAMETERS</span></span>

### <span data-ttu-id="59694-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59694-136">-AsJob</span></span>
<span data-ttu-id="59694-137">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59694-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59694-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59694-138">-DefaultProfile</span></span>
<span data-ttu-id="59694-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59694-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59694-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="59694-140">-DirectoryPath</span></span>
<span data-ttu-id="59694-141">Каталог, в котором будет выполняться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="59694-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="59694-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59694-142">-InputObject</span></span>
<span data-ttu-id="59694-143">Объект CloudEndpoint обычно передается через параметр.</span><span class="sxs-lookup"><span data-stu-id="59694-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="59694-144">-Name</span><span class="sxs-lookup"><span data-stu-id="59694-144">-Name</span></span>
<span data-ttu-id="59694-145">Имя CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="59694-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="59694-146">Это GUID, а не удобное имя, отображаемая на портале.</span><span class="sxs-lookup"><span data-stu-id="59694-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="59694-147">Чтобы получить CloudEndpointName, воспользуйтесь Get-AzStorageSyncCloudEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="59694-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="59694-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59694-148">-PassThru</span></span>
<span data-ttu-id="59694-149">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="59694-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="59694-150">Если для параметра PassThru задан параметр PassThru, после успешного выполнения он будет записывать значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="59694-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="59694-151">-Path</span><span class="sxs-lookup"><span data-stu-id="59694-151">-Path</span></span>
<span data-ttu-id="59694-152">Путь, по котором будет выполняться обнаружение изменений.</span><span class="sxs-lookup"><span data-stu-id="59694-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="59694-153">-Recursive</span><span class="sxs-lookup"><span data-stu-id="59694-153">-Recursive</span></span>
<span data-ttu-id="59694-154">Указывает, является ли обнаружение изменений каталога рекурсивным.</span><span class="sxs-lookup"><span data-stu-id="59694-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="59694-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59694-155">-ResourceGroupName</span></span>
<span data-ttu-id="59694-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59694-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="59694-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59694-157">-ResourceId</span></span>
<span data-ttu-id="59694-158">CloudEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="59694-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="59694-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="59694-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="59694-160">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="59694-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="59694-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="59694-161">-SyncGroupName</span></span>
<span data-ttu-id="59694-162">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59694-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="59694-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59694-163">-Confirm</span></span>
<span data-ttu-id="59694-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59694-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59694-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59694-165">-WhatIf</span></span>
<span data-ttu-id="59694-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59694-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59694-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="59694-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59694-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59694-168">CommonParameters</span></span>
<span data-ttu-id="59694-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59694-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59694-170">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59694-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59694-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59694-171">INPUTS</span></span>

### <span data-ttu-id="59694-172">System.String</span><span class="sxs-lookup"><span data-stu-id="59694-172">System.String</span></span>

### <span data-ttu-id="59694-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="59694-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="59694-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59694-174">OUTPUTS</span></span>

### <span data-ttu-id="59694-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="59694-175">System.Void</span></span>

## <span data-ttu-id="59694-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59694-176">NOTES</span></span>

## <span data-ttu-id="59694-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59694-177">RELATED LINKS</span></span>
