---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009587"
---
# <span data-ttu-id="cbf1f-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="cbf1f-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="cbf1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf1f-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf1f-103">Обновляет целевые свойства сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cbf1f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cbf1f-104">SYNTAX</span></span>

### <span data-ttu-id="cbf1f-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbf1f-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbf1f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="cbf1f-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cbf1f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbf1f-107">DESCRIPTION</span></span>
<span data-ttu-id="cbf1f-108">Он Set-AzMigrateServerReplication обновляет целевые свойства сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cbf1f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cbf1f-109">EXAMPLES</span></span>

### <span data-ttu-id="cbf1f-110">Пример 1. Обновление по id</span><span class="sxs-lookup"><span data-stu-id="cbf1f-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="cbf1f-111">По id.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-111">By id.</span></span>

## <span data-ttu-id="cbf1f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbf1f-112">PARAMETERS</span></span>

### <span data-ttu-id="cbf1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf1f-113">-DefaultProfile</span></span>
<span data-ttu-id="cbf1f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf1f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbf1f-115">-InputObject</span></span>
<span data-ttu-id="cbf1f-116">Указывает сервер репликации, для которого необходимо обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbf1f-117">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication..</span><span class="sxs-lookup"><span data-stu-id="cbf1f-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="cbf1f-118">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbf1f-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="cbf1f-119">-NicToUpdate</span></span>
<span data-ttu-id="cbf1f-120">Обновляет NIC для создаемого azure VM.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="cbf1f-121">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств NICTOUPDATE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbf1f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbf1f-122">-SubscriptionId</span></span>
<span data-ttu-id="cbf1f-123">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-123">The subscription Id.</span></span>

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

### <span data-ttu-id="cbf1f-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cbf1f-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="cbf1f-125">Определяет набор доступности, который будет использоваться для создания VM-2016.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="cbf1f-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="cbf1f-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="cbf1f-127">Определяет зону доступности, которая будет использоваться для создания VM-2016.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="cbf1f-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cbf1f-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="cbf1f-129">Указывает учетную запись хранения, которая будет использоваться для диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="cbf1f-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="cbf1f-130">-TargetNetworkId</span></span>
<span data-ttu-id="cbf1f-131">Обновляет виртуальный сетевой id в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cbf1f-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="cbf1f-132">-TargetObjectID</span></span>
<span data-ttu-id="cbf1f-133">Указывает сервер, для которого требуется обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbf1f-134">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cbf1f-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="cbf1f-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="cbf1f-136">Обновляет id группы ресурсов в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cbf1f-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="cbf1f-137">-TargetVMName</span></span>
<span data-ttu-id="cbf1f-138">Указывает сервер, для которого требуется обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cbf1f-139">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cbf1f-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="cbf1f-140">-TargetVMSize</span></span>
<span data-ttu-id="cbf1f-141">Обновляет SKU создаемого VM Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="cbf1f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf1f-142">CommonParameters</span></span>
<span data-ttu-id="cbf1f-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf1f-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbf1f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf1f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbf1f-145">INPUTS</span></span>

## <span data-ttu-id="cbf1f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cbf1f-146">OUTPUTS</span></span>

### <span data-ttu-id="cbf1f-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="cbf1f-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="cbf1f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cbf1f-148">NOTES</span></span>

<span data-ttu-id="cbf1f-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cbf1f-149">ALIASES</span></span>

<span data-ttu-id="cbf1f-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cbf1f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbf1f-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbf1f-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbf1f-153">INPUTOBJECT: сервер репликации, для которого <IMigrationItem> необходимо обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="cbf1f-154">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication..</span><span class="sxs-lookup"><span data-stu-id="cbf1f-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="cbf1f-155">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="cbf1f-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="cbf1f-156">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="cbf1f-157">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="cbf1f-158">`[CurrentJobStartTime <DateTime?>]`. Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="cbf1f-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="cbf1f-160">NICTOUPDATE <IVMwareCbtNicInput[]>: обновление NIC для azure VM.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="cbf1f-161">`IsPrimaryNic <String>`: Значение, указывающее, является ли это основной NIC.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="cbf1f-162">`NicId <String>`: NIC Id.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="cbf1f-163">`[IsSelectedForMigration <String>]`: Значение, указывающее, выбрана ли эта NIC для миграции.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="cbf1f-164">`[TargetStaticIPAddress <String>]`: статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="cbf1f-165">`[TargetSubnetName <String>]`: Имя целевой подсети.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="cbf1f-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbf1f-166">RELATED LINKS</span></span>

