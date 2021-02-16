---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219129"
---
# <span data-ttu-id="0ff75-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="0ff75-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="0ff75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff75-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff75-103">Остановка репликации для перенесенного сервера.</span><span class="sxs-lookup"><span data-stu-id="0ff75-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="0ff75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ff75-104">SYNTAX</span></span>

### <span data-ttu-id="0ff75-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ff75-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ff75-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="0ff75-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0ff75-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ff75-107">DESCRIPTION</span></span>
<span data-ttu-id="0ff75-108">Новый Remove-AzMigrateServerReplication останавливает репликацию для перенесенного сервера.</span><span class="sxs-lookup"><span data-stu-id="0ff75-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="0ff75-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ff75-109">EXAMPLES</span></span>

### <span data-ttu-id="0ff75-110">Пример 1. Удаление по id.</span><span class="sxs-lookup"><span data-stu-id="0ff75-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="0ff75-111">"Resync by id".</span><span class="sxs-lookup"><span data-stu-id="0ff75-111">Resync by id.</span></span>

### <span data-ttu-id="0ff75-112">Пример 2. Удаление объекта ввода</span><span class="sxs-lookup"><span data-stu-id="0ff75-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="0ff75-113">По имени.</span><span class="sxs-lookup"><span data-stu-id="0ff75-113">By name.</span></span>

## <span data-ttu-id="0ff75-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ff75-114">PARAMETERS</span></span>

### <span data-ttu-id="0ff75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff75-115">-DefaultProfile</span></span>
<span data-ttu-id="0ff75-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff75-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="0ff75-117">-ForceRemove</span></span>
<span data-ttu-id="0ff75-118">Указывает, требуется ли принудительно удалить репликацию.</span><span class="sxs-lookup"><span data-stu-id="0ff75-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="0ff75-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ff75-119">-InputObject</span></span>
<span data-ttu-id="0ff75-120">Определяет машинный объект сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="0ff75-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="0ff75-121">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="0ff75-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ff75-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ff75-122">-SubscriptionId</span></span>
<span data-ttu-id="0ff75-123">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff75-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0ff75-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="0ff75-124">-TargetObjectID</span></span>
<span data-ttu-id="0ff75-125">Указывает реплицирующий сервер, для которого требуется отключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="0ff75-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="0ff75-126">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="0ff75-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="0ff75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff75-127">CommonParameters</span></span>
<span data-ttu-id="0ff75-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff75-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ff75-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff75-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ff75-130">INPUTS</span></span>

## <span data-ttu-id="0ff75-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ff75-131">OUTPUTS</span></span>

### <span data-ttu-id="0ff75-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="0ff75-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="0ff75-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ff75-133">NOTES</span></span>

<span data-ttu-id="0ff75-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ff75-134">ALIASES</span></span>

<span data-ttu-id="0ff75-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0ff75-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ff75-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0ff75-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ff75-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ff75-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ff75-138">INPUTOBJECT: <IMigrationItem> определяет машинный объект сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="0ff75-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="0ff75-139">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="0ff75-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="0ff75-140">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="0ff75-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="0ff75-141">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="0ff75-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="0ff75-142">`[CurrentJobStartTime <DateTime?>]`: время начала задания.</span><span class="sxs-lookup"><span data-stu-id="0ff75-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="0ff75-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="0ff75-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="0ff75-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ff75-144">RELATED LINKS</span></span>

