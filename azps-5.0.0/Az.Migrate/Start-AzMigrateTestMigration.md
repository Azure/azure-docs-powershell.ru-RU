---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248620"
---
# <span data-ttu-id="9f8b0-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="9f8b0-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="9f8b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8b0-103">Запускает тестовую миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="9f8b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f8b0-104">SYNTAX</span></span>

### <span data-ttu-id="9f8b0-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f8b0-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9f8b0-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="9f8b0-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9f8b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-107">DESCRIPTION</span></span>
<span data-ttu-id="9f8b0-108">Командлет Start-AzMigrateTestMigration инициирует тестовую миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="9f8b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-109">EXAMPLES</span></span>

### <span data-ttu-id="9f8b0-110">Пример 1: по идентификатору компьютера.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="9f8b0-111">По идентификатору компьютера.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-111">By machine id.</span></span>

### <span data-ttu-id="9f8b0-112">Пример 2: по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="9f8b0-112">Example 2: By input object</span></span>
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

<span data-ttu-id="9f8b0-113">По объекту ввода.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-113">By input object.</span></span>

## <span data-ttu-id="9f8b0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-114">PARAMETERS</span></span>

### <span data-ttu-id="9f8b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8b0-115">-DefaultProfile</span></span>
<span data-ttu-id="9f8b0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8b0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f8b0-117">-InputObject</span></span>
<span data-ttu-id="9f8b0-118">Задает сервер репликации, для которого необходимо инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="9f8b0-119">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="9f8b0-120">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f8b0-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f8b0-121">-SubscriptionId</span></span>
<span data-ttu-id="9f8b0-122">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9f8b0-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="9f8b0-123">-TargetObjectID</span></span>
<span data-ttu-id="9f8b0-124">Задает сервер репликации, для которого необходимо инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="9f8b0-125">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="9f8b0-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="9f8b0-126">-TestNetworkID</span></span>
<span data-ttu-id="9f8b0-127">Обновление идентификатора виртуальной сети в конечной подписке Azure для использования при тестировании миграции.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="9f8b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8b0-128">CommonParameters</span></span>
<span data-ttu-id="9f8b0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8b0-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f8b0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8b0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f8b0-131">INPUTS</span></span>

## <span data-ttu-id="9f8b0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-132">OUTPUTS</span></span>

### <span data-ttu-id="9f8b0-133">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="9f8b0-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="9f8b0-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f8b0-134">NOTES</span></span>

<span data-ttu-id="9f8b0-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-135">ALIASES</span></span>

<span data-ttu-id="9f8b0-136">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f8b0-137">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f8b0-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f8b0-139">INPUTOBJECT <IMigrationItem> : определяет сервер репликации, для которого необходимо инициировать тестовую миграцию.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="9f8b0-140">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="9f8b0-141">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="9f8b0-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="9f8b0-142">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="9f8b0-143">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="9f8b0-144">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="9f8b0-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="9f8b0-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="9f8b0-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f8b0-146">RELATED LINKS</span></span>

