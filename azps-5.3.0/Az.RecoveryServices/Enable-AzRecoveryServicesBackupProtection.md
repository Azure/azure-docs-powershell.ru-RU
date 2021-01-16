---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424767"
---
# <span data-ttu-id="7a2c3-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="7a2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2c3-103">Включает резервное копирование элемента с помощью указанной политики защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="7a2c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a2c3-104">SYNTAX</span></span>

### <span data-ttu-id="7a2c3-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a2c3-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a2c3-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2c3-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2c3-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2c3-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a2c3-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a2c3-110">DESCRIPTION</span></span>
<span data-ttu-id="7a2c3-111">**Cmdlet Enable-AzRecoveryServicesBackupProtection** включает резервное копирование путем связывания политики защиты с элементом.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="7a2c3-112">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7a2c3-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a2c3-113">EXAMPLES</span></span>

### <span data-ttu-id="7a2c3-114">Пример 1. Защита резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="7a2c3-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="7a2c3-115">Первый cmdlet получает объект политики по умолчанию, а затем сохраняет его в $Pol переменной.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7a2c3-116">Второй cmdlet определяет коды LUNS диска, которые необходимо сделать сархивом, и их можно $inclusionDiskLUNS переменной.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="7a2c3-117">Третий cmdlet set the Backup protection policy for the ARM machine named V2VM using the policy in $Pol.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="7a2c3-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7a2c3-118">Example 2</span></span>

<span data-ttu-id="7a2c3-119">Включает резервное копирование элемента с помощью указанной политики защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="7a2c3-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="7a2c3-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="7a2c3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a2c3-121">PARAMETERS</span></span>

### <span data-ttu-id="7a2c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2c3-122">-DefaultProfile</span></span>
<span data-ttu-id="7a2c3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a2c3-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="7a2c3-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="7a2c3-125">Параметр для указания резервного копирования только дисков ОС</span><span class="sxs-lookup"><span data-stu-id="7a2c3-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7a2c3-126">-ExclusionDisksList</span></span>
<span data-ttu-id="7a2c3-127">Список кодов LUNS дисков, которые нужно исключить из резервного копирования, а остальные будут включены автоматически.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7a2c3-128">-InclusionDisksList</span></span>
<span data-ttu-id="7a2c3-129">Список кодов LUNS диска, которые нужно включить в резервное копирование, а остальные будут автоматически исключены, кроме диска ОС.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-130">-Item</span><span class="sxs-lookup"><span data-stu-id="7a2c3-130">-Item</span></span>
<span data-ttu-id="7a2c3-131">Элемент резервного копирования, для которого этот cmdlet обеспечивает защиту.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="7a2c3-132">Чтобы получить **azureRmRecoveryServicesBackupItem,** используйте Get-AzRecoveryServicesBackupItem управления.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-132">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-133">-Name</span><span class="sxs-lookup"><span data-stu-id="7a2c3-133">-Name</span></span>
<span data-ttu-id="7a2c3-134">Имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-135">-Политика</span><span class="sxs-lookup"><span data-stu-id="7a2c3-135">-Policy</span></span>
<span data-ttu-id="7a2c3-136">Определяет политику защиты, которую этот cmdlet связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="7a2c3-137">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy,** используйте Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7a2c3-138">-ProtectableItem</span></span>
<span data-ttu-id="7a2c3-139">Определяет элемент, который нужно защитить с помощью указанной политики.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="7a2c3-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="7a2c3-141">Указывает на сброс параметра исключения диска, связанного с элементом.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2c3-142">-ResourceGroupName</span></span>
<span data-ttu-id="7a2c3-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7a2c3-144">Укажите этот параметр только для ARM виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7a2c3-145">-StorageAccountName</span></span>
<span data-ttu-id="7a2c3-146">Имя учетной записи для файлового хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="7a2c3-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2c3-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7a2c3-147">-VaultId</span></span>
<span data-ttu-id="7a2c3-148">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7a2c3-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a2c3-149">-Confirm</span></span>
<span data-ttu-id="7a2c3-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2c3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2c3-151">-WhatIf</span></span>
<span data-ttu-id="7a2c3-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="7a2c3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2c3-153">CommonParameters</span></span>
<span data-ttu-id="7a2c3-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a2c3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2c3-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a2c3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2c3-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a2c3-156">INPUTS</span></span>

### <span data-ttu-id="7a2c3-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7a2c3-157">System.String</span></span>

### <span data-ttu-id="7a2c3-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="7a2c3-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7a2c3-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a2c3-159">OUTPUTS</span></span>

### <span data-ttu-id="7a2c3-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7a2c3-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7a2c3-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a2c3-161">NOTES</span></span>

## <span data-ttu-id="7a2c3-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a2c3-162">RELATED LINKS</span></span>

[<span data-ttu-id="7a2c3-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7a2c3-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7a2c3-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a2c3-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


