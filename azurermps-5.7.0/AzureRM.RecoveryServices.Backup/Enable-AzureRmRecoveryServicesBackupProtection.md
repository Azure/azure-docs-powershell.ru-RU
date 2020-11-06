---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558963"
---
# <span data-ttu-id="a8f3c-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a8f3c-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="a8f3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f3c-103">Включение резервного копирования для элемента с указанной политикой защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8f3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8f3c-104">SYNTAX</span></span>

### <span data-ttu-id="a8f3c-105">AzureVMComputeEnableProtection (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8f3c-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f3c-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="a8f3c-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f3c-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="a8f3c-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f3c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8f3c-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f3c-109">Командлет **Enable-AzureRmRecoveryServicesBackupProtection** задает политику защиты резервного копирования Azure для элемента.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="a8f3c-110">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a8f3c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8f3c-111">EXAMPLES</span></span>

### <span data-ttu-id="a8f3c-112">Пример 1: Включение защиты резервных копий для элемента</span><span class="sxs-lookup"><span data-stu-id="a8f3c-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="a8f3c-113">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="a8f3c-114">Второй командлет задает политику защиты резервного копирования для виртуальной машины ARM с именем V2VM, используя политику в $Pol.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="a8f3c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8f3c-115">PARAMETERS</span></span>

### <span data-ttu-id="a8f3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f3c-116">-DefaultProfile</span></span>
<span data-ttu-id="a8f3c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-118">-Item</span><span class="sxs-lookup"><span data-stu-id="a8f3c-118">-Item</span></span>
<span data-ttu-id="a8f3c-119">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="a8f3c-120">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8f3c-121">-Name</span></span>
<span data-ttu-id="a8f3c-122">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a8f3c-123">-Policy</span></span>
<span data-ttu-id="a8f3c-124">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="a8f3c-125">Чтобы получить объект **AzureRmRecoveryServicesBackupProtectionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f3c-126">-ResourceGroupName</span></span>
<span data-ttu-id="a8f3c-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="a8f3c-128">Указывайте этот параметр только для виртуальных машин ARM.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8f3c-129">-ServiceName</span></span>
<span data-ttu-id="a8f3c-130">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-130">Specifies the service name.</span></span>
<span data-ttu-id="a8f3c-131">Указывайте этот параметр только для виртуальных машин ASM.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8f3c-132">-Confirm</span></span>
<span data-ttu-id="a8f3c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f3c-134">-WhatIf</span></span>
<span data-ttu-id="a8f3c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8f3c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f3c-137">CommonParameters</span></span>
<span data-ttu-id="a8f3c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f3c-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f3c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f3c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8f3c-140">INPUTS</span></span>

### <span data-ttu-id="a8f3c-141">ItemBase</span><span class="sxs-lookup"><span data-stu-id="a8f3c-141">ItemBase</span></span>
<span data-ttu-id="a8f3c-142">Параметр "элемент" принимает значение типа "ItemBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8f3c-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="a8f3c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8f3c-143">OUTPUTS</span></span>

### <span data-ttu-id="a8f3c-144">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a8f3c-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a8f3c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8f3c-145">NOTES</span></span>

## <span data-ttu-id="a8f3c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8f3c-146">RELATED LINKS</span></span>

[<span data-ttu-id="a8f3c-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a8f3c-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="a8f3c-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a8f3c-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


