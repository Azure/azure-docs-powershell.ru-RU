---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247314"
---
# <span data-ttu-id="3e959-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="3e959-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="3e959-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e959-102">SYNOPSIS</span></span>
<span data-ttu-id="3e959-103">Запускает репликацию для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="3e959-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="3e959-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e959-104">SYNTAX</span></span>

### <span data-ttu-id="3e959-105">ByIdDefaultUser (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e959-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e959-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="3e959-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e959-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="3e959-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e959-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="3e959-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e959-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e959-109">DESCRIPTION</span></span>
<span data-ttu-id="3e959-110">Командлет New-AzMigrateServerReplication запускает репликацию для определенного обнаруженного сервера в проекте миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="3e959-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="3e959-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e959-111">EXAMPLES</span></span>

### <span data-ttu-id="3e959-112">Пример 1: когда есть только диск ОС</span><span class="sxs-lookup"><span data-stu-id="3e959-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="3e959-113">Это относится к ситуации, когда есть только один диск, который должен быть защищен.</span><span class="sxs-lookup"><span data-stu-id="3e959-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="3e959-114">Пример 2: если у вас несколько дисков</span><span class="sxs-lookup"><span data-stu-id="3e959-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="3e959-115">Это происходит для сценария, если требуется защитить несколько дисков.</span><span class="sxs-lookup"><span data-stu-id="3e959-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="3e959-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e959-116">PARAMETERS</span></span>

### <span data-ttu-id="3e959-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e959-117">-DefaultProfile</span></span>
<span data-ttu-id="3e959-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e959-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e959-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="3e959-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="3e959-120">Указывает используемый дисковый encyption.</span><span class="sxs-lookup"><span data-stu-id="3e959-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="3e959-121">-DiskToInclude</span></span>
<span data-ttu-id="3e959-122">Указывает диски исходного сервера, которые будут включены в репликацию.</span><span class="sxs-lookup"><span data-stu-id="3e959-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="3e959-123">Для конструирования ознакомьтесь с разделом "Заметки" для свойств DISKTOINCLUDE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e959-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="3e959-124">-DiskType</span></span>
<span data-ttu-id="3e959-125">Указывает тип дисков, которые будут использоваться для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3e959-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e959-126">-InputObject</span></span>
<span data-ttu-id="3e959-127">Указывает обнаруженный сервер для миграции.</span><span class="sxs-lookup"><span data-stu-id="3e959-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="3e959-128">Объект сервера можно получить с помощью командлета Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="3e959-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="3e959-129">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e959-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3e959-130">-LicenseType</span></span>
<span data-ttu-id="3e959-131">Указывает, применимо ли гибридное преимущество Azure для миграции исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="3e959-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="3e959-132">-MachineId</span></span>
<span data-ttu-id="3e959-133">Указывает ИД компьютера для обнаруженного сервера, который требуется перенести.</span><span class="sxs-lookup"><span data-stu-id="3e959-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="3e959-134">-OSDiskID</span></span>
<span data-ttu-id="3e959-135">Указывает диск операционной системы для исходного сервера, который требуется перенести.</span><span class="sxs-lookup"><span data-stu-id="3e959-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e959-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="3e959-136">-PerformAutoResync</span></span>
<span data-ttu-id="3e959-137">Указывает, будет ли репликация автоматически восстановлена при отслеживании изменений для исходного сервера в разделе Replication.</span><span class="sxs-lookup"><span data-stu-id="3e959-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="3e959-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e959-138">-SubscriptionId</span></span>
<span data-ttu-id="3e959-139">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3e959-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3e959-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e959-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="3e959-141">Указывает группу доступности, используемую для VM creationSpecifies, которая будет использоваться для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e959-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="3e959-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="3e959-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="3e959-143">Указывает зону доступности, используемую для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e959-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="3e959-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e959-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="3e959-145">Указывает учетную запись хранения, которая будет использоваться для диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="3e959-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="3e959-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="3e959-146">-TargetNetworkId</span></span>
<span data-ttu-id="3e959-147">Указывает идентификатор виртуальной сети в конечной подписке Azure, на которую необходимо выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="3e959-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="3e959-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3e959-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="3e959-149">Указывает идентификатор группы ресурсов в конечной подписке Azure, на которую необходимо выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="3e959-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="3e959-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="3e959-150">-TargetSubnetName</span></span>
<span data-ttu-id="3e959-151">Указывает имя подсети в целевом виртуальном Netowk, к которому требуется выполнить миграцию сервера.</span><span class="sxs-lookup"><span data-stu-id="3e959-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="3e959-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="3e959-152">-TargetVMName</span></span>
<span data-ttu-id="3e959-153">Указывает имя виртуальной машины Azure, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="3e959-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="3e959-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="3e959-154">-TargetVMSize</span></span>
<span data-ttu-id="3e959-155">Указывает конфигурацию виртуальной машины Azure, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="3e959-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="3e959-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="3e959-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="3e959-157">Идентификатор учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3e959-157">Account id.</span></span>

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

### <span data-ttu-id="3e959-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e959-158">CommonParameters</span></span>
<span data-ttu-id="3e959-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e959-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e959-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e959-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e959-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e959-161">INPUTS</span></span>

## <span data-ttu-id="3e959-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e959-162">OUTPUTS</span></span>

### <span data-ttu-id="3e959-163">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="3e959-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="3e959-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e959-164">NOTES</span></span>

<span data-ttu-id="3e959-165">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3e959-165">ALIASES</span></span>

<span data-ttu-id="3e959-166">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3e959-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e959-167">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e959-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e959-168">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e959-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e959-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: задает диски исходного сервера, которые будут включены в репликацию.</span><span class="sxs-lookup"><span data-stu-id="3e959-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="3e959-170">`DiskId <String>`: Идентификатор диска.</span><span class="sxs-lookup"><span data-stu-id="3e959-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="3e959-171">`IsOSDisk <String>`: Значение, указывающее, является ли диск диском операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3e959-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="3e959-172">`LogStorageAccountId <String>`: Идентификатор ARM учетной записи хранилища журнала.</span><span class="sxs-lookup"><span data-stu-id="3e959-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="3e959-173">`LogStorageAccountSasSecretName <String>`: Секретный ключ хранилища ключей учетной записи хранения журнала.</span><span class="sxs-lookup"><span data-stu-id="3e959-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="3e959-174">`[DiskEncryptionSetId <String>]`: Идентификатор ARM DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="3e959-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="3e959-175">`[DiskType <DiskAccountType?>]`: Тип диска.</span><span class="sxs-lookup"><span data-stu-id="3e959-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="3e959-176">INPUTOBJECT <IVMwareMachine> : определяет обнаруженный сервер для миграции.</span><span class="sxs-lookup"><span data-stu-id="3e959-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="3e959-177">Объект сервера можно получить с помощью командлета Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="3e959-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="3e959-178">`[GuestOSDetailOstype <String>]`: Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3e959-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="3e959-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e959-179">RELATED LINKS</span></span>

