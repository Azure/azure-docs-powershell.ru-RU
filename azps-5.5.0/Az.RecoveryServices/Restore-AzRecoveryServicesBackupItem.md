---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225412"
---
# <span data-ttu-id="d061a-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d061a-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d061a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d061a-102">SYNOPSIS</span></span>

<span data-ttu-id="d061a-103">Восстановление данных и конфигурации для элемента резервной копии до указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="d061a-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="d061a-104">Необходимые параметры зависят от типа элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d061a-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="d061a-105">Та же команда используется для восстановления виртуальных машин Azure, баз данных, работающих на виртуальных машинах Azure и файловых папках Azure.</span><span class="sxs-lookup"><span data-stu-id="d061a-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="d061a-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d061a-106">SYNTAX</span></span>

### <span data-ttu-id="d061a-107">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d061a-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d061a-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="d061a-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d061a-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="d061a-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d061a-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="d061a-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d061a-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="d061a-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d061a-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="d061a-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d061a-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d061a-113">DESCRIPTION</span></span>

<span data-ttu-id="d061a-114">С **его** использованием можно восстановить данные и конфигурацию элемента резервной копии Azure до указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="d061a-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="d061a-115">**Резервное копирование VM в Azure**</span><span class="sxs-lookup"><span data-stu-id="d061a-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="d061a-116">С помощью этой команды можно архивировать виртуальные машины Azure и восстанавливать диски (управляемые и неуправимые).</span><span class="sxs-lookup"><span data-stu-id="d061a-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="d061a-117">Восстановление полной виртуальной машины не происходит.</span><span class="sxs-lookup"><span data-stu-id="d061a-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="d061a-118">Если это управляемый диск VM, нужно у указывается целевая группа ресурсов, в которой хранятся восстановленные диски.</span><span class="sxs-lookup"><span data-stu-id="d061a-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="d061a-119">Если указана целевая группа ресурсов, моментальные снимки находятся в группе ресурсов, заданной в политике резервного копирования, восстановление происходит мгновенно, а диски создаются из локальных моментальных снимков и хранятся в группе целевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d061a-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="d061a-120">Кроме того, можно восстановить диски как диски без управляемых данных, но при этом будут использовать данные, присутствующие в хранилище служб восстановления Azure, поэтому они будут гораздо медленнее.</span><span class="sxs-lookup"><span data-stu-id="d061a-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="d061a-121">Конфигурация VM и шаблон развертывания, который можно использовать для создания VM-дисков на восстановленных дисках, будут загружены в указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="d061a-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="d061a-122">Если это неуправимный диск VM, моментальные снимки находятся в исходной учетной записи диска и /или в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d061a-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="d061a-123">Если пользователь предоставляет возможность восстановить исходную учетную запись хранения, можно мгновенно восстановить ее.</span><span class="sxs-lookup"><span data-stu-id="d061a-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="d061a-124">В противном случае данные извлекаются из хранилища служб восстановления Azure, а диски создаются в указанной учетной записи хранения вместе с конфигурацией VM и шаблоном развертывания.</span><span class="sxs-lookup"><span data-stu-id="d061a-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d061a-125">По умолчанию резервное копирование VM Azure резервное копирование делает резервные копии всех дисков.</span><span class="sxs-lookup"><span data-stu-id="d061a-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="d061a-126">Во время включения резервного копирования можно выборочно резервные копии соответствующих дисков, используя параметры exclusionList или InclusionList.</span><span class="sxs-lookup"><span data-stu-id="d061a-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="d061a-127">Возможность выборочного восстановления дисков доступна только в том случае, если для одного из них была выборочно размещена их одна из них.</span><span class="sxs-lookup"><span data-stu-id="d061a-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="d061a-128">Дополнительные сведения можно найти в различных наборах параметров и тексте параметров.</span><span class="sxs-lookup"><span data-stu-id="d061a-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="d061a-129">Если используется параметр -VaultId, необходимо также использовать параметр -VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="d061a-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="d061a-130">**Для резервного копирования файловой папки Azure**</span><span class="sxs-lookup"><span data-stu-id="d061a-130">**For Azure File share backup**</span></span>

<span data-ttu-id="d061a-131">Вы можете восстановить всю папку или только определенные файлы или папки.</span><span class="sxs-lookup"><span data-stu-id="d061a-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="d061a-132">Вы можете восстановить исходное или другое место.</span><span class="sxs-lookup"><span data-stu-id="d061a-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="d061a-133">**Для Azure Workloads**</span><span class="sxs-lookup"><span data-stu-id="d061a-133">**For Azure Workloads**</span></span>

<span data-ttu-id="d061a-134">Вы можете восстановить SQL DBs в VMs Azure</span><span class="sxs-lookup"><span data-stu-id="d061a-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="d061a-135">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d061a-135">EXAMPLES</span></span>

### <span data-ttu-id="d061a-136">Пример 1. Восстановление дисков управляемого диска Azure VM из заданной точки восстановления</span><span class="sxs-lookup"><span data-stu-id="d061a-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d061a-137">Первая команда получает хранилище служб восстановления и сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="d061a-138">Вторая команда получает элемент резервной копии типа AzureVM (V2VM) и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d061a-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d061a-139">Третья команда получает дату от семи дней назад и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d061a-140">Четвертая команда получает текущую дату, а затем сохраняет ее в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d061a-141">Пятая команда получает список точек восстановления для определенного элемента резервной копии, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="d061a-142">Последняя команда восстанавливает все диски целевой группы ресурсов Target_RG а затем предоставляет сведения о конфигурации VM и шаблон развертывания в учетной записи хранилища DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="d061a-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="d061a-143">Пример 2. Восстановление указанных дисков управляемого диска Azure VM из заданной точки восстановления</span><span class="sxs-lookup"><span data-stu-id="d061a-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d061a-144">Первая команда получает хранилище служб восстановления и сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="d061a-145">Вторая команда получает элемент резервной копии типа AzureVM (V2VM) и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d061a-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d061a-146">Третья команда получает дату от семи дней назад и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d061a-147">Четвертая команда получает текущую дату, а затем сохраняет ее в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d061a-148">Пятая команда получает список точек восстановления для определенного элемента резервной копии, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="d061a-149">Шестая команда сохраняет список дисков, которые нужно восстановить, в переменной restoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="d061a-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="d061a-150">Последняя команда восстанавливает указанные LUNS-диски в целевую группу ресурсов Target_RG, а затем предоставляет сведения о конфигурации VM и шаблоне развертывания в учетной записи хранилища DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="d061a-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="d061a-151">Пример 3. Восстановление дисков управляемой VM-модели в качестве неугодных дисков</span><span class="sxs-lookup"><span data-stu-id="d061a-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d061a-152">Первая команда получает хранилище RecoveryServices и сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="d061a-153">Вторая команда получает элемент резервной копии и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d061a-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d061a-154">Третья команда получает дату от семи дней назад и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d061a-155">Четвертая команда получает текущую дату, а затем сохраняет ее в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d061a-156">Пятая команда получает список точек восстановления для определенного элемента резервной копии, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="d061a-157">Шестая команда восстанавливает диски как неугодные диски.</span><span class="sxs-lookup"><span data-stu-id="d061a-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="d061a-158">Пример 4. Восстановление неугодного VM-диска с использованием исходной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d061a-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d061a-159">Первая команда получает хранилище RecoveryServices и сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="d061a-160">Вторая команда получает элемент резервной копии и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d061a-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d061a-161">Третья команда получает дату от семи дней назад и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d061a-162">Четвертая команда получает текущую дату, а затем сохраняет ее в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d061a-163">Пятая команда получает список точек восстановления для определенного элемента резервной копии, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d061a-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="d061a-164">Шестая команда восстанавливает диски как неугружаные диски для исходных учетных записей хранилища.</span><span class="sxs-lookup"><span data-stu-id="d061a-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="d061a-165">Пример 5. Восстановление нескольких файлов элемента AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d061a-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d061a-166">Первая команда получает хранилище служб восстановления и сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="d061a-167">Вторая команда получает элемент backup named fileshareitem и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d061a-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d061a-168">Третья команда получает список точек восстановления для определенного элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d061a-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="d061a-169">Четвертая команда определяет, какие файлы нужно восстановить, и сохраняет их в $files переменной.</span><span class="sxs-lookup"><span data-stu-id="d061a-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="d061a-170">Последняя команда восстанавливает исходное расположение указанных файлов.</span><span class="sxs-lookup"><span data-stu-id="d061a-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="d061a-171">Пример 6. Восстановление SQL в VM-объекте Azure на другой целевой VM-платформе для отдельной полной точки восстановления</span><span class="sxs-lookup"><span data-stu-id="d061a-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="d061a-172">Пример 7. Восстановление SQL в VM-объекте Azure на другой целевой VM-объект для точки восстановления журнала</span><span class="sxs-lookup"><span data-stu-id="d061a-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="d061a-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d061a-173">PARAMETERS</span></span>

### <span data-ttu-id="d061a-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d061a-174">-DefaultProfile</span></span>

<span data-ttu-id="d061a-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d061a-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="d061a-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="d061a-177">Используется для восстановления нескольких файлов из файловой папки.</span><span class="sxs-lookup"><span data-stu-id="d061a-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="d061a-178">Пути к элементым, которые нужно восстановить в файловой папке.</span><span class="sxs-lookup"><span data-stu-id="d061a-178">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d061a-179">-RecoveryPoint</span></span>

<span data-ttu-id="d061a-180">Указывает точку восстановления, до которой нужно восстановить элемент резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d061a-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="d061a-181">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint,** используйте cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**</span><span class="sxs-lookup"><span data-stu-id="d061a-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="d061a-182">-ResolveConflict</span></span>

<span data-ttu-id="d061a-183">Если восстановленный элемент также существует в пункте назначения, указать, следует ли переописать его.</span><span class="sxs-lookup"><span data-stu-id="d061a-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="d061a-184">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d061a-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d061a-185">Переописывание</span><span class="sxs-lookup"><span data-stu-id="d061a-185">Overwrite</span></span>
- <span data-ttu-id="d061a-186">Пропустить</span><span class="sxs-lookup"><span data-stu-id="d061a-186">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="d061a-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="d061a-188">Этот переключатель используется для указания функции "Восстановить как неудаченные диски"</span><span class="sxs-lookup"><span data-stu-id="d061a-188">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="d061a-189">-RestoreDiskList</span></span>
<span data-ttu-id="d061a-190">Выбор дисков для восстановления backed up VM</span><span class="sxs-lookup"><span data-stu-id="d061a-190">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="d061a-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="d061a-192">Используйте этот переключатель, чтобы восстановить только диски ОС для VM-</span><span class="sxs-lookup"><span data-stu-id="d061a-192">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="d061a-193">-SourceFilePath</span></span>

<span data-ttu-id="d061a-194">Используется для восстановления определенного элемента из файловой папки.</span><span class="sxs-lookup"><span data-stu-id="d061a-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="d061a-195">Путь к элементу, который нужно восстановить в файловой папке.</span><span class="sxs-lookup"><span data-stu-id="d061a-195">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="d061a-196">-SourceFileType</span></span>

<span data-ttu-id="d061a-197">Используется для восстановления определенного элемента из файловой папки.</span><span class="sxs-lookup"><span data-stu-id="d061a-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="d061a-198">Тип элемента, который нужно восстановить в файловой папке.</span><span class="sxs-lookup"><span data-stu-id="d061a-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="d061a-199">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d061a-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d061a-200">Файл</span><span class="sxs-lookup"><span data-stu-id="d061a-200">File</span></span>
- <span data-ttu-id="d061a-201">Каталог</span><span class="sxs-lookup"><span data-stu-id="d061a-201">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d061a-202">-StorageAccountName</span></span>

<span data-ttu-id="d061a-203">Указывает имя целевой учетной записи хранения в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="d061a-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="d061a-204">В рамках процесса восстановления этот cmdlet хранит диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d061a-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d061a-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="d061a-206">Имя группы ресурсов, которая содержит целевую учетную запись хранения в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="d061a-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="d061a-207">В рамках процесса восстановления этот cmdlet хранит диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d061a-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="d061a-208">-TargetFileShareName</span></span>

<span data-ttu-id="d061a-209">Файловая папка, в которую нужно восстановить файл.</span><span class="sxs-lookup"><span data-stu-id="d061a-209">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="d061a-210">-TargetFolder</span></span>

<span data-ttu-id="d061a-211">В папке TargetFileShareName необходимо восстановить папку, в которую нужно восстановить файл.</span><span class="sxs-lookup"><span data-stu-id="d061a-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="d061a-212">Если нужно восстановить его в корневую папку, придате значения целевой папки пустой строке.</span><span class="sxs-lookup"><span data-stu-id="d061a-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d061a-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="d061a-214">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="d061a-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="d061a-215">Применимо к резервному копированию VM-дисков</span><span class="sxs-lookup"><span data-stu-id="d061a-215">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d061a-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="d061a-217">Учетная запись хранения, в которую нужно восстановить файл.</span><span class="sxs-lookup"><span data-stu-id="d061a-217">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d061a-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="d061a-219">Используйте этот переключатель, если диски с точки восстановления восстанавливаются в исходных учетных записях хранилища.</span><span class="sxs-lookup"><span data-stu-id="d061a-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d061a-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="d061a-221">Код DES для шифрования восстановленных дисков.</span><span class="sxs-lookup"><span data-stu-id="d061a-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="d061a-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="d061a-223">Этот переключатель используется для запуска восстановления перекрестной области до дополнительного региона.</span><span class="sxs-lookup"><span data-stu-id="d061a-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d061a-224">-VaultId</span></span>

<span data-ttu-id="d061a-225">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d061a-225">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="d061a-226">-VaultLocation</span></span>

<span data-ttu-id="d061a-227">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d061a-227">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="d061a-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="d061a-229">Config восстановления</span><span class="sxs-lookup"><span data-stu-id="d061a-229">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-230">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d061a-230">-Confirm</span></span>

<span data-ttu-id="d061a-231">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d061a-231">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d061a-232">-WhatIf</span></span>

<span data-ttu-id="d061a-233">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d061a-233">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d061a-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d061a-234">CommonParameters</span></span>
<span data-ttu-id="d061a-235">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d061a-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d061a-236">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d061a-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d061a-237">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d061a-237">INPUTS</span></span>

### <span data-ttu-id="d061a-238">System.String</span><span class="sxs-lookup"><span data-stu-id="d061a-238">System.String</span></span>

### <span data-ttu-id="d061a-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="d061a-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="d061a-240">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d061a-240">OUTPUTS</span></span>

### <span data-ttu-id="d061a-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="d061a-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d061a-242">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d061a-242">NOTES</span></span>

## <span data-ttu-id="d061a-243">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d061a-243">RELATED LINKS</span></span>

[<span data-ttu-id="d061a-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d061a-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="d061a-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d061a-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="d061a-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d061a-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
