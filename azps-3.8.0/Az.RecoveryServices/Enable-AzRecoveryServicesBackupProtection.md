---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912720"
---
# <span data-ttu-id="da2f0-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="da2f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="da2f0-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="da2f0-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="da2f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da2f0-104">SYNTAX</span></span>

### <span data-ttu-id="da2f0-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da2f0-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da2f0-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da2f0-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da2f0-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da2f0-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da2f0-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da2f0-110">DESCRIPTION</span></span>
<span data-ttu-id="da2f0-111">Командлет **Enable-AzRecoveryServicesBackupProtection** задает политику защиты резервного копирования Azure для элемента.</span><span class="sxs-lookup"><span data-stu-id="da2f0-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="da2f0-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="da2f0-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="da2f0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da2f0-113">EXAMPLES</span></span>

### <span data-ttu-id="da2f0-114">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="da2f0-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="da2f0-115">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="da2f0-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="da2f0-116">Второй командлет указывает дисковый LUN, резервную копию которого нужно создать, и сохраняет его в $inclusionDiskLUNS переменной.</span><span class="sxs-lookup"><span data-stu-id="da2f0-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="da2f0-117">Третий командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="da2f0-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="da2f0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da2f0-118">PARAMETERS</span></span>

### <span data-ttu-id="da2f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da2f0-119">-DefaultProfile</span></span>
<span data-ttu-id="da2f0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da2f0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da2f0-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="da2f0-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="da2f0-122">Параметр для задания архивации только дисков ОС</span><span class="sxs-lookup"><span data-stu-id="da2f0-122">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="da2f0-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="da2f0-123">-ExclusionDisksList</span></span>
<span data-ttu-id="da2f0-124">Список дисковых устройств, которые нужно исключить из резервной копии</span><span class="sxs-lookup"><span data-stu-id="da2f0-124">List of Disk LUNs to exclude in backup</span></span>

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

### <span data-ttu-id="da2f0-125">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="da2f0-125">-InclusionDisksList</span></span>
<span data-ttu-id="da2f0-126">Список дисковых устройств, которые нужно включить в резервную копию</span><span class="sxs-lookup"><span data-stu-id="da2f0-126">List of Disk LUNs to include in backup</span></span>

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

### <span data-ttu-id="da2f0-127">-Item</span><span class="sxs-lookup"><span data-stu-id="da2f0-127">-Item</span></span>
<span data-ttu-id="da2f0-128">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="da2f0-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="da2f0-129">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="da2f0-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="da2f0-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da2f0-130">-Name</span></span>
<span data-ttu-id="da2f0-131">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="da2f0-131">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="da2f0-132">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="da2f0-132">-Policy</span></span>
<span data-ttu-id="da2f0-133">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="da2f0-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="da2f0-134">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="da2f0-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="da2f0-135">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="da2f0-135">-ProtectableItem</span></span>
<span data-ttu-id="da2f0-136">Значение фильтра для состояния задания.</span><span class="sxs-lookup"><span data-stu-id="da2f0-136">Filter value for status of job.</span></span>

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

### <span data-ttu-id="da2f0-137">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="da2f0-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="da2f0-138">Задает сброс параметров исключения диска, связанных с элементом</span><span class="sxs-lookup"><span data-stu-id="da2f0-138">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="da2f0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da2f0-139">-ResourceGroupName</span></span>
<span data-ttu-id="da2f0-140">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da2f0-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="da2f0-141">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="da2f0-141">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="da2f0-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da2f0-142">-ServiceName</span></span>
<span data-ttu-id="da2f0-143">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="da2f0-143">Specifies the service name.</span></span>
<span data-ttu-id="da2f0-144">Указывайте этот параметр только для виртуальных машин ASM.</span><span class="sxs-lookup"><span data-stu-id="da2f0-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da2f0-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="da2f0-145">-StorageAccountName</span></span>
<span data-ttu-id="da2f0-146">Имя учетной записи хранилища для общего доступа к хранилищу файлов Azure</span><span class="sxs-lookup"><span data-stu-id="da2f0-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="da2f0-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="da2f0-147">-VaultId</span></span>
<span data-ttu-id="da2f0-148">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="da2f0-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="da2f0-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da2f0-149">-Confirm</span></span>
<span data-ttu-id="da2f0-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da2f0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da2f0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da2f0-151">-WhatIf</span></span>
<span data-ttu-id="da2f0-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da2f0-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da2f0-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da2f0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da2f0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2f0-154">CommonParameters</span></span>
<span data-ttu-id="da2f0-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da2f0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2f0-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da2f0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2f0-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da2f0-157">INPUTS</span></span>

### <span data-ttu-id="da2f0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="da2f0-158">System.String</span></span>

### <span data-ttu-id="da2f0-159">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="da2f0-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="da2f0-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da2f0-160">OUTPUTS</span></span>

### <span data-ttu-id="da2f0-161">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="da2f0-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="da2f0-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="da2f0-162">NOTES</span></span>

## <span data-ttu-id="da2f0-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da2f0-163">RELATED LINKS</span></span>

[<span data-ttu-id="da2f0-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="da2f0-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="da2f0-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da2f0-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


