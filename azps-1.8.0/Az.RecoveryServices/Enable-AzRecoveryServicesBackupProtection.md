---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729750"
---
# <span data-ttu-id="48ed1-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="48ed1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="48ed1-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="48ed1-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="48ed1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48ed1-104">SYNTAX</span></span>

### <span data-ttu-id="48ed1-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48ed1-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ed1-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ed1-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ed1-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ed1-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ed1-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ed1-110">DESCRIPTION</span></span>
<span data-ttu-id="48ed1-111">Командлет **Enable-AzRecoveryServicesBackupProtection** задает политику защиты резервного копирования Azure для элемента.</span><span class="sxs-lookup"><span data-stu-id="48ed1-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="48ed1-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="48ed1-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="48ed1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48ed1-113">EXAMPLES</span></span>

### <span data-ttu-id="48ed1-114">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="48ed1-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="48ed1-115">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="48ed1-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="48ed1-116">Второй командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="48ed1-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="48ed1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48ed1-117">PARAMETERS</span></span>

### <span data-ttu-id="48ed1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ed1-118">-DefaultProfile</span></span>
<span data-ttu-id="48ed1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48ed1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48ed1-120">-Item</span><span class="sxs-lookup"><span data-stu-id="48ed1-120">-Item</span></span>
<span data-ttu-id="48ed1-121">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="48ed1-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="48ed1-122">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="48ed1-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="48ed1-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48ed1-123">-Name</span></span>
<span data-ttu-id="48ed1-124">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="48ed1-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="48ed1-125">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="48ed1-125">-Policy</span></span>
<span data-ttu-id="48ed1-126">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="48ed1-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="48ed1-127">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="48ed1-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ed1-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="48ed1-128">-ProtectableItem</span></span>
<span data-ttu-id="48ed1-129">Значение фильтра для состояния задания.</span><span class="sxs-lookup"><span data-stu-id="48ed1-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="48ed1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ed1-130">-ResourceGroupName</span></span>
<span data-ttu-id="48ed1-131">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48ed1-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="48ed1-132">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="48ed1-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="48ed1-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48ed1-133">-ServiceName</span></span>
<span data-ttu-id="48ed1-134">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="48ed1-134">Specifies the service name.</span></span>
<span data-ttu-id="48ed1-135">Указывайте этот параметр только для виртуальных машин ASM.</span><span class="sxs-lookup"><span data-stu-id="48ed1-135">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="48ed1-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48ed1-136">-StorageAccountName</span></span>
<span data-ttu-id="48ed1-137">Имя учетной записи хранилища для общего доступа к хранилищу файлов Azure</span><span class="sxs-lookup"><span data-stu-id="48ed1-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="48ed1-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="48ed1-138">-VaultId</span></span>
<span data-ttu-id="48ed1-139">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="48ed1-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="48ed1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48ed1-140">-Confirm</span></span>
<span data-ttu-id="48ed1-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48ed1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ed1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ed1-142">-WhatIf</span></span>
<span data-ttu-id="48ed1-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48ed1-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48ed1-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48ed1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ed1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ed1-145">CommonParameters</span></span>
<span data-ttu-id="48ed1-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48ed1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ed1-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ed1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ed1-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48ed1-148">INPUTS</span></span>

### <span data-ttu-id="48ed1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="48ed1-149">System.String</span></span>

### <span data-ttu-id="48ed1-150">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="48ed1-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="48ed1-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ed1-151">OUTPUTS</span></span>

### <span data-ttu-id="48ed1-152">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="48ed1-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="48ed1-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="48ed1-153">NOTES</span></span>

## <span data-ttu-id="48ed1-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48ed1-154">RELATED LINKS</span></span>

[<span data-ttu-id="48ed1-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="48ed1-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="48ed1-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="48ed1-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


