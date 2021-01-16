---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412812"
---
# <span data-ttu-id="a75f1-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="a75f1-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="a75f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a75f1-103">Очистка тестовой миграции для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="a75f1-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="a75f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a75f1-104">SYNTAX</span></span>

### <span data-ttu-id="a75f1-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a75f1-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a75f1-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="a75f1-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a75f1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a75f1-107">DESCRIPTION</span></span>
<span data-ttu-id="a75f1-108">С Start-AzMigrateTestMigrationCleanup- инициируется очистка тестовой миграции для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="a75f1-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="a75f1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a75f1-109">EXAMPLES</span></span>

### <span data-ttu-id="a75f1-110">Пример 1. По компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a75f1-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="a75f1-111">По компьютеру.</span><span class="sxs-lookup"><span data-stu-id="a75f1-111">By machine id.</span></span>

### <span data-ttu-id="a75f1-112">Пример 2. По объекту ввода</span><span class="sxs-lookup"><span data-stu-id="a75f1-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="a75f1-113">По объекту ввода.</span><span class="sxs-lookup"><span data-stu-id="a75f1-113">By input object.</span></span>

## <span data-ttu-id="a75f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75f1-114">PARAMETERS</span></span>

### <span data-ttu-id="a75f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75f1-115">-DefaultProfile</span></span>
<span data-ttu-id="a75f1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a75f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a75f1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a75f1-117">-InputObject</span></span>
<span data-ttu-id="a75f1-118">Указывает сервер репликации, для которого нужно инициировать проверку миграции.</span><span class="sxs-lookup"><span data-stu-id="a75f1-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="a75f1-119">Объект сервера можно получить с помощью Get-AzMigrateServerReplication-Get-AzMigrateServerReplication Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a75f1-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a75f1-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a75f1-120">-SubscriptionId</span></span>
<span data-ttu-id="a75f1-121">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a75f1-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a75f1-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="a75f1-122">-TargetObjectID</span></span>
<span data-ttu-id="a75f1-123">Указывает сервер репликации, для которого нужно инициировать проверку миграции.</span><span class="sxs-lookup"><span data-stu-id="a75f1-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="a75f1-124">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="a75f1-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a75f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75f1-125">CommonParameters</span></span>
<span data-ttu-id="a75f1-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75f1-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a75f1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75f1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a75f1-128">INPUTS</span></span>

## <span data-ttu-id="a75f1-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a75f1-129">OUTPUTS</span></span>

### <span data-ttu-id="a75f1-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="a75f1-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a75f1-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a75f1-131">NOTES</span></span>

<span data-ttu-id="a75f1-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a75f1-132">ALIASES</span></span>

<span data-ttu-id="a75f1-133">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a75f1-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a75f1-134">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a75f1-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a75f1-135">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a75f1-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a75f1-136">INPUTOBJECT: сервер репликации, для которого нужно инициировать проверку <IMigrationItem> миграции.</span><span class="sxs-lookup"><span data-stu-id="a75f1-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="a75f1-137">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication-управления</span><span class="sxs-lookup"><span data-stu-id="a75f1-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="a75f1-138">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="a75f1-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a75f1-139">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="a75f1-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="a75f1-140">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="a75f1-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="a75f1-141">`[CurrentJobStartTime <DateTime?>]`: время начала задания.</span><span class="sxs-lookup"><span data-stu-id="a75f1-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="a75f1-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="a75f1-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="a75f1-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a75f1-143">RELATED LINKS</span></span>

