---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077704"
---
# <span data-ttu-id="c1266-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c1266-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1266-102">SYNOPSIS</span></span>
<span data-ttu-id="c1266-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c1266-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="c1266-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1266-104">SYNTAX</span></span>

### <span data-ttu-id="c1266-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1266-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1266-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1266-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1266-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1266-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1266-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1266-110">DESCRIPTION</span></span>
<span data-ttu-id="c1266-111">Командлет **Enable-AzRecoveryServicesBackupProtection** включает резервное копирование, связывая политику защиты с элементом.</span><span class="sxs-lookup"><span data-stu-id="c1266-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="c1266-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="c1266-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c1266-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1266-113">EXAMPLES</span></span>

### <span data-ttu-id="c1266-114">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="c1266-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="c1266-115">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="c1266-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="c1266-116">Второй командлет указывает дисковый LUN, резервную копию которого нужно создать, и сохраняет его в $inclusionDiskLUNS переменной.</span><span class="sxs-lookup"><span data-stu-id="c1266-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="c1266-117">Третий командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="c1266-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="c1266-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c1266-118">Example 2</span></span>

<span data-ttu-id="c1266-119">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c1266-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="c1266-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="c1266-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="c1266-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1266-121">PARAMETERS</span></span>

### <span data-ttu-id="c1266-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1266-122">-DefaultProfile</span></span>
<span data-ttu-id="c1266-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1266-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1266-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="c1266-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="c1266-125">Параметр для задания архивации только дисков ОС</span><span class="sxs-lookup"><span data-stu-id="c1266-125">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="c1266-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="c1266-126">-ExclusionDisksList</span></span>
<span data-ttu-id="c1266-127">Список дисковых устройств, которые нужно исключить из резервной копии, и остальные будут включены автоматически.</span><span class="sxs-lookup"><span data-stu-id="c1266-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="c1266-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="c1266-128">-InclusionDisksList</span></span>
<span data-ttu-id="c1266-129">Список дисковых LUN, которые должны быть включены в резервную копию, и остальные автоматически исключаются за исключением диска с ОС.</span><span class="sxs-lookup"><span data-stu-id="c1266-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="c1266-130">-Item</span><span class="sxs-lookup"><span data-stu-id="c1266-130">-Item</span></span>
<span data-ttu-id="c1266-131">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="c1266-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="c1266-132">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c1266-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="c1266-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1266-133">-Name</span></span>
<span data-ttu-id="c1266-134">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="c1266-134">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="c1266-135">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c1266-135">-Policy</span></span>
<span data-ttu-id="c1266-136">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="c1266-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="c1266-137">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c1266-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="c1266-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c1266-138">-ProtectableItem</span></span>
<span data-ttu-id="c1266-139">Указывает элемент, который должен быть защищен с помощью заданной политики.</span><span class="sxs-lookup"><span data-stu-id="c1266-139">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="c1266-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="c1266-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="c1266-141">Задает сброс параметров исключения диска, связанных с элементом</span><span class="sxs-lookup"><span data-stu-id="c1266-141">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="c1266-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1266-142">-ResourceGroupName</span></span>
<span data-ttu-id="c1266-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1266-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c1266-144">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="c1266-144">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="c1266-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c1266-145">-StorageAccountName</span></span>
<span data-ttu-id="c1266-146">Имя учетной записи хранилища для общего доступа к хранилищу файлов Azure</span><span class="sxs-lookup"><span data-stu-id="c1266-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="c1266-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c1266-147">-VaultId</span></span>
<span data-ttu-id="c1266-148">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="c1266-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c1266-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1266-149">-Confirm</span></span>
<span data-ttu-id="c1266-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1266-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1266-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1266-151">-WhatIf</span></span>
<span data-ttu-id="c1266-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1266-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="c1266-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1266-153">CommonParameters</span></span>
<span data-ttu-id="c1266-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1266-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1266-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1266-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1266-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1266-156">INPUTS</span></span>

### <span data-ttu-id="c1266-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c1266-157">System.String</span></span>

### <span data-ttu-id="c1266-158">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="c1266-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="c1266-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1266-159">OUTPUTS</span></span>

### <span data-ttu-id="c1266-160">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c1266-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c1266-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1266-161">NOTES</span></span>

## <span data-ttu-id="c1266-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1266-162">RELATED LINKS</span></span>

[<span data-ttu-id="c1266-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c1266-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c1266-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1266-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


