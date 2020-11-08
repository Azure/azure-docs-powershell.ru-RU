---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079372"
---
# <span data-ttu-id="5ddea-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5ddea-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5ddea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ddea-102">SYNOPSIS</span></span>

<span data-ttu-id="5ddea-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="5ddea-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="5ddea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ddea-104">SYNTAX</span></span>

### <span data-ttu-id="5ddea-105">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ddea-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ddea-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddea-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ddea-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddea-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ddea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ddea-108">DESCRIPTION</span></span>

<span data-ttu-id="5ddea-109">Командлет **RESTORE-AzRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="5ddea-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="5ddea-110">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="5ddea-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="5ddea-111">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5ddea-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5ddea-112">Она восстанавливает управляемые диски в целевую группу ресурсов и сведения о конфигурации для учетной записи хранения клиента после завершения операции восстановления, необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="5ddea-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="5ddea-113">Чтобы получить дополнительные сведения, refter другие возможные наборы параметров и текст параметров.</span><span class="sxs-lookup"><span data-stu-id="5ddea-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="5ddea-114">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="5ddea-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="5ddea-115">Примечание. чтобы успешно выполнить этот командлет в дополнение к параметру-VaultId Parameter-VaultLocation, необходимо также использовать его.</span><span class="sxs-lookup"><span data-stu-id="5ddea-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="5ddea-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ddea-116">EXAMPLES</span></span>

### <span data-ttu-id="5ddea-117">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="5ddea-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="5ddea-118">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5ddea-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5ddea-119">Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5ddea-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5ddea-120">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="5ddea-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5ddea-121">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5ddea-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5ddea-122">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5ddea-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5ddea-123">Указанный диапазон дат — последние 7 дней.</span><span class="sxs-lookup"><span data-stu-id="5ddea-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="5ddea-124">Команда седьмая указывает, какие диски нужно восстановить из точки восстановления и будет храниться в $restoreDiskLUNs переменной.</span><span class="sxs-lookup"><span data-stu-id="5ddea-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="5ddea-125">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="5ddea-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="5ddea-126">Пример 2: восстановление нескольких файлов элемента AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5ddea-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="5ddea-127">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5ddea-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5ddea-128">Вторая команда возвращает элемент резервного копирования с именем fileshareitem и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5ddea-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5ddea-129">Третья команда получает список точек восстановления для определенного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5ddea-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="5ddea-130">Четвертая команда, spceifies, какие файлы нужно восстановить, и сохранит ее в $files переменной.</span><span class="sxs-lookup"><span data-stu-id="5ddea-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="5ddea-131">Последняя команда восстанавливает исходное расположение указанных файлов.</span><span class="sxs-lookup"><span data-stu-id="5ddea-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="5ddea-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5ddea-132">Example 3</span></span>

<span data-ttu-id="5ddea-133">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="5ddea-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="5ddea-134">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="5ddea-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="5ddea-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ddea-135">PARAMETERS</span></span>

### <span data-ttu-id="5ddea-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddea-136">-DefaultProfile</span></span>

<span data-ttu-id="5ddea-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddea-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ddea-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5ddea-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="5ddea-139">Используется для восстановления нескольких файлов из общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="5ddea-140">Пути к элементам, которые должны быть восстановлены в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="5ddea-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5ddea-141">-RecoveryPoint</span></span>

<span data-ttu-id="5ddea-142">Указывает точку восстановления, в которую нужно восстановить элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5ddea-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="5ddea-143">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="5ddea-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="5ddea-144">-ResolveConflict</span></span>

<span data-ttu-id="5ddea-145">Если восстановленный элемент также существует в месте назначения, используйте его, чтобы указать, следует ли переписывать или нет.</span><span class="sxs-lookup"><span data-stu-id="5ddea-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="5ddea-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5ddea-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ddea-147">Перезаписать</span><span class="sxs-lookup"><span data-stu-id="5ddea-147">Overwrite</span></span>
- <span data-ttu-id="5ddea-148">Пуст</span><span class="sxs-lookup"><span data-stu-id="5ddea-148">Skip</span></span>

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

### <span data-ttu-id="5ddea-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="5ddea-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="5ddea-150">Используйте этот параметр, чтобы указать, что нужно восстановить как неуправляемые диски.</span><span class="sxs-lookup"><span data-stu-id="5ddea-150">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="5ddea-151">-RestoreDiskList</span></span>
<span data-ttu-id="5ddea-152">Указание дисков для восстановления резервной копии виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5ddea-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="5ddea-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="5ddea-154">Используйте этот переключатель, чтобы восстановить только диски ОС резервной копии виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ddea-154">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5ddea-155">-SourceFilePath</span></span>

<span data-ttu-id="5ddea-156">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5ddea-157">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="5ddea-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="5ddea-158">-SourceFileType</span></span>

<span data-ttu-id="5ddea-159">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5ddea-160">Тип элемента, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="5ddea-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5ddea-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ddea-162">Файл</span><span class="sxs-lookup"><span data-stu-id="5ddea-162">File</span></span>
- <span data-ttu-id="5ddea-163">Папка</span><span class="sxs-lookup"><span data-stu-id="5ddea-163">Directory</span></span>

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

### <span data-ttu-id="5ddea-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5ddea-164">-StorageAccountName</span></span>

<span data-ttu-id="5ddea-165">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5ddea-166">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5ddea-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddea-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="5ddea-168">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="5ddea-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5ddea-169">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5ddea-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="5ddea-170">-TargetFileShareName</span></span>

<span data-ttu-id="5ddea-171">Файловый документ, на который должна быть восстановлена файловая общий доступ.</span><span class="sxs-lookup"><span data-stu-id="5ddea-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5ddea-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="5ddea-172">-TargetFolder</span></span>

<span data-ttu-id="5ddea-173">Папка, в которой должен быть восстановлен файл общего доступа в TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="5ddea-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="5ddea-174">Если резервное содержимое должно быть восстановлено в корневой папке, присвойте целевым папкам значения в виде пустой строки.</span><span class="sxs-lookup"><span data-stu-id="5ddea-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="5ddea-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddea-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="5ddea-176">Группа ресурсов, на которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="5ddea-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="5ddea-177">Применимо к резервному копированию ВМ с управляемыми дисками</span><span class="sxs-lookup"><span data-stu-id="5ddea-177">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5ddea-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="5ddea-179">Учетная запись хранения, на которую нужно восстановить файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="5ddea-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5ddea-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ddea-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="5ddea-181">Используйте этот параметр, если нужно восстановить диски из точки восстановления в первоначальные учетные записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5ddea-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddea-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5ddea-182">-VaultId</span></span>

<span data-ttu-id="5ddea-183">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5ddea-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ddea-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="5ddea-184">-VaultLocation</span></span>

<span data-ttu-id="5ddea-185">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5ddea-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ddea-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="5ddea-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="5ddea-187">Конфигурация восстановления</span><span class="sxs-lookup"><span data-stu-id="5ddea-187">Recovery config</span></span>

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

### <span data-ttu-id="5ddea-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ddea-188">-Confirm</span></span>

<span data-ttu-id="5ddea-189">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ddea-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ddea-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddea-190">-WhatIf</span></span>

<span data-ttu-id="5ddea-191">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ddea-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="5ddea-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddea-192">CommonParameters</span></span>
<span data-ttu-id="5ddea-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ddea-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddea-194">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ddea-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddea-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ddea-195">INPUTS</span></span>

### <span data-ttu-id="5ddea-196">System. String</span><span class="sxs-lookup"><span data-stu-id="5ddea-196">System.String</span></span>

### <span data-ttu-id="5ddea-197">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5ddea-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="5ddea-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ddea-198">OUTPUTS</span></span>

### <span data-ttu-id="5ddea-199">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5ddea-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5ddea-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ddea-200">NOTES</span></span>

## <span data-ttu-id="5ddea-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ddea-201">RELATED LINKS</span></span>

[<span data-ttu-id="5ddea-202">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5ddea-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5ddea-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5ddea-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5ddea-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5ddea-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
