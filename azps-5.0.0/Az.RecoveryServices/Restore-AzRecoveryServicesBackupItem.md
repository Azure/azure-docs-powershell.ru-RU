---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247212"
---
# <span data-ttu-id="26443-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="26443-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="26443-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26443-102">SYNOPSIS</span></span>

<span data-ttu-id="26443-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="26443-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="26443-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26443-104">SYNTAX</span></span>

### <span data-ttu-id="26443-105">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26443-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26443-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="26443-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26443-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="26443-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26443-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="26443-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26443-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="26443-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26443-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="26443-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26443-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26443-111">DESCRIPTION</span></span>

<span data-ttu-id="26443-112">Командлет **RESTORE-AzRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="26443-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="26443-113">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="26443-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="26443-114">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="26443-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="26443-115">Она восстанавливает управляемые диски в целевую группу ресурсов и сведения о конфигурации для учетной записи хранения клиента после завершения операции восстановления, необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="26443-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="26443-116">Чтобы получить дополнительные сведения, refter другие возможные наборы параметров и текст параметров.</span><span class="sxs-lookup"><span data-stu-id="26443-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="26443-117">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="26443-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="26443-118">Примечание. чтобы успешно выполнить этот командлет в дополнение к параметру-VaultId Parameter-VaultLocation, необходимо также использовать его.</span><span class="sxs-lookup"><span data-stu-id="26443-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="26443-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26443-119">EXAMPLES</span></span>

### <span data-ttu-id="26443-120">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="26443-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="26443-121">Первая команда получает хранилище RecoveryServices и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="26443-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="26443-122">Вторая команда получает элементы резервного копирования, а затем сохраняет их в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="26443-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="26443-123">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="26443-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="26443-124">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="26443-125">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="26443-126">Шестая команда задает диски для восстановления из точки восстановления и сохраняет их в $restoreDiskLUNs переменной.</span><span class="sxs-lookup"><span data-stu-id="26443-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="26443-127">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="26443-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="26443-128">Пример 2: восстановление нескольких файлов элемента AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="26443-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="26443-129">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="26443-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="26443-130">Вторая команда возвращает элемент резервного копирования с именем fileshareitem и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="26443-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="26443-131">Третья команда получает список точек восстановления для определенного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="26443-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="26443-132">Четвертая команда, spceifies, какие файлы нужно восстановить, и сохранит ее в $files переменной.</span><span class="sxs-lookup"><span data-stu-id="26443-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="26443-133">Последняя команда восстанавливает исходное расположение указанных файлов.</span><span class="sxs-lookup"><span data-stu-id="26443-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="26443-134">Пример 3</span><span class="sxs-lookup"><span data-stu-id="26443-134">Example 3</span></span>

<span data-ttu-id="26443-135">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="26443-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="26443-136">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="26443-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="26443-137">Пример 4: восстановление управляемой виртуальной машины в качестве управляемых дисков</span><span class="sxs-lookup"><span data-stu-id="26443-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="26443-138">Первая команда получает хранилище RecoveryServices и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="26443-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="26443-139">Вторая команда возвращает элемент резервного копирования, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="26443-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="26443-140">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="26443-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="26443-141">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="26443-142">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="26443-143">Шестая команда восстанавливает диски как управляемые диски с заданной группой целевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26443-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="26443-144">Пример 5: восстановление управляемой виртуальной машины в качестве неуправляемых дисков</span><span class="sxs-lookup"><span data-stu-id="26443-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="26443-145">Первая команда получает хранилище RecoveryServices и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="26443-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="26443-146">Вторая команда возвращает элемент резервного копирования, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="26443-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="26443-147">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="26443-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="26443-148">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="26443-149">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="26443-150">Шестая команда восстанавливает диски как неуправляемые диски.</span><span class="sxs-lookup"><span data-stu-id="26443-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="26443-151">Пример 6: восстановление неуправляемой виртуальной машины в качестве неуправляемых дисков с помощью исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26443-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="26443-152">Первая команда получает хранилище RecoveryServices и сохраняет его в переменной $vault.</span><span class="sxs-lookup"><span data-stu-id="26443-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="26443-153">Вторая команда возвращает элемент резервного копирования, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="26443-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="26443-154">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="26443-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="26443-155">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="26443-156">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="26443-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="26443-157">Шестая команда восстанавливает диски как неуправляемые диски с помощью исходной учетной записи хранения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26443-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="26443-158">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26443-158">PARAMETERS</span></span>

### <span data-ttu-id="26443-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26443-159">-DefaultProfile</span></span>

<span data-ttu-id="26443-160">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26443-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26443-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="26443-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="26443-162">Используется для восстановления нескольких файлов из общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="26443-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="26443-163">Пути к элементам, которые должны быть восстановлены в общей папке.</span><span class="sxs-lookup"><span data-stu-id="26443-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="26443-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="26443-164">-RecoveryPoint</span></span>

<span data-ttu-id="26443-165">Указывает точку восстановления, в которую нужно восстановить элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="26443-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="26443-166">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="26443-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="26443-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="26443-167">-ResolveConflict</span></span>

<span data-ttu-id="26443-168">Если восстановленный элемент также существует в месте назначения, используйте его, чтобы указать, следует ли переписывать или нет.</span><span class="sxs-lookup"><span data-stu-id="26443-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="26443-169">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26443-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26443-170">Перезаписать</span><span class="sxs-lookup"><span data-stu-id="26443-170">Overwrite</span></span>
- <span data-ttu-id="26443-171">Пуст</span><span class="sxs-lookup"><span data-stu-id="26443-171">Skip</span></span>

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

### <span data-ttu-id="26443-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="26443-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="26443-173">Используйте этот параметр, чтобы указать, что нужно восстановить как неуправляемые диски.</span><span class="sxs-lookup"><span data-stu-id="26443-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="26443-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="26443-174">-RestoreDiskList</span></span>
<span data-ttu-id="26443-175">Указание дисков для восстановления резервной копии виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="26443-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="26443-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="26443-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="26443-177">Используйте этот переключатель, чтобы восстановить только диски ОС резервной копии виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26443-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="26443-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="26443-178">-SourceFilePath</span></span>

<span data-ttu-id="26443-179">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="26443-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="26443-180">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="26443-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="26443-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="26443-181">-SourceFileType</span></span>

<span data-ttu-id="26443-182">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="26443-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="26443-183">Тип элемента, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="26443-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="26443-184">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26443-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26443-185">Файл</span><span class="sxs-lookup"><span data-stu-id="26443-185">File</span></span>
- <span data-ttu-id="26443-186">Папка</span><span class="sxs-lookup"><span data-stu-id="26443-186">Directory</span></span>

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

### <span data-ttu-id="26443-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="26443-187">-StorageAccountName</span></span>

<span data-ttu-id="26443-188">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="26443-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="26443-189">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26443-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="26443-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26443-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="26443-191">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="26443-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="26443-192">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26443-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="26443-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="26443-193">-TargetFileShareName</span></span>

<span data-ttu-id="26443-194">Файловый документ, на который должна быть восстановлена файловая общий доступ.</span><span class="sxs-lookup"><span data-stu-id="26443-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="26443-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="26443-195">-TargetFolder</span></span>

<span data-ttu-id="26443-196">Папка, в которой должен быть восстановлен файл общего доступа в TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="26443-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="26443-197">Если резервное содержимое должно быть восстановлено в корневой папке, присвойте целевым папкам значения в виде пустой строки.</span><span class="sxs-lookup"><span data-stu-id="26443-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="26443-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26443-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="26443-199">Группа ресурсов, на которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="26443-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="26443-200">Применимо к резервному копированию ВМ с управляемыми дисками</span><span class="sxs-lookup"><span data-stu-id="26443-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="26443-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="26443-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="26443-202">Учетная запись хранения, на которую нужно восстановить файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="26443-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="26443-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26443-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="26443-204">Используйте этот параметр, если нужно восстановить диски из точки восстановления в первоначальные учетные записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26443-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="26443-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="26443-205">-VaultId</span></span>

<span data-ttu-id="26443-206">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="26443-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="26443-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="26443-207">-VaultLocation</span></span>

<span data-ttu-id="26443-208">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="26443-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="26443-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="26443-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="26443-210">Конфигурация восстановления</span><span class="sxs-lookup"><span data-stu-id="26443-210">Recovery config</span></span>

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

### <span data-ttu-id="26443-211">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26443-211">-Confirm</span></span>

<span data-ttu-id="26443-212">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26443-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26443-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26443-213">-WhatIf</span></span>

<span data-ttu-id="26443-214">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26443-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="26443-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26443-215">CommonParameters</span></span>
<span data-ttu-id="26443-216">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26443-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26443-217">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26443-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26443-218">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26443-218">INPUTS</span></span>

### <span data-ttu-id="26443-219">System. String</span><span class="sxs-lookup"><span data-stu-id="26443-219">System.String</span></span>

### <span data-ttu-id="26443-220">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="26443-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="26443-221">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26443-221">OUTPUTS</span></span>

### <span data-ttu-id="26443-222">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="26443-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="26443-223">Пуск</span><span class="sxs-lookup"><span data-stu-id="26443-223">NOTES</span></span>

## <span data-ttu-id="26443-224">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26443-224">RELATED LINKS</span></span>

[<span data-ttu-id="26443-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="26443-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="26443-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="26443-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="26443-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="26443-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
