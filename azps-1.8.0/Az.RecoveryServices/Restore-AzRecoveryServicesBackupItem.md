---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729621"
---
# <span data-ttu-id="e4a49-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e4a49-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e4a49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4a49-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a49-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4a49-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="e4a49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4a49-104">SYNTAX</span></span>

### <span data-ttu-id="e4a49-105">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4a49-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4a49-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4a49-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4a49-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4a49-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a49-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4a49-108">DESCRIPTION</span></span>
<span data-ttu-id="e4a49-109">Командлет **RESTORE-AzRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4a49-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="e4a49-110">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="e4a49-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="e4a49-111">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e4a49-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="e4a49-112">Она восстанавливает данные о дисках и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e4a49-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="e4a49-113">После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="e4a49-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="e4a49-114">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="e4a49-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e4a49-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4a49-115">EXAMPLES</span></span>

### <span data-ttu-id="e4a49-116">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="e4a49-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="e4a49-117">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e4a49-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e4a49-118">Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e4a49-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e4a49-119">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="e4a49-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e4a49-120">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e4a49-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e4a49-121">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="e4a49-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e4a49-122">Указанный диапазон дат — последние 7 дней.</span><span class="sxs-lookup"><span data-stu-id="e4a49-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="e4a49-123">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="e4a49-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="e4a49-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4a49-124">PARAMETERS</span></span>

### <span data-ttu-id="e4a49-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a49-125">-DefaultProfile</span></span>
<span data-ttu-id="e4a49-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a49-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4a49-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e4a49-127">-RecoveryPoint</span></span>
<span data-ttu-id="e4a49-128">Указывает точку восстановления, в которую нужно восстановить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e4a49-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="e4a49-129">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет Get-AzRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="e4a49-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="e4a49-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="e4a49-130">-ResolveConflict</span></span>
<span data-ttu-id="e4a49-131">Если восстановленный элемент также существует в месте назначения, используйте его, чтобы указать, следует ли переписывать или нет.</span><span class="sxs-lookup"><span data-stu-id="e4a49-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="e4a49-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="e4a49-132">-SourceFilePath</span></span>
<span data-ttu-id="e4a49-133">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="e4a49-134">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="e4a49-135">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="e4a49-135">-SourceFileType</span></span>
<span data-ttu-id="e4a49-136">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="e4a49-137">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="e4a49-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4a49-138">-StorageAccountName</span></span>
<span data-ttu-id="e4a49-139">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="e4a49-140">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e4a49-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="e4a49-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a49-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="e4a49-142">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="e4a49-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="e4a49-143">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e4a49-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="e4a49-144">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="e4a49-144">-TargetFileShareName</span></span>
<span data-ttu-id="e4a49-145">Файловый документ, на который должна быть восстановлена файловая общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e4a49-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="e4a49-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="e4a49-146">-TargetFolder</span></span>
<span data-ttu-id="e4a49-147">Папка, в которой должен быть восстановлен файл общего доступа в targetFileShareName. Оставьте переменную пустой для восстановления в разделе корневая папка.</span><span class="sxs-lookup"><span data-stu-id="e4a49-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="e4a49-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a49-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="e4a49-149">Группа ресурсов, на которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="e4a49-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="e4a49-150">Применимо к резервному копированию ВМ с управляемыми дисками</span><span class="sxs-lookup"><span data-stu-id="e4a49-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="e4a49-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4a49-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="e4a49-152">Учетная запись хранения, на которую нужно восстановить файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e4a49-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="e4a49-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4a49-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="e4a49-154">Используйте этот параметр, если нужно восстановить диски из точки восстановления в первоначальные учетные записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e4a49-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="e4a49-155">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e4a49-155">-VaultId</span></span>
<span data-ttu-id="e4a49-156">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4a49-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e4a49-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="e4a49-157">-VaultLocation</span></span>
<span data-ttu-id="e4a49-158">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4a49-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e4a49-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="e4a49-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="e4a49-160">Конфигурация восстановления</span><span class="sxs-lookup"><span data-stu-id="e4a49-160">Recovery config</span></span>

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

### <span data-ttu-id="e4a49-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4a49-161">-Confirm</span></span>
<span data-ttu-id="e4a49-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4a49-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a49-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a49-163">-WhatIf</span></span>
<span data-ttu-id="e4a49-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4a49-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4a49-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4a49-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a49-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a49-166">CommonParameters</span></span>
<span data-ttu-id="e4a49-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4a49-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a49-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a49-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a49-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4a49-169">INPUTS</span></span>

### <span data-ttu-id="e4a49-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e4a49-170">System.String</span></span>

### <span data-ttu-id="e4a49-171">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e4a49-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e4a49-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4a49-172">OUTPUTS</span></span>

### <span data-ttu-id="e4a49-173">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e4a49-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e4a49-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4a49-174">NOTES</span></span>

## <span data-ttu-id="e4a49-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4a49-175">RELATED LINKS</span></span>

[<span data-ttu-id="e4a49-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e4a49-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e4a49-177">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e4a49-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e4a49-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e4a49-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


