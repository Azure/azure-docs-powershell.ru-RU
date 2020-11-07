---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904830"
---
# <span data-ttu-id="0ab53-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0ab53-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0ab53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ab53-102">SYNOPSIS</span></span>

<span data-ttu-id="0ab53-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ab53-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="0ab53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ab53-104">SYNTAX</span></span>

### <span data-ttu-id="0ab53-105">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ab53-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ab53-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ab53-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab53-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ab53-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab53-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab53-108">DESCRIPTION</span></span>

<span data-ttu-id="0ab53-109">Командлет **RESTORE-AzRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ab53-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="0ab53-110">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="0ab53-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="0ab53-111">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0ab53-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="0ab53-112">Она восстанавливает данные о дисках и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0ab53-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="0ab53-113">После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="0ab53-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="0ab53-114">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="0ab53-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="0ab53-115">Примечание. чтобы успешно выполнить этот командлет в дополнение к параметру-VaultId Parameter-VaultLocation, необходимо также использовать его.</span><span class="sxs-lookup"><span data-stu-id="0ab53-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="0ab53-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ab53-116">EXAMPLES</span></span>

### <span data-ttu-id="0ab53-117">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="0ab53-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="0ab53-118">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="0ab53-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="0ab53-119">Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="0ab53-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="0ab53-120">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="0ab53-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="0ab53-121">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="0ab53-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="0ab53-122">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="0ab53-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="0ab53-123">Указанный диапазон дат — последние 7 дней.</span><span class="sxs-lookup"><span data-stu-id="0ab53-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="0ab53-124">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="0ab53-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="0ab53-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ab53-125">PARAMETERS</span></span>

### <span data-ttu-id="0ab53-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab53-126">-DefaultProfile</span></span>

<span data-ttu-id="0ab53-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab53-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ab53-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0ab53-128">-RecoveryPoint</span></span>

<span data-ttu-id="0ab53-129">Указывает точку восстановления, в которую нужно восстановить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0ab53-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="0ab53-130">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="0ab53-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="0ab53-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="0ab53-131">-ResolveConflict</span></span>

<span data-ttu-id="0ab53-132">Если восстановленный элемент также существует в месте назначения, используйте его, чтобы указать, следует ли переписывать или нет.</span><span class="sxs-lookup"><span data-stu-id="0ab53-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="0ab53-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ab53-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab53-134">Перезаписать</span><span class="sxs-lookup"><span data-stu-id="0ab53-134">Overwrite</span></span>
- <span data-ttu-id="0ab53-135">Пуст</span><span class="sxs-lookup"><span data-stu-id="0ab53-135">Skip</span></span>

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

### <span data-ttu-id="0ab53-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="0ab53-136">-SourceFilePath</span></span>

<span data-ttu-id="0ab53-137">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="0ab53-138">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="0ab53-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="0ab53-139">-SourceFileType</span></span>

<span data-ttu-id="0ab53-140">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="0ab53-141">Тип элемента, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="0ab53-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ab53-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab53-143">Файл</span><span class="sxs-lookup"><span data-stu-id="0ab53-143">File</span></span>
- <span data-ttu-id="0ab53-144">Папка</span><span class="sxs-lookup"><span data-stu-id="0ab53-144">Directory</span></span>

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

### <span data-ttu-id="0ab53-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ab53-145">-StorageAccountName</span></span>

<span data-ttu-id="0ab53-146">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="0ab53-147">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ab53-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="0ab53-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab53-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="0ab53-149">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="0ab53-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="0ab53-150">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ab53-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="0ab53-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="0ab53-151">-TargetFileShareName</span></span>

<span data-ttu-id="0ab53-152">Файловый документ, на который должна быть восстановлена файловая общий доступ.</span><span class="sxs-lookup"><span data-stu-id="0ab53-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="0ab53-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="0ab53-153">-TargetFolder</span></span>

<span data-ttu-id="0ab53-154">Папка, в которой должен быть восстановлен файл общего доступа в TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="0ab53-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="0ab53-155">Если резервное содержимое должно быть восстановлено в корневой папке, присвойте целевым папкам значения в виде пустой строки.</span><span class="sxs-lookup"><span data-stu-id="0ab53-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="0ab53-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab53-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="0ab53-157">Группа ресурсов, на которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="0ab53-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="0ab53-158">Применимо к резервному копированию ВМ с управляемыми дисками</span><span class="sxs-lookup"><span data-stu-id="0ab53-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="0ab53-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ab53-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="0ab53-160">Учетная запись хранения, на которую нужно восстановить файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="0ab53-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="0ab53-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ab53-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="0ab53-162">Используйте этот параметр, если нужно восстановить диски из точки восстановления в первоначальные учетные записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ab53-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="0ab53-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0ab53-163">-VaultId</span></span>

<span data-ttu-id="0ab53-164">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ab53-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0ab53-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="0ab53-165">-VaultLocation</span></span>

<span data-ttu-id="0ab53-166">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ab53-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0ab53-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="0ab53-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="0ab53-168">Конфигурация восстановления</span><span class="sxs-lookup"><span data-stu-id="0ab53-168">Recovery config</span></span>

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

### <span data-ttu-id="0ab53-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ab53-169">-Confirm</span></span>

<span data-ttu-id="0ab53-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ab53-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab53-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab53-171">-WhatIf</span></span>

<span data-ttu-id="0ab53-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ab53-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ab53-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ab53-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab53-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab53-174">-CommonParameters</span></span>

<span data-ttu-id="0ab53-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ab53-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab53-176">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ab53-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab53-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ab53-177">INPUTS</span></span>

### <span data-ttu-id="0ab53-178">System. String</span><span class="sxs-lookup"><span data-stu-id="0ab53-178">System.String</span></span>

### <span data-ttu-id="0ab53-179">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="0ab53-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="0ab53-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab53-180">OUTPUTS</span></span>

### <span data-ttu-id="0ab53-181">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0ab53-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0ab53-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ab53-182">NOTES</span></span>

## <span data-ttu-id="0ab53-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ab53-183">RELATED LINKS</span></span>

[<span data-ttu-id="0ab53-184">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0ab53-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0ab53-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0ab53-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0ab53-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0ab53-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
