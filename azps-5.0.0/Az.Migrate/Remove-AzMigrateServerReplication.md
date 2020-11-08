---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248627"
---
# <span data-ttu-id="02af2-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="02af2-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="02af2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02af2-102">SYNOPSIS</span></span>
<span data-ttu-id="02af2-103">Останавливает репликацию для перенесенного сервера.</span><span class="sxs-lookup"><span data-stu-id="02af2-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="02af2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02af2-104">SYNTAX</span></span>

### <span data-ttu-id="02af2-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02af2-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02af2-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="02af2-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="02af2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02af2-107">DESCRIPTION</span></span>
<span data-ttu-id="02af2-108">Командлет Remove-AzMigrateServerReplication останавливает репликацию для мигрировавшего сервера.</span><span class="sxs-lookup"><span data-stu-id="02af2-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="02af2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02af2-109">EXAMPLES</span></span>

### <span data-ttu-id="02af2-110">Пример 1: удаление по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="02af2-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="02af2-111">Повторная синхронизация по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="02af2-111">Resync by id.</span></span>

### <span data-ttu-id="02af2-112">Пример 2: удаление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="02af2-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="02af2-113">По имени.</span><span class="sxs-lookup"><span data-stu-id="02af2-113">By name.</span></span>

## <span data-ttu-id="02af2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02af2-114">PARAMETERS</span></span>

### <span data-ttu-id="02af2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02af2-115">-DefaultProfile</span></span>
<span data-ttu-id="02af2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02af2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02af2-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="02af2-117">-ForceRemove</span></span>
<span data-ttu-id="02af2-118">Указывает, нужно ли принудительно удалять репликацию.</span><span class="sxs-lookup"><span data-stu-id="02af2-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="02af2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02af2-119">-InputObject</span></span>
<span data-ttu-id="02af2-120">Указывает объект Machine сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="02af2-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="02af2-121">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="02af2-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02af2-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02af2-122">-SubscriptionId</span></span>
<span data-ttu-id="02af2-123">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="02af2-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="02af2-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="02af2-124">-TargetObjectID</span></span>
<span data-ttu-id="02af2-125">Указывает сервер replcating, для которого необходимо отключить replicatio.</span><span class="sxs-lookup"><span data-stu-id="02af2-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="02af2-126">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="02af2-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="02af2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02af2-127">CommonParameters</span></span>
<span data-ttu-id="02af2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02af2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02af2-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02af2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02af2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02af2-130">INPUTS</span></span>

## <span data-ttu-id="02af2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02af2-131">OUTPUTS</span></span>

### <span data-ttu-id="02af2-132">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="02af2-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="02af2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="02af2-133">NOTES</span></span>

<span data-ttu-id="02af2-134">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="02af2-134">ALIASES</span></span>

<span data-ttu-id="02af2-135">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="02af2-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02af2-136">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02af2-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02af2-137">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02af2-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02af2-138">INPUTOBJECT <IMigrationItem> : определяет объект компьютера, на котором находится сервер репликации.</span><span class="sxs-lookup"><span data-stu-id="02af2-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="02af2-139">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="02af2-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="02af2-140">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="02af2-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="02af2-141">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="02af2-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="02af2-142">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="02af2-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="02af2-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="02af2-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="02af2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02af2-144">RELATED LINKS</span></span>

