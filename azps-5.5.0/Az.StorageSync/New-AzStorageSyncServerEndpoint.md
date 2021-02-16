---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229732"
---
# <span data-ttu-id="0a873-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a873-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="0a873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a873-102">SYNOPSIS</span></span>
<span data-ttu-id="0a873-103">Эта команда создает конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="0a873-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0a873-104">Это позволяет заданный путь на сервере начать синхронизацию файлов с другими конечными точками в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0a873-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="0a873-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a873-105">SYNTAX</span></span>

### <span data-ttu-id="0a873-106">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a873-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a873-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a873-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a873-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a873-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a873-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a873-109">DESCRIPTION</span></span>
<span data-ttu-id="0a873-110">Эта команда создает конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="0a873-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0a873-111">Это позволяет заданный путь на сервере начать синхронизацию файлов с другими конечными точками в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0a873-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="0a873-112">Если в группе синхронизации уже имеются файлы из других конечных точек и это добавленное расположение также содержит файлы, будет предпринята попытка определить, совпадают ли файлы с папками на других конечных точках.</span><span class="sxs-lookup"><span data-stu-id="0a873-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="0a873-113">Пространства имен будут объединяться, а выверка помогает предотвратить файлы конфликтов.</span><span class="sxs-lookup"><span data-stu-id="0a873-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="0a873-114">Если есть файлы на других конечных точках сервера, зачастую лучше начать с пустого места на этом сервере, чтобы файлы из облака возвращались на сервер в автоматическом процессе, который называется быстрым аварийном восстановлением.</span><span class="sxs-lookup"><span data-stu-id="0a873-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="0a873-115">Сначала синхронизируются метаданные пространства имен, а затем загружается поток данных каждого файла.</span><span class="sxs-lookup"><span data-stu-id="0a873-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="0a873-116">Если файл запрашивается пользователем или приложением из-за заказа на скачивание, он отзывается с приоритетом для удовлетворения запроса на доступ.</span><span class="sxs-lookup"><span data-stu-id="0a873-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="0a873-117">При желании с помощью уровня облака на этой конечной точке сервера можно определить, должна ли эта конечная точка стать кэшом всего набора файлов из облака.</span><span class="sxs-lookup"><span data-stu-id="0a873-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="0a873-118">Если используется уровень облачного уровня, скачивание контента файла прекратится на этапе, задаемом политиками уровня облачных уровней.</span><span class="sxs-lookup"><span data-stu-id="0a873-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="0a873-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a873-119">EXAMPLES</span></span>

### <span data-ttu-id="0a873-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a873-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="0a873-121">Эта команда создает конечную точку сервера на зарегистрированном сервере и вставляет ее в группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0a873-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="0a873-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span><span class="sxs-lookup"><span data-stu-id="0a873-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="0a873-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a873-123">PARAMETERS</span></span>

### <span data-ttu-id="0a873-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a873-124">-AsJob</span></span>
<span data-ttu-id="0a873-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0a873-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a873-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="0a873-126">-CloudTiering</span></span>
<span data-ttu-id="0a873-127">Параметр уровня облака</span><span class="sxs-lookup"><span data-stu-id="0a873-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="0a873-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a873-128">-DefaultProfile</span></span>
<span data-ttu-id="0a873-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a873-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a873-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0a873-130">-Name</span></span>
<span data-ttu-id="0a873-131">Имя сервераEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0a873-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="0a873-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="0a873-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="0a873-133">Параметр облачных данных</span><span class="sxs-lookup"><span data-stu-id="0a873-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="0a873-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="0a873-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="0a873-135">Параметр URI для облачного файла данных (Share Uri)</span><span class="sxs-lookup"><span data-stu-id="0a873-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="0a873-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="0a873-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="0a873-137">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="0a873-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="0a873-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="0a873-138">-localCacheMode</span></span>
<span data-ttu-id="0a873-139">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="0a873-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="0a873-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a873-140">-ParentObject</span></span>
<span data-ttu-id="0a873-141">Объект SyncGroup, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="0a873-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0a873-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a873-142">-ParentResourceId</span></span>
<span data-ttu-id="0a873-143">ИД родительского ресурса SyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a873-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="0a873-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a873-144">-ResourceGroupName</span></span>
<span data-ttu-id="0a873-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a873-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a873-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="0a873-146">-ServerLocalPath</span></span>
<span data-ttu-id="0a873-147">Параметр локального пути сервера</span><span class="sxs-lookup"><span data-stu-id="0a873-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="0a873-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="0a873-148">-ServerResourceId</span></span>
<span data-ttu-id="0a873-149">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="0a873-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="0a873-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0a873-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="0a873-151">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0a873-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0a873-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0a873-152">-SyncGroupName</span></span>
<span data-ttu-id="0a873-153">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0a873-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0a873-154">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="0a873-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="0a873-155">Параметр "Файлы с более старыми уровнями, чем дни"</span><span class="sxs-lookup"><span data-stu-id="0a873-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="0a873-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="0a873-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="0a873-157">Параметр Volume Free Space Percent</span><span class="sxs-lookup"><span data-stu-id="0a873-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="0a873-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a873-158">-Confirm</span></span>
<span data-ttu-id="0a873-159">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0a873-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a873-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a873-160">-WhatIf</span></span>
<span data-ttu-id="0a873-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a873-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a873-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0a873-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a873-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a873-163">CommonParameters</span></span>
<span data-ttu-id="0a873-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a873-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a873-165">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a873-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a873-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a873-166">INPUTS</span></span>

### <span data-ttu-id="0a873-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a873-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0a873-168">System.String</span><span class="sxs-lookup"><span data-stu-id="0a873-168">System.String</span></span>

## <span data-ttu-id="0a873-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a873-169">OUTPUTS</span></span>

### <span data-ttu-id="0a873-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a873-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="0a873-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a873-171">NOTES</span></span>

## <span data-ttu-id="0a873-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a873-172">RELATED LINKS</span></span>
