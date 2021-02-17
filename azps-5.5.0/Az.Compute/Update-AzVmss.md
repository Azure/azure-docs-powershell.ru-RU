---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233217"
---
# <span data-ttu-id="c6086-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-101">Update-AzVmss</span></span>

## <span data-ttu-id="c6086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6086-102">SYNOPSIS</span></span>
<span data-ttu-id="c6086-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="c6086-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6086-104">SYNTAX</span></span>

### <span data-ttu-id="c6086-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6086-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6086-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6086-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6086-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6086-107">DESCRIPTION</span></span>
<span data-ttu-id="c6086-108">При **настройке** набора виртуальных машин (VMSS) состояние набора виртуальных машин (VMSS) обновляется до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="c6086-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6086-109">EXAMPLES</span></span>

### <span data-ttu-id="c6086-110">Пример 1. Обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="c6086-111">Эта команда обновляет состояние VMSS под названием VMSS001, которая принадлежит к группе ресурсов Group001, до состояния локального объекта VMSS ($LocalVMSS).</span><span class="sxs-lookup"><span data-stu-id="c6086-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="c6086-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6086-112">PARAMETERS</span></span>

### <span data-ttu-id="c6086-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6086-113">-AsJob</span></span>
<span data-ttu-id="c6086-114">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c6086-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c6086-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="c6086-116">Определяет, следует ли автоматически применять обновления ОС для масштабирования экземпляров набора при обновлении изображения.</span><span class="sxs-lookup"><span data-stu-id="c6086-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="c6086-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="c6086-118">Время, на которое автоматические восстановления приостановлены из-за изменения состояния в VM.</span><span class="sxs-lookup"><span data-stu-id="c6086-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="c6086-119">Время отсрочки начинается после завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="c6086-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="c6086-120">Это помогает избежать ремонта по ошибке или по ошибке.</span><span class="sxs-lookup"><span data-stu-id="c6086-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="c6086-121">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c6086-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="c6086-122">Минимальный допустимый период отсрочки составляет 30 минут (PT30M), что также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6086-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="c6086-123">Максимальный допустимый период отсрочки составляет 90 минут (PT90M).</span><span class="sxs-lookup"><span data-stu-id="c6086-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="c6086-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="c6086-125">Следует ли включить диагностику загрузки в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="c6086-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="c6086-127">URI учетной записи хранения, используемой для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="c6086-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="c6086-128">-CustomData</span></span>
<span data-ttu-id="c6086-129">Указывает строку пользовательских данных с кодом базы 64.</span><span class="sxs-lookup"><span data-stu-id="c6086-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="c6086-130">Он декодироваться в двоичный массив, сохраненный в файле на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c6086-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="c6086-131">Максимальная длина двоичного массива составляет 65 535 тол.</span><span class="sxs-lookup"><span data-stu-id="c6086-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="c6086-132">Чтобы узнать, как использовать cloud-init для своего VM-решения, см. в этой теме использование cloud-init для настройки [VM-решения Linux во](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)время создания.</span><span class="sxs-lookup"><span data-stu-id="c6086-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6086-133">-DefaultProfile</span></span>
<span data-ttu-id="c6086-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6086-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6086-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="c6086-135">-DisableAutoRollback</span></span>
<span data-ttu-id="c6086-136">Отключение автоматического отката для политики обновления автоматической ОС</span><span class="sxs-lookup"><span data-stu-id="c6086-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="c6086-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="c6086-138">Указывает на то, что этот cmdlet отключает проверку подлинности паролем для Ос Linux.</span><span class="sxs-lookup"><span data-stu-id="c6086-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="c6086-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="c6086-140">Включив или отключив автоматическое восстановление на наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="c6086-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="c6086-142">Указывает, включены ли автоматические обновления на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c6086-143">-EncryptionAtHost</span></span>
<span data-ttu-id="c6086-144">Пользователь может использовать этот параметр в запросе, чтобы включить или отключить шифрование хоста для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c6086-145">-IdentityId</span></span>
<span data-ttu-id="c6086-146">Определяет список удостоверений пользователей, связанных с набором масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c6086-147">Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="c6086-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c6086-148">-IdentityType</span></span>
<span data-ttu-id="c6086-149">Определяет тип удостоверения, используемого для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="c6086-150">Тип SystemAssignedUserAssigned включает неявно созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="c6086-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="c6086-151">Тип "Нет" удаляет все удостоверения из набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="c6086-152">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c6086-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6086-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c6086-153">SystemAssigned</span></span>
- <span data-ttu-id="c6086-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c6086-154">UserAssigned</span></span>
- <span data-ttu-id="c6086-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="c6086-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="c6086-156">Нет</span><span class="sxs-lookup"><span data-stu-id="c6086-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="c6086-157">-ImageReferenceId</span></span>
<span data-ttu-id="c6086-158">Определяет ИД ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="c6086-158">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="c6086-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="c6086-160">Тип изображения виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="c6086-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="c6086-161">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="c6086-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="c6086-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="c6086-163">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6086-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="c6086-164">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c6086-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="c6086-165">-ImageReferenceSku</span></span>
<span data-ttu-id="c6086-166">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6086-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="c6086-167">Чтобы получить skus, используйте Get-AzVMImageSku-код.</span><span class="sxs-lookup"><span data-stu-id="c6086-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="c6086-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="c6086-169">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6086-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="c6086-170">Чтобы использовать последнюю версию, укажите последнюю версию, а не конкретную.</span><span class="sxs-lookup"><span data-stu-id="c6086-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="c6086-171">-ImageUri</span></span>
<span data-ttu-id="c6086-172">Определяет URI BLOB-данных для изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6086-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="c6086-173">VMSS создает диск операционной системы в том же контейнере изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6086-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c6086-174">-LicenseType</span></span>
<span data-ttu-id="c6086-175">Укажите тип лицензии, который можно установить для вашего сценария.</span><span class="sxs-lookup"><span data-stu-id="c6086-175">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c6086-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="c6086-177">Определяет тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c6086-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="c6086-178">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c6086-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6086-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="c6086-179">StandardLRS</span></span>
- <span data-ttu-id="c6086-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="c6086-180">PremiumLRS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c6086-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="c6086-182">Максимальный процент всех экземпляров виртуальных машин, которые будут одновременно обновлены путем пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="c6086-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="c6086-183">Поскольку это максимально неработоспособные экземпляры в предыдущих или будущих пакетах, процент экземпляров в пакете может снизиться, чтобы обеспечить более высокую надежность.</span><span class="sxs-lookup"><span data-stu-id="c6086-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="c6086-184">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="c6086-184">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="c6086-185">-MaxPrice</span></span>
<span data-ttu-id="c6086-186">Указывает максимальную цену, которую вы будете оплачивать для службы VM или VMSS с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c6086-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="c6086-187">Эта цена в долларах США.</span><span class="sxs-lookup"><span data-stu-id="c6086-187">This price is in US Dollars.</span></span> <span data-ttu-id="c6086-188">Эта цена будет сравниваться с текущей низкой ценой приоритета для размера VM.</span><span class="sxs-lookup"><span data-stu-id="c6086-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="c6086-189">Кроме того, цены сравниваются во время создания или обновления низкой приоритетной VM-или VMSS и операция будет работать только в том случае, если максимальная цена больше текущей цены с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c6086-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="c6086-190">Максимальное значение maxPrice также будет использоваться для создания обетовки VM или VMSS с низким приоритетом, если текущая цена с низким приоритетом выходит за пределы максимальной цены после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="c6086-191">Возможные значения: любое десятичее значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="c6086-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="c6086-192">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="c6086-192">Example: 0.01538.</span></span>  <span data-ttu-id="c6086-193">-1 указывает на то, что не следует переумелять VM или VMSS с низким приоритетом по ценам.</span><span class="sxs-lookup"><span data-stu-id="c6086-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="c6086-194">Кроме того, максимальная цена по умолчанию составляет -1, если она не предоставлена вами.</span><span class="sxs-lookup"><span data-stu-id="c6086-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c6086-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="c6086-196">Максимальный процент от общего числа экземпляров виртуальной машины в наборе, которые могут одновременно неработоспособно работать либо в результате обновления, либо из-за неработоспособного состояния виртуальной машины проверяется, пока не будет установлено обновление.</span><span class="sxs-lookup"><span data-stu-id="c6086-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="c6086-197">Это ограничение будет проверено перед запуском любого пакета.</span><span class="sxs-lookup"><span data-stu-id="c6086-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="c6086-198">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="c6086-198">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c6086-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="c6086-200">Максимальный процент обновленных экземпляров виртуальной машины, которые могут быть признаны неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="c6086-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="c6086-201">Эта проверка будет происходить после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="c6086-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="c6086-202">Если это процентное соотношение будет превышено, будут обновлены все изменения.</span><span class="sxs-lookup"><span data-stu-id="c6086-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="c6086-203">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="c6086-203">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="c6086-204">-OsDiskCaching</span></span>
<span data-ttu-id="c6086-205">Определяет режим кэшации диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c6086-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="c6086-206">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c6086-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6086-207">Нет</span><span class="sxs-lookup"><span data-stu-id="c6086-207">None</span></span>
- <span data-ttu-id="c6086-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c6086-208">ReadOnly</span></span>
- <span data-ttu-id="c6086-209">Значением по умолчанию readWrite является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="c6086-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="c6086-210">Если изменить значение кэшинга, будет перезапущена виртуальная машину.</span><span class="sxs-lookup"><span data-stu-id="c6086-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="c6086-211">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="c6086-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c6086-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="c6086-213">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="c6086-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="c6086-214">-Overprovision</span></span>
<span data-ttu-id="c6086-215">Указывает, будет ли cmdlet перепроцессом VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="c6086-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="c6086-217">Время ожидания между завершением обновления всех виртуальных машин одним пакетом и началом следующего.</span><span class="sxs-lookup"><span data-stu-id="c6086-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="c6086-218">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c6086-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="c6086-219">Значение по умолчанию — 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="c6086-219">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c6086-220">-PlanName</span></span>
<span data-ttu-id="c6086-221">Название плана.</span><span class="sxs-lookup"><span data-stu-id="c6086-221">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c6086-222">-PlanProduct</span></span>
<span data-ttu-id="c6086-223">Продукт плана.</span><span class="sxs-lookup"><span data-stu-id="c6086-223">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c6086-224">-PlanPromotionCode</span></span>
<span data-ttu-id="c6086-225">Указывает рекламный код плана.</span><span class="sxs-lookup"><span data-stu-id="c6086-225">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c6086-226">-PlanPublisher</span></span>
<span data-ttu-id="c6086-227">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="c6086-227">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="c6086-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="c6086-229">Указывает на то, следует ли заказать агент виртуальной машины на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c6086-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="c6086-231">The resource id of the Proximity Placement Group to use with this scale set.</span><span class="sxs-lookup"><span data-stu-id="c6086-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6086-232">-ResourceGroupName</span></span>
<span data-ttu-id="c6086-233">Имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="c6086-234">-ScaleInPolicy</span></span>
<span data-ttu-id="c6086-235">Правила, за которыми нужно следовать при масштабирования в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="c6086-236">Возможные значения: Default, 'OldestVM' и 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="c6086-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="c6086-237">При масштабе набора виртуальных машин набор "По умолчанию" сначала будет балансироваться в разных зонах, если он является набором золонного масштаба.</span><span class="sxs-lookup"><span data-stu-id="c6086-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="c6086-238">Затем он будет как можно остаток на балансе по всем доменам fault Domains.</span><span class="sxs-lookup"><span data-stu-id="c6086-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="c6086-239">В каждом домене ошибок будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c6086-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="c6086-240">При масштабе масштабирования в виртуальной машине выбирается "OldestVM", для удаления будут выбраны старые виртуальные машины, которые не защищены от масштаба.</span><span class="sxs-lookup"><span data-stu-id="c6086-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="c6086-241">Для наборов шкалы виртуальной машины, задаваемой в золевом аппарате, сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="c6086-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="c6086-242">В каждой зоне выбираются старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="c6086-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="c6086-243">При масштабе масштабирования набора виртуальных машин будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c6086-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="c6086-244">Для наборов шкалы виртуальной машины, задаваемой в золевом аппарате, сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="c6086-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="c6086-245">В каждой зоне для удаления будут выбраны новые не защищенные виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c6086-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="c6086-247">Определяет группу одного размещения.</span><span class="sxs-lookup"><span data-stu-id="c6086-247">Specifies the single placement group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="c6086-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="c6086-249">Указывает на то, что расширения не запускаются для лишних перезапроизводиных VMs.</span><span class="sxs-lookup"><span data-stu-id="c6086-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c6086-250">-SkuCapacity</span></span>
<span data-ttu-id="c6086-251">Количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-251">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c6086-252">-SkuName</span></span>
<span data-ttu-id="c6086-253">Определяет размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-253">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c6086-254">-SkuTier</span></span>
<span data-ttu-id="c6086-255">Определяет уровень службы VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="c6086-256">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c6086-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6086-257">Стандартный</span><span class="sxs-lookup"><span data-stu-id="c6086-257">Standard</span></span>
- <span data-ttu-id="c6086-258">Базовая</span><span class="sxs-lookup"><span data-stu-id="c6086-258">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6086-259">-Tag</span></span>
<span data-ttu-id="c6086-260">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="c6086-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c6086-261">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c6086-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c6086-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="c6086-263">Настраиваемая продолжительность удаления виртуальной машины (в минутах) может утвердить запланированное событие", прежде чем событие будет утверждено автоматически (по времени).</span><span class="sxs-lookup"><span data-stu-id="c6086-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="c6086-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="c6086-265">Указывает, включено ли событие "Завершенное запланированное время".</span><span class="sxs-lookup"><span data-stu-id="c6086-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c6086-266">-TimeZone</span></span>
<span data-ttu-id="c6086-267">Определяет часовой пояс для Ос Windows.</span><span class="sxs-lookup"><span data-stu-id="c6086-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="c6086-268">Например, по \" тихоокеанскому \" времени.</span><span class="sxs-lookup"><span data-stu-id="c6086-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="c6086-269">Возможные значения могут [быть](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="c6086-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="c6086-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="c6086-271">Флаг, который позволяет или отключает возможность иметь один или несколько управляемых дисков данных с типом учетной UltraSSD_LRS в наборе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6086-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="c6086-272">Управляемые диски с типом учетной UltraSSD_LRS можно добавить на VMSS, только если это свойство включено.</span><span class="sxs-lookup"><span data-stu-id="c6086-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c6086-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="c6086-274">В наборе масштабов указан режим обновления до виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c6086-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="c6086-275">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c6086-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6086-276">Автоматически</span><span class="sxs-lookup"><span data-stu-id="c6086-276">Automatic</span></span>
- <span data-ttu-id="c6086-277">Вручную</span><span class="sxs-lookup"><span data-stu-id="c6086-277">Manual</span></span>
- <span data-ttu-id="c6086-278">Вкатегов</span><span class="sxs-lookup"><span data-stu-id="c6086-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="c6086-279">-VhdContainer</span></span>
<span data-ttu-id="c6086-280">Определяет URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c6086-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c6086-282">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="c6086-283">Чтобы получить объект VMSS, используйте Get-AzVmss..</span><span class="sxs-lookup"><span data-stu-id="c6086-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="c6086-284">Этот виртуальный объект содержит обновленное состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6086-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c6086-285">-VMScaleSetName</span></span>
<span data-ttu-id="c6086-286">Указывает имя службы VMSS, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6086-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-287">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6086-287">-Confirm</span></span>
<span data-ttu-id="c6086-288">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6086-288">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6086-289">-WhatIf</span></span>
<span data-ttu-id="c6086-290">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6086-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6086-291">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6086-291">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6086-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6086-292">CommonParameters</span></span>
<span data-ttu-id="c6086-293">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6086-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6086-294">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6086-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6086-295">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6086-295">INPUTS</span></span>

### <span data-ttu-id="c6086-296">System.String</span><span class="sxs-lookup"><span data-stu-id="c6086-296">System.String</span></span>

### <span data-ttu-id="c6086-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="c6086-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c6086-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6086-298">System.Boolean</span></span>

## <span data-ttu-id="c6086-299">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6086-299">OUTPUTS</span></span>

### <span data-ttu-id="c6086-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="c6086-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c6086-301">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6086-301">NOTES</span></span>

## <span data-ttu-id="c6086-302">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6086-302">RELATED LINKS</span></span>

[<span data-ttu-id="c6086-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="c6086-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="c6086-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="c6086-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="c6086-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="c6086-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="c6086-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6086-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


