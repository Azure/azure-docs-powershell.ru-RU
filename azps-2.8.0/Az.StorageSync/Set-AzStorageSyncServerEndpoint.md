---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904229"
---
# <span data-ttu-id="1e614-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e614-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="1e614-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e614-102">SYNOPSIS</span></span>
<span data-ttu-id="1e614-103">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="1e614-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="1e614-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e614-104">SYNTAX</span></span>

### <span data-ttu-id="1e614-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e614-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e614-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e614-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e614-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e614-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e614-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e614-108">DESCRIPTION</span></span>
<span data-ttu-id="1e614-109">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="1e614-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="1e614-110">В любое время можно изменить уровень облака и политики уровней в облаке.</span><span class="sxs-lookup"><span data-stu-id="1e614-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="1e614-111">Некоторые аспекты конечной точки сервера, например локальный путь, невозможно изменить после создания конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="1e614-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="1e614-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e614-112">EXAMPLES</span></span>

### <span data-ttu-id="1e614-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e614-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="1e614-114">В этом примере выполняются два действия: она задает новую политику уровня облака в указанной конечной точке сервера, которая направляет сервер на уровень всех файлов, к которым не обращались в течение последних 30 дней, а также отключает режим автономной передачи данных, который изначально был включен в этой конечной точке сервера при ее создании.</span><span class="sxs-lookup"><span data-stu-id="1e614-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="1e614-115">Автономная передача данных используется как часть взаимодействия со службами массовой миграции, например полем данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1e614-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="1e614-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e614-116">PARAMETERS</span></span>

### <span data-ttu-id="1e614-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e614-117">-AsJob</span></span>
<span data-ttu-id="1e614-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1e614-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e614-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="1e614-119">-CloudTiering</span></span>
<span data-ttu-id="1e614-120">Параметр уровня облака</span><span class="sxs-lookup"><span data-stu-id="1e614-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="1e614-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e614-121">-DefaultProfile</span></span>
<span data-ttu-id="1e614-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e614-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e614-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e614-123">-InputObject</span></span>
<span data-ttu-id="1e614-124">Объект SyncGroup, обычно передаваемый через параметр.</span><span class="sxs-lookup"><span data-stu-id="1e614-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1e614-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e614-125">-Name</span></span>
<span data-ttu-id="1e614-126">Имя ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1e614-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="1e614-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="1e614-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="1e614-128">Параметр данных, заполненный облаком</span><span class="sxs-lookup"><span data-stu-id="1e614-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="1e614-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e614-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e614-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e614-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="1e614-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e614-131">-ResourceId</span></span>
<span data-ttu-id="1e614-132">Идентификатор ресурса ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e614-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="1e614-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1e614-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="1e614-134">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1e614-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1e614-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1e614-135">-SyncGroupName</span></span>
<span data-ttu-id="1e614-136">Имя SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="1e614-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1e614-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="1e614-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="1e614-138">Уровни файлов, предшествующих дню, с параметрами</span><span class="sxs-lookup"><span data-stu-id="1e614-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="1e614-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="1e614-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="1e614-140">Параметр процента свободного места в томе</span><span class="sxs-lookup"><span data-stu-id="1e614-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="1e614-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e614-141">-Confirm</span></span>
<span data-ttu-id="1e614-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e614-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e614-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e614-143">-WhatIf</span></span>
<span data-ttu-id="1e614-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e614-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e614-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e614-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e614-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e614-146">CommonParameters</span></span>
<span data-ttu-id="1e614-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e614-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e614-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e614-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e614-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e614-149">INPUTS</span></span>

### <span data-ttu-id="1e614-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1e614-150">System.String</span></span>

### <span data-ttu-id="1e614-151">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e614-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1e614-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e614-152">OUTPUTS</span></span>

### <span data-ttu-id="1e614-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e614-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1e614-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e614-154">NOTES</span></span>

## <span data-ttu-id="1e614-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e614-155">RELATED LINKS</span></span>
