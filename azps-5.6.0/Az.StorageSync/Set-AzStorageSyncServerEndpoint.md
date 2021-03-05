---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 65df82b189442a32738e445a1b48093c18816bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974003"
---
# <span data-ttu-id="61e75-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="61e75-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="61e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e75-102">SYNOPSIS</span></span>
<span data-ttu-id="61e75-103">Эта команда позволяет вносить изменения в настраиваемые параметры конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="61e75-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="61e75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61e75-104">SYNTAX</span></span>

### <span data-ttu-id="61e75-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61e75-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e75-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e75-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e75-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e75-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e75-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61e75-108">DESCRIPTION</span></span>
<span data-ttu-id="61e75-109">Эта команда позволяет вносить изменения в настраиваемые параметры конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="61e75-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="61e75-110">Например, можно в любое время изменить политики уровня облачных и облачных уровней.</span><span class="sxs-lookup"><span data-stu-id="61e75-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="61e75-111">Некоторые аспекты конечной точки сервера, например локальный путь, невозможно изменить после создания конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="61e75-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="61e75-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61e75-112">EXAMPLES</span></span>

### <span data-ttu-id="61e75-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61e75-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="61e75-114">В этом примере выполняются два действия: задана новая политика уровня облака для указанной конечной точки сервера, которая переводит сервер на уровень всех файлов, которые не были доступны за последние 30 дней, а также отключает автономный режим передачи данных, который изначально был включен на этой конечной точке сервера при его создании.</span><span class="sxs-lookup"><span data-stu-id="61e75-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="61e75-115">Автономный перенос данных используется для обеспечения связи со службами массовой миграции, такими как поле данных Azure.</span><span class="sxs-lookup"><span data-stu-id="61e75-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="61e75-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61e75-116">PARAMETERS</span></span>

### <span data-ttu-id="61e75-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61e75-117">-AsJob</span></span>
<span data-ttu-id="61e75-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61e75-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61e75-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="61e75-119">-CloudTiering</span></span>
<span data-ttu-id="61e75-120">Параметр уровня облака</span><span class="sxs-lookup"><span data-stu-id="61e75-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="61e75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e75-121">-DefaultProfile</span></span>
<span data-ttu-id="61e75-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61e75-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e75-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e75-123">-InputObject</span></span>
<span data-ttu-id="61e75-124">Объект SyncGroup, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="61e75-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e75-125">-Name</span><span class="sxs-lookup"><span data-stu-id="61e75-125">-Name</span></span>
<span data-ttu-id="61e75-126">Имя сервераEndpoint.</span><span class="sxs-lookup"><span data-stu-id="61e75-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e75-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="61e75-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="61e75-128">Параметр облачных данных</span><span class="sxs-lookup"><span data-stu-id="61e75-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="61e75-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="61e75-129">-localCacheMode</span></span>
<span data-ttu-id="61e75-130">Параметр режима локального кэша</span><span class="sxs-lookup"><span data-stu-id="61e75-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="61e75-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e75-131">-ResourceGroupName</span></span>
<span data-ttu-id="61e75-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61e75-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="61e75-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61e75-133">-ResourceId</span></span>
<span data-ttu-id="61e75-134">ИД ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="61e75-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e75-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="61e75-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="61e75-136">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="61e75-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="61e75-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="61e75-137">-SyncGroupName</span></span>
<span data-ttu-id="61e75-138">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="61e75-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="61e75-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="61e75-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="61e75-140">Параметр "Файлы с более старыми уровнями, чем дни"</span><span class="sxs-lookup"><span data-stu-id="61e75-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="61e75-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="61e75-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="61e75-142">Параметр Volume Free Space Percent</span><span class="sxs-lookup"><span data-stu-id="61e75-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="61e75-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e75-143">-Confirm</span></span>
<span data-ttu-id="61e75-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61e75-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e75-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e75-145">-WhatIf</span></span>
<span data-ttu-id="61e75-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e75-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61e75-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61e75-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e75-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e75-148">CommonParameters</span></span>
<span data-ttu-id="61e75-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e75-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e75-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e75-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e75-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61e75-151">INPUTS</span></span>

### <span data-ttu-id="61e75-152">System.String</span><span class="sxs-lookup"><span data-stu-id="61e75-152">System.String</span></span>

### <span data-ttu-id="61e75-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="61e75-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="61e75-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61e75-154">OUTPUTS</span></span>

### <span data-ttu-id="61e75-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="61e75-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="61e75-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61e75-156">NOTES</span></span>

## <span data-ttu-id="61e75-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61e75-157">RELATED LINKS</span></span>
