---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227121"
---
# <span data-ttu-id="b1b58-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="b1b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b58-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b58-103">Включает резервное копирование элемента с помощью указанной политики защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1b58-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="b1b58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1b58-104">SYNTAX</span></span>

### <span data-ttu-id="b1b58-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1b58-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b58-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b58-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b58-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b58-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1b58-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b58-110">DESCRIPTION</span></span>
<span data-ttu-id="b1b58-111">**Cmdlet Enable-AzRecoveryServicesBackupProtection** включает резервное копирование путем связывания политики защиты с элементом.</span><span class="sxs-lookup"><span data-stu-id="b1b58-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="b1b58-112">Если код политики не существует или элемент резервной копии не связан с какой-либо политикой, эта команда будет ожидать код политики.</span><span class="sxs-lookup"><span data-stu-id="b1b58-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="b1b58-113">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="b1b58-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b1b58-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1b58-114">EXAMPLES</span></span>

### <span data-ttu-id="b1b58-115">Пример 1. Защита резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="b1b58-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="b1b58-116">Первый cmdlet получает объект политики по умолчанию, а затем сохраняет его в $Pol переменной.</span><span class="sxs-lookup"><span data-stu-id="b1b58-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="b1b58-117">Второй cmdlet указывает, какие коды luNs диска необходимо сделать сархивом и которые будут $inclusionDiskLUNS переменной.</span><span class="sxs-lookup"><span data-stu-id="b1b58-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="b1b58-118">Третий cmdlet set the Backup protection policy for the ARM machine named V2VM using the policy in $Pol.</span><span class="sxs-lookup"><span data-stu-id="b1b58-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="b1b58-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1b58-119">Example 2</span></span>

<span data-ttu-id="b1b58-120">Включает резервное копирование элемента с помощью указанной политики защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1b58-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="b1b58-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b1b58-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="b1b58-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1b58-122">PARAMETERS</span></span>

### <span data-ttu-id="b1b58-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b58-123">-DefaultProfile</span></span>
<span data-ttu-id="b1b58-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b58-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b58-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="b1b58-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="b1b58-126">Параметр для указания резервного копирования только дисков ОС</span><span class="sxs-lookup"><span data-stu-id="b1b58-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="b1b58-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="b1b58-127">-ExclusionDisksList</span></span>
<span data-ttu-id="b1b58-128">Список кодов LUNS дисков, которые нужно исключить из резервного копирования, а остальные будут включены автоматически.</span><span class="sxs-lookup"><span data-stu-id="b1b58-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="b1b58-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="b1b58-129">-InclusionDisksList</span></span>
<span data-ttu-id="b1b58-130">Список кодов LUNS диска, которые нужно включить в резервное копирование, а остальные будут автоматически исключены, кроме диска ОС.</span><span class="sxs-lookup"><span data-stu-id="b1b58-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="b1b58-131">-Item</span><span class="sxs-lookup"><span data-stu-id="b1b58-131">-Item</span></span>
<span data-ttu-id="b1b58-132">Элемент резервного копирования, для которого этот cmdlet обеспечивает защиту.</span><span class="sxs-lookup"><span data-stu-id="b1b58-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="b1b58-133">Чтобы получить **azureRmRecoveryServicesBackupItem,** используйте Get-AzRecoveryServicesBackupItem управления.</span><span class="sxs-lookup"><span data-stu-id="b1b58-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="b1b58-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b1b58-134">-Name</span></span>
<span data-ttu-id="b1b58-135">Имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b1b58-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="b1b58-136">-Политика</span><span class="sxs-lookup"><span data-stu-id="b1b58-136">-Policy</span></span>
<span data-ttu-id="b1b58-137">Определяет политику защиты, которую этот cmdlet связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="b1b58-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="b1b58-138">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy,** используйте Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b1b58-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="b1b58-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b1b58-139">-ProtectableItem</span></span>
<span data-ttu-id="b1b58-140">Определяет элемент, который нужно защитить с помощью указанной политики.</span><span class="sxs-lookup"><span data-stu-id="b1b58-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="b1b58-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="b1b58-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="b1b58-142">Указывает на сброс параметра исключения диска, связанного с элементом.</span><span class="sxs-lookup"><span data-stu-id="b1b58-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="b1b58-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b58-143">-ResourceGroupName</span></span>
<span data-ttu-id="b1b58-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1b58-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b1b58-145">Укажите этот параметр только для ARM виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b1b58-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="b1b58-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1b58-146">-StorageAccountName</span></span>
<span data-ttu-id="b1b58-147">Имя учетной записи для файлового хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b1b58-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="b1b58-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b1b58-148">-VaultId</span></span>
<span data-ttu-id="b1b58-149">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b1b58-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b1b58-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1b58-150">-Confirm</span></span>
<span data-ttu-id="b1b58-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b58-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b58-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b58-152">-WhatIf</span></span>
<span data-ttu-id="b1b58-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b58-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="b1b58-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b58-154">CommonParameters</span></span>
<span data-ttu-id="b1b58-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b58-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b58-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1b58-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b58-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1b58-157">INPUTS</span></span>

### <span data-ttu-id="b1b58-158">System.String</span><span class="sxs-lookup"><span data-stu-id="b1b58-158">System.String</span></span>

### <span data-ttu-id="b1b58-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="b1b58-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="b1b58-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1b58-160">OUTPUTS</span></span>

### <span data-ttu-id="b1b58-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="b1b58-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b1b58-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1b58-162">NOTES</span></span>

## <span data-ttu-id="b1b58-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1b58-163">RELATED LINKS</span></span>

[<span data-ttu-id="b1b58-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b1b58-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="b1b58-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1b58-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


