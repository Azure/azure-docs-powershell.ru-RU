---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505077"
---
# <span data-ttu-id="c3d82-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c3d82-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c3d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d82-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d82-103">Обновляет целевые свойства сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c3d82-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c3d82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c3d82-104">SYNTAX</span></span>

### <span data-ttu-id="c3d82-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3d82-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c3d82-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c3d82-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c3d82-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3d82-107">DESCRIPTION</span></span>
<span data-ttu-id="c3d82-108">Он Set-AzMigrateServerReplication обновляет целевые свойства сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c3d82-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c3d82-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c3d82-109">EXAMPLES</span></span>

### <span data-ttu-id="c3d82-110">Пример 1. Обновление по id</span><span class="sxs-lookup"><span data-stu-id="c3d82-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c3d82-111">По id.</span><span class="sxs-lookup"><span data-stu-id="c3d82-111">By id.</span></span>

## <span data-ttu-id="c3d82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3d82-112">PARAMETERS</span></span>

### <span data-ttu-id="c3d82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d82-113">-DefaultProfile</span></span>
<span data-ttu-id="c3d82-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d82-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d82-115">-InputObject</span></span>
<span data-ttu-id="c3d82-116">Указывает сервер репликации, для которого необходимо обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="c3d82-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c3d82-117">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="c3d82-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c3d82-118">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="c3d82-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d82-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="c3d82-119">-NicToUpdate</span></span>
<span data-ttu-id="c3d82-120">Обновляет NIC для создаемого azure VM.</span><span class="sxs-lookup"><span data-stu-id="c3d82-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="c3d82-121">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств NICTOUPDATE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c3d82-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d82-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3d82-122">-SubscriptionId</span></span>
<span data-ttu-id="c3d82-123">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="c3d82-123">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d82-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c3d82-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="c3d82-125">Определяет набор доступности, который будет использоваться для создания VM-2016.</span><span class="sxs-lookup"><span data-stu-id="c3d82-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="c3d82-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="c3d82-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="c3d82-127">Определяет зону доступности, которая будет использоваться для создания VM-2016.</span><span class="sxs-lookup"><span data-stu-id="c3d82-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="c3d82-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3d82-128">-TargetNetworkId</span></span>
<span data-ttu-id="c3d82-129">Обновляет виртуальный сетевой id в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="c3d82-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c3d82-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c3d82-130">-TargetObjectID</span></span>
<span data-ttu-id="c3d82-131">Указывает сервер, для которого требуется обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="c3d82-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c3d82-132">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="c3d82-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d82-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="c3d82-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="c3d82-134">Обновляет id группы ресурсов в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="c3d82-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c3d82-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="c3d82-135">-TargetVMName</span></span>
<span data-ttu-id="c3d82-136">Указывает сервер, для которого требуется обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="c3d82-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c3d82-137">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="c3d82-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c3d82-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="c3d82-138">-TargetVMSize</span></span>
<span data-ttu-id="c3d82-139">Обновляет SKU создаемого VM Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d82-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="c3d82-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d82-140">CommonParameters</span></span>
<span data-ttu-id="c3d82-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d82-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d82-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3d82-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d82-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d82-143">INPUTS</span></span>

## <span data-ttu-id="c3d82-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d82-144">OUTPUTS</span></span>

### <span data-ttu-id="c3d82-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c3d82-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c3d82-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c3d82-146">NOTES</span></span>

<span data-ttu-id="c3d82-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c3d82-147">ALIASES</span></span>

<span data-ttu-id="c3d82-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c3d82-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3d82-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c3d82-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3d82-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3d82-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3d82-151">INPUTOBJECT: сервер репликации, для которого <IMigrationItem> необходимо обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="c3d82-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="c3d82-152">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="c3d82-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c3d82-153">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="c3d82-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c3d82-154">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="c3d82-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c3d82-155">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="c3d82-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c3d82-156">`[CurrentJobStartTime <DateTime?>]`. Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="c3d82-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c3d82-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="c3d82-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="c3d82-158">NICTOUPDATE <IVMwareCbtNicInput[]>: обновление NIC для azure VM.</span><span class="sxs-lookup"><span data-stu-id="c3d82-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="c3d82-159">`IsPrimaryNic <String>`: Значение, указывающее, является ли это основной NIC.</span><span class="sxs-lookup"><span data-stu-id="c3d82-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="c3d82-160">`NicId <String>`: NIC Id.</span><span class="sxs-lookup"><span data-stu-id="c3d82-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="c3d82-161">`[IsSelectedForMigration <String>]`: Значение, указывающее, выбрана ли эта NIC для миграции.</span><span class="sxs-lookup"><span data-stu-id="c3d82-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="c3d82-162">`[TargetStaticIPAddress <String>]`: статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c3d82-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="c3d82-163">`[TargetSubnetName <String>]`: Имя целевой подсети.</span><span class="sxs-lookup"><span data-stu-id="c3d82-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="c3d82-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3d82-164">RELATED LINKS</span></span>

