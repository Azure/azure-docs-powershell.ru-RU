---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975731"
---
# <span data-ttu-id="802a8-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="802a8-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="802a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802a8-102">SYNOPSIS</span></span>
<span data-ttu-id="802a8-103">Запускает репликацию для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="802a8-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="802a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="802a8-104">SYNTAX</span></span>

### <span data-ttu-id="802a8-105">ByIdDefaultUser (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="802a8-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="802a8-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="802a8-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="802a8-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="802a8-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="802a8-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="802a8-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="802a8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="802a8-109">DESCRIPTION</span></span>
<span data-ttu-id="802a8-110">С New-AzMigrateServerReplication запускает репликацию для определенного сервера, обнаруженного в проекте миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="802a8-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="802a8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="802a8-111">EXAMPLES</span></span>

### <span data-ttu-id="802a8-112">Пример 1. При только на диске ОС</span><span class="sxs-lookup"><span data-stu-id="802a8-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="802a8-113">Это происходит в ситуации, когда нужно защитить только один диск.</span><span class="sxs-lookup"><span data-stu-id="802a8-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="802a8-114">Пример 2. Если у вас несколько дисков</span><span class="sxs-lookup"><span data-stu-id="802a8-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="802a8-115">Это происходит в ситуации, когда нужно защитить несколько дисков.</span><span class="sxs-lookup"><span data-stu-id="802a8-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="802a8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="802a8-116">PARAMETERS</span></span>

### <span data-ttu-id="802a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802a8-117">-DefaultProfile</span></span>
<span data-ttu-id="802a8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="802a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802a8-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="802a8-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="802a8-120">Определяет используемый набор encyption диска.</span><span class="sxs-lookup"><span data-stu-id="802a8-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="802a8-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="802a8-121">-DiskToInclude</span></span>
<span data-ttu-id="802a8-122">Определяет диски на сервере-источнике, которые нужно включить для репликации.</span><span class="sxs-lookup"><span data-stu-id="802a8-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="802a8-123">Чтобы создать таблицу, см. раздел "Заметки" для свойств DISKTOINCLUDE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="802a8-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="802a8-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="802a8-124">-DiskType</span></span>
<span data-ttu-id="802a8-125">Определяет тип дисков, используемых для Azure VM.</span><span class="sxs-lookup"><span data-stu-id="802a8-125">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="802a8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="802a8-126">-InputObject</span></span>
<span data-ttu-id="802a8-127">Определяет обнаруженный сервер, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="802a8-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="802a8-128">Объект сервера можно извлечь с помощью Get-AzMigrateServer..</span><span class="sxs-lookup"><span data-stu-id="802a8-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="802a8-129">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="802a8-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="802a8-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="802a8-130">-LicenseType</span></span>
<span data-ttu-id="802a8-131">Указывает, применимо ли гибридное преимущество Azure к переносимому серверу-источнику.</span><span class="sxs-lookup"><span data-stu-id="802a8-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="802a8-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="802a8-132">-MachineId</span></span>
<span data-ttu-id="802a8-133">Определяет машинный ИД обнаруженного сервера, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="802a8-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="802a8-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="802a8-134">-OSDiskID</span></span>
<span data-ttu-id="802a8-135">Определяет диск операционной системы для сервера-источника, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="802a8-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="802a8-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="802a8-136">-PerformAutoResync</span></span>
<span data-ttu-id="802a8-137">Указывает, будет ли репликация восстановлена автоматически в случае потери отслеживания изменений для исходных серверов в режиме репликации.</span><span class="sxs-lookup"><span data-stu-id="802a8-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="802a8-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="802a8-138">-SubscriptionId</span></span>
<span data-ttu-id="802a8-139">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="802a8-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="802a8-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="802a8-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="802a8-141">Набор доступности, используемый для создания VM, определяет набор доступности, который будет использоваться для создания VM.</span><span class="sxs-lookup"><span data-stu-id="802a8-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="802a8-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="802a8-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="802a8-143">Определяет зону доступности, которая будет использоваться для создания VM-2016.</span><span class="sxs-lookup"><span data-stu-id="802a8-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="802a8-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="802a8-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="802a8-145">Указывает учетную запись хранения, которая будет использоваться для диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="802a8-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="802a8-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="802a8-146">-TargetNetworkId</span></span>
<span data-ttu-id="802a8-147">Определяет виртуальный сетевой id в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="802a8-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="802a8-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="802a8-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="802a8-149">Определяет id группы ресурсов в рамках подписки Azure, в которую требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="802a8-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="802a8-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="802a8-150">-TargetSubnetName</span></span>
<span data-ttu-id="802a8-151">Имя подсети в пределах назначения Virtual Netowk, в который требуется перенести сервер.</span><span class="sxs-lookup"><span data-stu-id="802a8-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="802a8-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="802a8-152">-TargetVMName</span></span>
<span data-ttu-id="802a8-153">Указывает имя созда создаемого azure VM.</span><span class="sxs-lookup"><span data-stu-id="802a8-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="802a8-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="802a8-154">-TargetVMSize</span></span>
<span data-ttu-id="802a8-155">Указывает SKU созда создаемого VM Azure.</span><span class="sxs-lookup"><span data-stu-id="802a8-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="802a8-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="802a8-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="802a8-157">ИД учетной записи.</span><span class="sxs-lookup"><span data-stu-id="802a8-157">Account id.</span></span>

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

### <span data-ttu-id="802a8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802a8-158">CommonParameters</span></span>
<span data-ttu-id="802a8-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802a8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802a8-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="802a8-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802a8-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="802a8-161">INPUTS</span></span>

## <span data-ttu-id="802a8-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="802a8-162">OUTPUTS</span></span>

### <span data-ttu-id="802a8-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="802a8-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="802a8-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="802a8-164">NOTES</span></span>

<span data-ttu-id="802a8-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="802a8-165">ALIASES</span></span>

<span data-ttu-id="802a8-166">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="802a8-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="802a8-167">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="802a8-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="802a8-168">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="802a8-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="802a8-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: определяет диски на сервере-источнике, которые нужно включить для репликации.</span><span class="sxs-lookup"><span data-stu-id="802a8-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="802a8-170">`DiskId <String>`: ИД диска.</span><span class="sxs-lookup"><span data-stu-id="802a8-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="802a8-171">`IsOSDisk <String>`: значение, указывающее, является ли диск ОС диском.</span><span class="sxs-lookup"><span data-stu-id="802a8-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="802a8-172">`LogStorageAccountId <String>`: учетная запись хранения журнала, ARM ИД.</span><span class="sxs-lookup"><span data-stu-id="802a8-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="802a8-173">`LogStorageAccountSasSecretName <String>`: key vault secret name of the log storage account.</span><span class="sxs-lookup"><span data-stu-id="802a8-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="802a8-174">`[DiskEncryptionSetId <String>]`: DiskEncryptionSet ARM ID.</span><span class="sxs-lookup"><span data-stu-id="802a8-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="802a8-175">`[DiskType <DiskAccountType?>]`Тип диска.</span><span class="sxs-lookup"><span data-stu-id="802a8-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="802a8-176">INPUTOBJECT: <IVMwareMachine> определяет обнаруженный сервер, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="802a8-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="802a8-177">Объект сервера можно извлечь с помощью Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="802a8-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="802a8-178">`[GuestOSDetailOstype <String>]`: Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="802a8-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="802a8-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="802a8-179">RELATED LINKS</span></span>

