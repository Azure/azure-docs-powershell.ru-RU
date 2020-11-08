---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248621"
---
# <span data-ttu-id="5089f-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="5089f-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="5089f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5089f-102">SYNOPSIS</span></span>
<span data-ttu-id="5089f-103">Обновляет целевые свойства для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="5089f-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="5089f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5089f-104">SYNTAX</span></span>

### <span data-ttu-id="5089f-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5089f-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5089f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="5089f-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5089f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5089f-107">DESCRIPTION</span></span>
<span data-ttu-id="5089f-108">Командлет Set-AzMigrateServerReplication обновляет целевые свойства сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="5089f-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="5089f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5089f-109">EXAMPLES</span></span>

### <span data-ttu-id="5089f-110">Пример 1: обновление по идентификатору</span><span class="sxs-lookup"><span data-stu-id="5089f-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="5089f-111">По идентификатору.</span><span class="sxs-lookup"><span data-stu-id="5089f-111">By id.</span></span>

## <span data-ttu-id="5089f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5089f-112">PARAMETERS</span></span>

### <span data-ttu-id="5089f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5089f-113">-DefaultProfile</span></span>
<span data-ttu-id="5089f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5089f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5089f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5089f-115">-InputObject</span></span>
<span data-ttu-id="5089f-116">Задает сервер репликации, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="5089f-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="5089f-117">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="5089f-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="5089f-118">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5089f-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5089f-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="5089f-119">-NicToUpdate</span></span>
<span data-ttu-id="5089f-120">Обновляет сетевую карту виртуальной машины Azure, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5089f-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="5089f-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NICTOUPDATE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5089f-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5089f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5089f-122">-SubscriptionId</span></span>
<span data-ttu-id="5089f-123">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="5089f-123">The subscription Id.</span></span>

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

### <span data-ttu-id="5089f-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5089f-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="5089f-125">Указывает группу доступности, используемую для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5089f-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="5089f-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="5089f-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="5089f-127">Указывает зону доступности, используемую для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5089f-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="5089f-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="5089f-128">-TargetNetworkId</span></span>
<span data-ttu-id="5089f-129">Обновление идентификатора виртуальной сети в конечной подписке Azure, в которую необходимо выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="5089f-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="5089f-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5089f-130">-TargetObjectID</span></span>
<span data-ttu-id="5089f-131">Указывает сервер replcating, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="5089f-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="5089f-132">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="5089f-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5089f-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="5089f-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="5089f-134">Обновляет идентификатор группы ресурсов в конечной подписке Azure, в которую необходимо выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="5089f-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="5089f-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="5089f-135">-TargetVMName</span></span>
<span data-ttu-id="5089f-136">Указывает сервер replcating, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="5089f-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="5089f-137">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="5089f-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5089f-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="5089f-138">-TargetVMSize</span></span>
<span data-ttu-id="5089f-139">Обновляет SKU виртуальной машины Azure, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5089f-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="5089f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5089f-140">CommonParameters</span></span>
<span data-ttu-id="5089f-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5089f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5089f-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5089f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5089f-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5089f-143">INPUTS</span></span>

## <span data-ttu-id="5089f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5089f-144">OUTPUTS</span></span>

### <span data-ttu-id="5089f-145">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="5089f-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5089f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="5089f-146">NOTES</span></span>

<span data-ttu-id="5089f-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5089f-147">ALIASES</span></span>

<span data-ttu-id="5089f-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5089f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5089f-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5089f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5089f-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5089f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5089f-151">INPUTOBJECT <IMigrationItem> : определяет сервер репликации, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="5089f-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="5089f-152">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="5089f-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="5089f-153">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="5089f-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5089f-154">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="5089f-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5089f-155">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="5089f-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5089f-156">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="5089f-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5089f-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="5089f-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="5089f-158">NICTOUPDATE <IVMwareCbtNicInput [] >: обновляет сетевую карту для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5089f-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="5089f-159">`IsPrimaryNic <String>`: Значение, указывающее, является ли это основной NIC.</span><span class="sxs-lookup"><span data-stu-id="5089f-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="5089f-160">`NicId <String>`: Идентификатор NIC.</span><span class="sxs-lookup"><span data-stu-id="5089f-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="5089f-161">`[IsSelectedForMigration <String>]`: Значение, указывающее, выбрано ли этот сетевой адаптер для миграции.</span><span class="sxs-lookup"><span data-stu-id="5089f-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="5089f-162">`[TargetStaticIPAddress <String>]`: Статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5089f-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="5089f-163">`[TargetSubnetName <String>]`: Имя целевой подсети.</span><span class="sxs-lookup"><span data-stu-id="5089f-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="5089f-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5089f-164">RELATED LINKS</span></span>

