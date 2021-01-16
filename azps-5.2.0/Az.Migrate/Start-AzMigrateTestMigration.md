---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412815"
---
# <span data-ttu-id="64142-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="64142-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="64142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64142-102">SYNOPSIS</span></span>
<span data-ttu-id="64142-103">Запускает тестовую миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="64142-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="64142-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64142-104">SYNTAX</span></span>

### <span data-ttu-id="64142-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64142-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64142-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="64142-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="64142-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64142-107">DESCRIPTION</span></span>
<span data-ttu-id="64142-108">Он Start-AzMigrateTestMigration инициирует тестовую миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="64142-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="64142-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64142-109">EXAMPLES</span></span>

### <span data-ttu-id="64142-110">Пример 1. По компьютеру.</span><span class="sxs-lookup"><span data-stu-id="64142-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="64142-111">По компьютеру.</span><span class="sxs-lookup"><span data-stu-id="64142-111">By machine id.</span></span>

### <span data-ttu-id="64142-112">Пример 2. По объекту ввода</span><span class="sxs-lookup"><span data-stu-id="64142-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="64142-113">По объекту ввода.</span><span class="sxs-lookup"><span data-stu-id="64142-113">By input object.</span></span>

## <span data-ttu-id="64142-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64142-114">PARAMETERS</span></span>

### <span data-ttu-id="64142-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64142-115">-DefaultProfile</span></span>
<span data-ttu-id="64142-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64142-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64142-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64142-117">-InputObject</span></span>
<span data-ttu-id="64142-118">Указывает сервер репликации, для которого нужно инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="64142-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="64142-119">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication..</span><span class="sxs-lookup"><span data-stu-id="64142-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="64142-120">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="64142-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64142-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64142-121">-SubscriptionId</span></span>
<span data-ttu-id="64142-122">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="64142-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="64142-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="64142-123">-TargetObjectID</span></span>
<span data-ttu-id="64142-124">Указывает сервер репликации, для которого нужно инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="64142-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="64142-125">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="64142-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="64142-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="64142-126">-TestNetworkID</span></span>
<span data-ttu-id="64142-127">Обновляет виртуальный сетевой id в рамках подписки Azure, используемой для тестовой миграции.</span><span class="sxs-lookup"><span data-stu-id="64142-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64142-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64142-128">CommonParameters</span></span>
<span data-ttu-id="64142-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64142-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64142-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64142-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64142-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64142-131">INPUTS</span></span>

## <span data-ttu-id="64142-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64142-132">OUTPUTS</span></span>

### <span data-ttu-id="64142-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="64142-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="64142-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64142-134">NOTES</span></span>

<span data-ttu-id="64142-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64142-135">ALIASES</span></span>

<span data-ttu-id="64142-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="64142-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64142-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="64142-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64142-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64142-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64142-139">INPUTOBJECT: сервер репликации, для которого нужно <IMigrationItem> инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="64142-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="64142-140">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication..</span><span class="sxs-lookup"><span data-stu-id="64142-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="64142-141">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="64142-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="64142-142">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="64142-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="64142-143">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="64142-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="64142-144">`[CurrentJobStartTime <DateTime?>]`: время начала задания.</span><span class="sxs-lookup"><span data-stu-id="64142-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="64142-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="64142-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="64142-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64142-146">RELATED LINKS</span></span>

