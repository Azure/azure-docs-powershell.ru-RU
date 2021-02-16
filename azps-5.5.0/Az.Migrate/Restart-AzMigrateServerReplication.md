---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219116"
---
# <span data-ttu-id="5d501-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="5d501-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="5d501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d501-102">SYNOPSIS</span></span>
<span data-ttu-id="5d501-103">Перезапуск репликации для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="5d501-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="5d501-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d501-104">SYNTAX</span></span>

### <span data-ttu-id="5d501-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d501-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d501-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="5d501-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5d501-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d501-107">DESCRIPTION</span></span>
<span data-ttu-id="5d501-108">Он Restart-AzMigrateServerReplication восстановить репликацию для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="5d501-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="5d501-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d501-109">EXAMPLES</span></span>

### <span data-ttu-id="5d501-110">Пример 1. По id.</span><span class="sxs-lookup"><span data-stu-id="5d501-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="5d501-111">По id.</span><span class="sxs-lookup"><span data-stu-id="5d501-111">By id.</span></span>

### <span data-ttu-id="5d501-112">Пример 2. По объекту input</span><span class="sxs-lookup"><span data-stu-id="5d501-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="5d501-113">По объекту input.</span><span class="sxs-lookup"><span data-stu-id="5d501-113">By Input Object.</span></span>

## <span data-ttu-id="5d501-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d501-114">PARAMETERS</span></span>

### <span data-ttu-id="5d501-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d501-115">-DefaultProfile</span></span>
<span data-ttu-id="5d501-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d501-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d501-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d501-117">-InputObject</span></span>
<span data-ttu-id="5d501-118">Определяет машинный объект сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="5d501-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="5d501-119">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="5d501-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d501-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d501-120">-SubscriptionId</span></span>
<span data-ttu-id="5d501-121">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5d501-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5d501-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5d501-122">-TargetObjectID</span></span>
<span data-ttu-id="5d501-123">Указывает реплицирующий сервер, для которого нужно инициировать повторную проверку.</span><span class="sxs-lookup"><span data-stu-id="5d501-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="5d501-124">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="5d501-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5d501-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d501-125">CommonParameters</span></span>
<span data-ttu-id="5d501-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d501-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d501-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d501-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d501-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d501-128">INPUTS</span></span>

## <span data-ttu-id="5d501-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d501-129">OUTPUTS</span></span>

### <span data-ttu-id="5d501-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="5d501-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5d501-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d501-131">NOTES</span></span>

<span data-ttu-id="5d501-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5d501-132">ALIASES</span></span>

<span data-ttu-id="5d501-133">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5d501-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d501-134">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5d501-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d501-135">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d501-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d501-136">INPUTOBJECT: <IMigrationItem> определяет машинный объект сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="5d501-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="5d501-137">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="5d501-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5d501-138">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="5d501-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5d501-139">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="5d501-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5d501-140">`[CurrentJobStartTime <DateTime?>]`: время начала задания.</span><span class="sxs-lookup"><span data-stu-id="5d501-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5d501-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="5d501-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5d501-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d501-142">RELATED LINKS</span></span>

