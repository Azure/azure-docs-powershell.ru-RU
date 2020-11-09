---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318212"
---
# <span data-ttu-id="32328-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32328-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="32328-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32328-102">SYNOPSIS</span></span>
<span data-ttu-id="32328-103">Эта команда создает новую конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="32328-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="32328-104">Это позволяет заданному пути на сервере запустить синхронизацию файлов с другими конечными точками в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="32328-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="32328-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32328-105">SYNTAX</span></span>

### <span data-ttu-id="32328-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32328-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32328-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32328-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32328-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="32328-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32328-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32328-109">DESCRIPTION</span></span>
<span data-ttu-id="32328-110">Эта команда создает новую конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="32328-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="32328-111">Это позволяет заданному пути на сервере запустить синхронизацию файлов с другими конечными точками в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="32328-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="32328-112">Если в группе синхронизация уже есть файлы, а в этом новом расположении есть файлы, процесс выверки попытается определить, находятся ли файлы в том же папке, что и в других конечных точках.</span><span class="sxs-lookup"><span data-stu-id="32328-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="32328-113">Эти пространства имен будут объединяться и выверять, что предотвращает конфликт файлов.</span><span class="sxs-lookup"><span data-stu-id="32328-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="32328-114">Если в других конечных точках сервера есть файлы, лучше всего начать с пустого местоположения на этом сервере, чтобы файлы из облака переходили на сервер в автоматическом процессе, именуемом быстрым восстановлением после аварии.</span><span class="sxs-lookup"><span data-stu-id="32328-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="32328-115">Метаданные пространства имен будут сначала синхронизированы, а затем будет загружен поток данных каждого файла.</span><span class="sxs-lookup"><span data-stu-id="32328-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="32328-116">Если файл, запрошенный пользователем или приложением, выходит из порядка загрузки, этот файл будет отозван с приоритетом для удовлетворения запроса на доступ.</span><span class="sxs-lookup"><span data-stu-id="32328-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="32328-117">Вы также можете использовать уровень облака на этой конечной точке сервера, чтобы определить, должна ли эта конечная точка стать кэшем полного набора файлов из облака.</span><span class="sxs-lookup"><span data-stu-id="32328-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="32328-118">Если используется облачное tiering, скачивание содержимого файла будет остановлено в точке, определенной политикой уровня облака, которую вы можете настроить.</span><span class="sxs-lookup"><span data-stu-id="32328-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="32328-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32328-119">EXAMPLES</span></span>

### <span data-ttu-id="32328-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32328-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="32328-121">Эта команда создает новую конечную точку сервера на зарегистрированном сервере и вставляет ее в группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="32328-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="32328-122">Таким образом, она является частью топологии других конечных точек и метаданных файла, и содержимое сразу же начнет синхронизироваться между всеми местами, на которые ссылаются как конечные точки в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="32328-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="32328-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32328-123">PARAMETERS</span></span>

### <span data-ttu-id="32328-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32328-124">-AsJob</span></span>
<span data-ttu-id="32328-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32328-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32328-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="32328-126">-CloudTiering</span></span>
<span data-ttu-id="32328-127">Параметр уровня облака</span><span class="sxs-lookup"><span data-stu-id="32328-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="32328-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32328-128">-DefaultProfile</span></span>
<span data-ttu-id="32328-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32328-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32328-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32328-130">-Name</span></span>
<span data-ttu-id="32328-131">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="32328-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32328-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="32328-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="32328-133">Параметр данных, заполненный облаком</span><span class="sxs-lookup"><span data-stu-id="32328-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="32328-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="32328-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="32328-135">Параметр URI общего доступа к файлам данных в облаке</span><span class="sxs-lookup"><span data-stu-id="32328-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="32328-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="32328-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="32328-137">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="32328-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="32328-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="32328-138">-localCacheMode</span></span>
<span data-ttu-id="32328-139">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="32328-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="32328-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32328-140">-ParentObject</span></span>
<span data-ttu-id="32328-141">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="32328-141">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32328-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32328-142">-ParentResourceId</span></span>
<span data-ttu-id="32328-143">Идентификатор родительского ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="32328-143">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32328-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32328-144">-ResourceGroupName</span></span>
<span data-ttu-id="32328-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32328-145">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32328-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="32328-146">-ServerLocalPath</span></span>
<span data-ttu-id="32328-147">Параметр "локальный путь сервера"</span><span class="sxs-lookup"><span data-stu-id="32328-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="32328-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="32328-148">-ServerResourceId</span></span>
<span data-ttu-id="32328-149">Идентификатор ресурса RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="32328-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="32328-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="32328-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="32328-151">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="32328-151">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32328-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="32328-152">-SyncGroupName</span></span>
<span data-ttu-id="32328-153">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="32328-153">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32328-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="32328-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="32328-155">Уровни файлов, предшествующих дню, с параметрами</span><span class="sxs-lookup"><span data-stu-id="32328-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="32328-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="32328-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="32328-157">Параметр процента свободного места в томе</span><span class="sxs-lookup"><span data-stu-id="32328-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="32328-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32328-158">-Confirm</span></span>
<span data-ttu-id="32328-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32328-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32328-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32328-160">-WhatIf</span></span>
<span data-ttu-id="32328-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32328-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32328-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32328-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32328-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32328-163">CommonParameters</span></span>
<span data-ttu-id="32328-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32328-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32328-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32328-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32328-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32328-166">INPUTS</span></span>

### <span data-ttu-id="32328-167">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="32328-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="32328-168">System. String</span><span class="sxs-lookup"><span data-stu-id="32328-168">System.String</span></span>

## <span data-ttu-id="32328-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32328-169">OUTPUTS</span></span>

### <span data-ttu-id="32328-170">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32328-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="32328-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="32328-171">NOTES</span></span>

## <span data-ttu-id="32328-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32328-172">RELATED LINKS</span></span>
