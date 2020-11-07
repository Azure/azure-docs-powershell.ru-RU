---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733818"
---
# <span data-ttu-id="88541-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="88541-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="88541-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88541-102">SYNOPSIS</span></span>
<span data-ttu-id="88541-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="88541-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88541-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88541-104">SYNTAX</span></span>

### <span data-ttu-id="88541-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88541-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88541-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="88541-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88541-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="88541-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88541-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="88541-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88541-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88541-109">DESCRIPTION</span></span>
<span data-ttu-id="88541-110">Командлет **Enable-AzureRmRecoveryServicesBackupProtection** задает политику защиты резервного копирования Azure для элемента.</span><span class="sxs-lookup"><span data-stu-id="88541-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="88541-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="88541-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="88541-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88541-112">EXAMPLES</span></span>

### <span data-ttu-id="88541-113">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="88541-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="88541-114">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="88541-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="88541-115">Второй командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="88541-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="88541-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88541-116">PARAMETERS</span></span>

### <span data-ttu-id="88541-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88541-117">-DefaultProfile</span></span>
<span data-ttu-id="88541-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88541-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88541-119">-Item</span><span class="sxs-lookup"><span data-stu-id="88541-119">-Item</span></span>
<span data-ttu-id="88541-120">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="88541-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="88541-121">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="88541-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="88541-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88541-122">-Name</span></span>
<span data-ttu-id="88541-123">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="88541-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="88541-124">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="88541-124">-Policy</span></span>
<span data-ttu-id="88541-125">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="88541-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="88541-126">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="88541-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="88541-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88541-127">-ResourceGroupName</span></span>
<span data-ttu-id="88541-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88541-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="88541-129">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="88541-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="88541-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="88541-130">-ServiceName</span></span>
<span data-ttu-id="88541-131">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="88541-131">Specifies the service name.</span></span>
<span data-ttu-id="88541-132">Указывайте этот параметр только для виртуальных машин ASM.</span><span class="sxs-lookup"><span data-stu-id="88541-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="88541-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="88541-133">-StorageAccountName</span></span>
<span data-ttu-id="88541-134">Имя учетной записи хранилища для общего доступа к хранилищу файлов Azure</span><span class="sxs-lookup"><span data-stu-id="88541-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88541-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="88541-135">-VaultId</span></span>
<span data-ttu-id="88541-136">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="88541-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="88541-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88541-137">-Confirm</span></span>
<span data-ttu-id="88541-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88541-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88541-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88541-139">-WhatIf</span></span>
<span data-ttu-id="88541-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88541-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88541-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88541-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88541-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88541-142">CommonParameters</span></span>
<span data-ttu-id="88541-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88541-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88541-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88541-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88541-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88541-145">INPUTS</span></span>

### <span data-ttu-id="88541-146">System. String</span><span class="sxs-lookup"><span data-stu-id="88541-146">System.String</span></span>
<span data-ttu-id="88541-147">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88541-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="88541-148">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="88541-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="88541-149">Параметры: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88541-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="88541-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88541-150">OUTPUTS</span></span>

### <span data-ttu-id="88541-151">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="88541-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="88541-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="88541-152">NOTES</span></span>

## <span data-ttu-id="88541-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88541-153">RELATED LINKS</span></span>

[<span data-ttu-id="88541-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="88541-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="88541-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="88541-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


