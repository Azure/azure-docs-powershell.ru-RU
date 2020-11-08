---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
ms.openlocfilehash: d66c21c33065fa1e142f38acbd3ef7971a7489dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248876"
---
# <span data-ttu-id="67c9e-101">Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="67c9e-101">Get-AzMigrateServerReplication</span></span>

## <span data-ttu-id="67c9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="67c9e-103">Извлекает сведения о сервере репликации.</span><span class="sxs-lookup"><span data-stu-id="67c9e-103">Retrieves the details of the replicating server.</span></span>

## <span data-ttu-id="67c9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67c9e-104">SYNTAX</span></span>

### <span data-ttu-id="67c9e-105">ListByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67c9e-105">ListByName (Default)</span></span>
```
Get-AzMigrateServerReplication -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67c9e-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="67c9e-106">GetByInputObject</span></span>
```
Get-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67c9e-107">GetBySDSID</span><span class="sxs-lookup"><span data-stu-id="67c9e-107">GetBySDSID</span></span>
```
Get-AzMigrateServerReplication -DiscoveredMachineId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67c9e-108">GetBySRSID</span><span class="sxs-lookup"><span data-stu-id="67c9e-108">GetBySRSID</span></span>
```
Get-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67c9e-109">ListById</span><span class="sxs-lookup"><span data-stu-id="67c9e-109">ListById</span></span>
```
Get-AzMigrateServerReplication -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="67c9e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67c9e-110">DESCRIPTION</span></span>
<span data-ttu-id="67c9e-111">Командлет Get-AzMigrateServerReplication извлекает объект для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="67c9e-111">The Get-AzMigrateServerReplication cmdlet retrieves the object for the replicating server.</span></span>

## <span data-ttu-id="67c9e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67c9e-112">EXAMPLES</span></span>

### <span data-ttu-id="67c9e-113">Пример 1: получение сведений по идентификатору</span><span class="sxs-lookup"><span data-stu-id="67c9e-113">Example 1: Get details by id</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="67c9e-114">Получить по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="67c9e-114">Get by id.</span></span>

### <span data-ttu-id="67c9e-115">Пример 2: список всех в Project по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="67c9e-115">Example 2: List all in project by id.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupID /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020 -ProjectID "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Migrate/MigrateProjects/AzMigrateTestProjectPWSH"

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="67c9e-116">Список всех.</span><span class="sxs-lookup"><span data-stu-id="67c9e-116">List all.</span></span>

### <span data-ttu-id="67c9e-117">Пример 2: список всех в Project по имени.</span><span class="sxs-lookup"><span data-stu-id="67c9e-117">Example 2: List all in project by name.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupName azmigratepwshtestasr13072020 -ProjectName AzMigrateTestProjectPWSH

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="67c9e-118">Список всех.</span><span class="sxs-lookup"><span data-stu-id="67c9e-118">List all.</span></span>

## <span data-ttu-id="67c9e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67c9e-119">PARAMETERS</span></span>

### <span data-ttu-id="67c9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c9e-120">-DefaultProfile</span></span>
<span data-ttu-id="67c9e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67c9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c9e-122">-DiscoveredMachineId</span><span class="sxs-lookup"><span data-stu-id="67c9e-122">-DiscoveredMachineId</span></span>
<span data-ttu-id="67c9e-123">Указывает ИД компьютера обнаруженного сервера.</span><span class="sxs-lookup"><span data-stu-id="67c9e-123">Specifies the machine ID of the discovered server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySDSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="67c9e-124">-Filter</span></span>
<span data-ttu-id="67c9e-125">Параметры фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="67c9e-125">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c9e-126">-InputObject</span></span>
<span data-ttu-id="67c9e-127">Указывает объект Machine сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="67c9e-127">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="67c9e-128">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="67c9e-128">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-129">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="67c9e-129">-ProjectID</span></span>
<span data-ttu-id="67c9e-130">Задает проект миграции Azure, в котором реплицируются серверы.</span><span class="sxs-lookup"><span data-stu-id="67c9e-130">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-131">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="67c9e-131">-ProjectName</span></span>
<span data-ttu-id="67c9e-132">Указывает проект миграции Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="67c9e-132">Specifies the Azure Migrate project  in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-133">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="67c9e-133">-ResourceGroupID</span></span>
<span data-ttu-id="67c9e-134">Указывает группу ресурсов для проекта миграции Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="67c9e-134">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c9e-135">-ResourceGroupName</span></span>
<span data-ttu-id="67c9e-136">Указывает группу ресурсов для проекта миграции Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="67c9e-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-137">-SkipToken</span><span class="sxs-lookup"><span data-stu-id="67c9e-137">-SkipToken</span></span>
<span data-ttu-id="67c9e-138">Маркер разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="67c9e-138">The pagination token.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67c9e-139">-SubscriptionId</span></span>
<span data-ttu-id="67c9e-140">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="67c9e-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="67c9e-141">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="67c9e-141">-TargetObjectID</span></span>
<span data-ttu-id="67c9e-142">Задает сервер репликации.</span><span class="sxs-lookup"><span data-stu-id="67c9e-142">Specifies the replicating server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySRSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c9e-143">CommonParameters</span></span>
<span data-ttu-id="67c9e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67c9e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c9e-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67c9e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c9e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67c9e-146">INPUTS</span></span>

## <span data-ttu-id="67c9e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67c9e-147">OUTPUTS</span></span>

### <span data-ttu-id="67c9e-148">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IMigrationItem</span><span class="sxs-lookup"><span data-stu-id="67c9e-148">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span></span>

## <span data-ttu-id="67c9e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="67c9e-149">NOTES</span></span>

<span data-ttu-id="67c9e-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="67c9e-150">ALIASES</span></span>

<span data-ttu-id="67c9e-151">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="67c9e-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67c9e-152">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67c9e-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67c9e-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67c9e-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67c9e-154">INPUTOBJECT <IMigrationItem> : определяет объект компьютера, на котором находится сервер репликации.</span><span class="sxs-lookup"><span data-stu-id="67c9e-154">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="67c9e-155">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="67c9e-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="67c9e-156">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="67c9e-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="67c9e-157">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="67c9e-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="67c9e-158">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="67c9e-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="67c9e-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="67c9e-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="67c9e-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67c9e-160">RELATED LINKS</span></span>

