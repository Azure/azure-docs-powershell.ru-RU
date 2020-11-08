---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248624"
---
# <span data-ttu-id="5eaeb-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="5eaeb-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="5eaeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5eaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="5eaeb-103">Перезапускает репликацию для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="5eaeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5eaeb-104">SYNTAX</span></span>

### <span data-ttu-id="5eaeb-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5eaeb-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5eaeb-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="5eaeb-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5eaeb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-107">DESCRIPTION</span></span>
<span data-ttu-id="5eaeb-108">Командлет Restart-AzMigrateServerReplication восстанавливает репликацию для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="5eaeb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-109">EXAMPLES</span></span>

### <span data-ttu-id="5eaeb-110">Пример 1: по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-110">Example 1: By id.</span></span>
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

<span data-ttu-id="5eaeb-111">По идентификатору.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-111">By id.</span></span>

### <span data-ttu-id="5eaeb-112">Пример 2: по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="5eaeb-112">Example 2: By Input Object</span></span>
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

<span data-ttu-id="5eaeb-113">По объекту ввода.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-113">By Input Object.</span></span>

## <span data-ttu-id="5eaeb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-114">PARAMETERS</span></span>

### <span data-ttu-id="5eaeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eaeb-115">-DefaultProfile</span></span>
<span data-ttu-id="5eaeb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eaeb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eaeb-117">-InputObject</span></span>
<span data-ttu-id="5eaeb-118">Указывает объект Machine сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="5eaeb-119">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5eaeb-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eaeb-120">-SubscriptionId</span></span>
<span data-ttu-id="5eaeb-121">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5eaeb-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5eaeb-122">-TargetObjectID</span></span>
<span data-ttu-id="5eaeb-123">Указывает сервер replcating, для которого должна быть инициирована повторная синхронизация.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="5eaeb-124">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5eaeb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eaeb-125">CommonParameters</span></span>
<span data-ttu-id="5eaeb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eaeb-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eaeb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eaeb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5eaeb-128">INPUTS</span></span>

## <span data-ttu-id="5eaeb-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-129">OUTPUTS</span></span>

### <span data-ttu-id="5eaeb-130">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="5eaeb-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5eaeb-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5eaeb-131">NOTES</span></span>

<span data-ttu-id="5eaeb-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-132">ALIASES</span></span>

<span data-ttu-id="5eaeb-133">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eaeb-134">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eaeb-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eaeb-136">INPUTOBJECT <IMigrationItem> : определяет объект компьютера, на котором находится сервер репликации.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="5eaeb-137">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="5eaeb-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5eaeb-138">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5eaeb-139">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5eaeb-140">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5eaeb-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="5eaeb-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5eaeb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eaeb-142">RELATED LINKS</span></span>

