---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556560"
---
# <span data-ttu-id="02428-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="02428-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="02428-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02428-102">SYNOPSIS</span></span>
<span data-ttu-id="02428-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="02428-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02428-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02428-104">SYNTAX</span></span>

### <span data-ttu-id="02428-105">AzureVMParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02428-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02428-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="02428-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02428-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02428-107">DESCRIPTION</span></span>
<span data-ttu-id="02428-108">Командлет **RESTORE-AzureRmRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="02428-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="02428-109">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="02428-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="02428-110">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="02428-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="02428-111">Она восстанавливает данные о дисках и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="02428-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="02428-112">После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="02428-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="02428-113">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="02428-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="02428-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02428-114">EXAMPLES</span></span>

### <span data-ttu-id="02428-115">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="02428-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="02428-116">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="02428-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="02428-117">Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="02428-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="02428-118">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="02428-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="02428-119">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="02428-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="02428-120">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="02428-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="02428-121">Указанный диапазон дат — последние 7 дней.</span><span class="sxs-lookup"><span data-stu-id="02428-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="02428-122">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="02428-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="02428-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02428-123">PARAMETERS</span></span>

### <span data-ttu-id="02428-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02428-124">-DefaultProfile</span></span>
<span data-ttu-id="02428-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02428-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02428-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="02428-126">-RecoveryPoint</span></span>
<span data-ttu-id="02428-127">Указывает точку восстановления, в которую нужно восстановить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="02428-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="02428-128">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="02428-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02428-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="02428-129">-ResolveConflict</span></span>
<span data-ttu-id="02428-130">Если восстановленный элемент также существует в месте назначения, используйте его, чтобы указать, следует ли переписывать или нет.</span><span class="sxs-lookup"><span data-stu-id="02428-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02428-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="02428-131">-SourceFilePath</span></span>
<span data-ttu-id="02428-132">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="02428-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="02428-133">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="02428-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="02428-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="02428-134">-SourceFileType</span></span>
<span data-ttu-id="02428-135">Используется для восстановления определенного элемента в общей папке.</span><span class="sxs-lookup"><span data-stu-id="02428-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="02428-136">Путь к элементу, который нужно восстановить в общей папке.</span><span class="sxs-lookup"><span data-stu-id="02428-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02428-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02428-137">-StorageAccountName</span></span>
<span data-ttu-id="02428-138">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="02428-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="02428-139">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="02428-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02428-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02428-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="02428-141">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="02428-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="02428-142">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="02428-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02428-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="02428-143">-TargetFileShareName</span></span>
<span data-ttu-id="02428-144">Файловый документ, на который должна быть восстановлена файловая общий доступ.</span><span class="sxs-lookup"><span data-stu-id="02428-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="02428-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="02428-145">-TargetFolder</span></span>
<span data-ttu-id="02428-146">Папка, в которой должен быть восстановлен файл общего доступа в targetFileShareName. Оставьте переменную пустой для восстановления в разделе корневая папка.</span><span class="sxs-lookup"><span data-stu-id="02428-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="02428-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02428-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="02428-148">Группа ресурсов, на которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="02428-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="02428-149">Применимо к резервному копированию ВМ с управляемыми дисками</span><span class="sxs-lookup"><span data-stu-id="02428-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="02428-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02428-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="02428-151">Учетная запись хранения, на которую нужно восстановить файловый общий доступ.</span><span class="sxs-lookup"><span data-stu-id="02428-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="02428-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="02428-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="02428-153">Используйте этот параметр, если нужно восстановить диски из точки восстановления в первоначальные учетные записи хранения.</span><span class="sxs-lookup"><span data-stu-id="02428-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="02428-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="02428-154">-VaultId</span></span>
<span data-ttu-id="02428-155">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="02428-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="02428-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="02428-156">-VaultLocation</span></span>
<span data-ttu-id="02428-157">Расположение хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="02428-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="02428-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02428-158">-Confirm</span></span>
<span data-ttu-id="02428-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02428-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02428-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02428-160">-WhatIf</span></span>
<span data-ttu-id="02428-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02428-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02428-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02428-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02428-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02428-163">CommonParameters</span></span>
<span data-ttu-id="02428-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02428-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02428-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02428-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02428-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02428-166">INPUTS</span></span>

### <span data-ttu-id="02428-167">System. String</span><span class="sxs-lookup"><span data-stu-id="02428-167">System.String</span></span>
<span data-ttu-id="02428-168">Параметры: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02428-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="02428-169">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="02428-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="02428-170">Параметры: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02428-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="02428-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02428-171">OUTPUTS</span></span>

### <span data-ttu-id="02428-172">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="02428-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="02428-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="02428-173">NOTES</span></span>

## <span data-ttu-id="02428-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02428-174">RELATED LINKS</span></span>

[<span data-ttu-id="02428-175">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="02428-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="02428-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="02428-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="02428-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="02428-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


