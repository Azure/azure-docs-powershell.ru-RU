---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015395"
---
# <span data-ttu-id="2a409-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-101">Update-AzVmss</span></span>

## <span data-ttu-id="2a409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a409-102">SYNOPSIS</span></span>
<span data-ttu-id="2a409-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="2a409-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a409-104">SYNTAX</span></span>

### <span data-ttu-id="2a409-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a409-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="2a409-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a409-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="2a409-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a409-107">DESCRIPTION</span></span>
<span data-ttu-id="2a409-108">При **настройке** набора виртуальных машин (VMSS) состояние набора виртуальных машин (VMSS) обновляется до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="2a409-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a409-109">EXAMPLES</span></span>

### <span data-ttu-id="2a409-110">Пример 1. Обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="2a409-111">Эта команда обновляет состояние VMSS под названием VMSS001, которая принадлежит к группе ресурсов Group001, до состояния локального объекта VMSS ($LocalVMSS).</span><span class="sxs-lookup"><span data-stu-id="2a409-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="2a409-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a409-112">PARAMETERS</span></span>

### <span data-ttu-id="2a409-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a409-113">-AsJob</span></span>
<span data-ttu-id="2a409-114">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a409-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2a409-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2a409-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="2a409-116">Определяет, следует ли автоматически применять обновления ОС для масштабирования экземпляров набора в скользячем режиме при обновлении изображения.</span><span class="sxs-lookup"><span data-stu-id="2a409-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="2a409-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="2a409-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="2a409-118">Время, на которое автоматические восстановления приостановлены из-за изменения состояния в VM.</span><span class="sxs-lookup"><span data-stu-id="2a409-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="2a409-119">Время отсрочки начинается после завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="2a409-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="2a409-120">Это помогает избежать ремонта по ошибке или по ошибке.</span><span class="sxs-lookup"><span data-stu-id="2a409-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="2a409-121">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2a409-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="2a409-122">Минимальный допустимый период отсрочки составляет 30 минут (PT30M), что также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a409-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="2a409-123">Максимальный допустимый период отсрочки составляет 90 минут (PT90M).</span><span class="sxs-lookup"><span data-stu-id="2a409-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="2a409-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="2a409-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="2a409-125">Следует ли включить диагностику загрузки в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2a409-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="2a409-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="2a409-127">URI учетной записи хранения, используемой для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="2a409-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="2a409-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="2a409-128">-CustomData</span></span>
<span data-ttu-id="2a409-129">Указывает строку пользовательских данных с кодом базы 64.</span><span class="sxs-lookup"><span data-stu-id="2a409-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="2a409-130">Он декодироваться в двоичный массив, сохраненный в файле на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2a409-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="2a409-131">Максимальная длина двоичного массива составляет 65 535 тол.</span><span class="sxs-lookup"><span data-stu-id="2a409-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="2a409-132">Чтобы узнать, как использовать cloud-init для своего VM-решения, см. в этой теме использование cloud-init для настройки [VM-решения Linux во](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)время создания.</span><span class="sxs-lookup"><span data-stu-id="2a409-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="2a409-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a409-133">-DefaultProfile</span></span>
<span data-ttu-id="2a409-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a409-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a409-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="2a409-135">-DisableAutoRollback</span></span>
<span data-ttu-id="2a409-136">Отключение автоматического отката для политики обновления автоматической ОС</span><span class="sxs-lookup"><span data-stu-id="2a409-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="2a409-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="2a409-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="2a409-138">Указывает на то, что этот cmdlet отключает проверку подлинности паролем для Ос Linux.</span><span class="sxs-lookup"><span data-stu-id="2a409-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="2a409-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="2a409-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="2a409-140">Включив или отключив автоматическое восстановление на наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2a409-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="2a409-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="2a409-142">Указывает, включены ли автоматические обновления на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="2a409-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="2a409-143">-EncryptionAtHost</span></span>
<span data-ttu-id="2a409-144">Пользователь может использовать этот параметр в запросе, чтобы включить или отключить шифрование хоста для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="2a409-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2a409-145">-IdentityId</span></span>
<span data-ttu-id="2a409-146">Определяет список удостоверений пользователей, связанных с набором масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2a409-147">Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="2a409-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2a409-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2a409-148">-IdentityType</span></span>
<span data-ttu-id="2a409-149">Определяет тип удостоверения, используемого для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="2a409-150">Тип SystemAssignedUserAssigned включает неявно созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="2a409-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="2a409-151">Тип "Нет" удаляет все удостоверения из набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="2a409-152">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a409-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a409-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2a409-153">SystemAssigned</span></span>
- <span data-ttu-id="2a409-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="2a409-154">UserAssigned</span></span>
- <span data-ttu-id="2a409-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="2a409-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="2a409-156">Нет</span><span class="sxs-lookup"><span data-stu-id="2a409-156">None</span></span>

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

### <span data-ttu-id="2a409-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="2a409-157">-ImageReferenceId</span></span>
<span data-ttu-id="2a409-158">Определяет ИД ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="2a409-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="2a409-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="2a409-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="2a409-160">Тип изображения виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="2a409-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="2a409-161">Чтобы получить предложение для изображения, воспользуйтесь Get-AzVMImageOffer- и рисунками.</span><span class="sxs-lookup"><span data-stu-id="2a409-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="2a409-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="2a409-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="2a409-163">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="2a409-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2a409-164">Чтобы получить издателя, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2a409-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2a409-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="2a409-165">-ImageReferenceSku</span></span>
<span data-ttu-id="2a409-166">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="2a409-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="2a409-167">Чтобы получить skus, используйте Get-AzVMImageSku-код.</span><span class="sxs-lookup"><span data-stu-id="2a409-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="2a409-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="2a409-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="2a409-169">Определяет версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="2a409-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="2a409-170">Чтобы использовать последнюю версию, укажите последнюю версию, а не конкретную.</span><span class="sxs-lookup"><span data-stu-id="2a409-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="2a409-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="2a409-171">-ImageUri</span></span>
<span data-ttu-id="2a409-172">Определяет URI BLOB-адреса для изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a409-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="2a409-173">VMSS создает диск операционной системы в том же контейнере изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a409-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="2a409-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2a409-174">-LicenseType</span></span>
<span data-ttu-id="2a409-175">Укажите тип лицензии, который будет выводить на себя.</span><span class="sxs-lookup"><span data-stu-id="2a409-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="2a409-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2a409-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="2a409-177">Определяет тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="2a409-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="2a409-178">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a409-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a409-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="2a409-179">StandardLRS</span></span>
- <span data-ttu-id="2a409-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="2a409-180">PremiumLRS</span></span>

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

### <span data-ttu-id="2a409-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2a409-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="2a409-182">Максимальный процент всех экземпляров виртуальных машин, которые будут одновременно обновлены путем пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="2a409-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="2a409-183">Поскольку это максимально неработоспособные экземпляры в предыдущих или будущих пакетах, процент экземпляров в пакете может снизиться, чтобы обеспечить более высокую надежность.</span><span class="sxs-lookup"><span data-stu-id="2a409-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="2a409-184">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="2a409-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2a409-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="2a409-185">-MaxPrice</span></span>
<span data-ttu-id="2a409-186">Указывает максимальную цену, которую вы будете оплачивать для службы VM или VMSS с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="2a409-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="2a409-187">Эта цена в долларах США.</span><span class="sxs-lookup"><span data-stu-id="2a409-187">This price is in US Dollars.</span></span> <span data-ttu-id="2a409-188">Эта цена будет сравниваться с текущей низкой ценой приоритета для размера VM.</span><span class="sxs-lookup"><span data-stu-id="2a409-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="2a409-189">Кроме того, цены сравниваются во время создания или обновления низкой приоритетной VM-или VMSS и операция будет работать только в том случае, если максимальная цена больше текущей цены с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="2a409-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="2a409-190">Максимальное значение maxPrice также будет использоваться для создания обетовки VM или VMSS с низким приоритетом, если текущая цена с низким приоритетом выходит за пределы максимальной цены после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="2a409-191">Возможные значения: любое десятичее значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="2a409-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="2a409-192">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="2a409-192">Example: 0.01538.</span></span>  <span data-ttu-id="2a409-193">-1 указывает на то, что не следует переумелять VM или VMSS с низким приоритетом по ценам.</span><span class="sxs-lookup"><span data-stu-id="2a409-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="2a409-194">Кроме того, максимальная цена по умолчанию составляет -1, если она не предоставлена вами.</span><span class="sxs-lookup"><span data-stu-id="2a409-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="2a409-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2a409-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="2a409-196">Максимальный процент от общего числа экземпляров виртуальной машины в наборе, которые могут быть одновременно неработоспособными в результате обновления или из-за неработоспособного состояния с помощью проверки состояния виртуальной машины перед обновлением.</span><span class="sxs-lookup"><span data-stu-id="2a409-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="2a409-197">Это ограничение будет проверено перед запуском любого пакета.</span><span class="sxs-lookup"><span data-stu-id="2a409-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="2a409-198">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="2a409-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2a409-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2a409-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="2a409-200">Максимальный процент обновленных экземпляров виртуальной машины, которые могут быть признаны неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="2a409-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="2a409-201">Эта проверка будет происходить после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="2a409-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="2a409-202">Если это процентное соотношение будет превышено, будут обновлены все изменения.</span><span class="sxs-lookup"><span data-stu-id="2a409-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="2a409-203">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="2a409-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2a409-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="2a409-204">-OsDiskCaching</span></span>
<span data-ttu-id="2a409-205">Определяет режим кэшации диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2a409-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="2a409-206">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a409-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a409-207">Нет</span><span class="sxs-lookup"><span data-stu-id="2a409-207">None</span></span>
- <span data-ttu-id="2a409-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2a409-208">ReadOnly</span></span>
- <span data-ttu-id="2a409-209">Значением по умолчанию readWrite является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2a409-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="2a409-210">Если изменить значение кэшинга, будет перезапущена виртуальная машину.</span><span class="sxs-lookup"><span data-stu-id="2a409-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="2a409-211">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="2a409-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="2a409-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2a409-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="2a409-213">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="2a409-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="2a409-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="2a409-214">-Overprovision</span></span>
<span data-ttu-id="2a409-215">Указывает, является ли cmdlet перенастройка VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="2a409-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="2a409-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="2a409-217">Время ожидания между завершением обновления всех виртуальных машин одним пакетом и началом следующего.</span><span class="sxs-lookup"><span data-stu-id="2a409-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="2a409-218">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2a409-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="2a409-219">Значение по умолчанию — 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="2a409-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="2a409-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2a409-220">-PlanName</span></span>
<span data-ttu-id="2a409-221">Название плана.</span><span class="sxs-lookup"><span data-stu-id="2a409-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="2a409-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="2a409-222">-PlanProduct</span></span>
<span data-ttu-id="2a409-223">Продукт плана.</span><span class="sxs-lookup"><span data-stu-id="2a409-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="2a409-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="2a409-224">-PlanPromotionCode</span></span>
<span data-ttu-id="2a409-225">Определяет рекламный код плана.</span><span class="sxs-lookup"><span data-stu-id="2a409-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="2a409-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2a409-226">-PlanPublisher</span></span>
<span data-ttu-id="2a409-227">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="2a409-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="2a409-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="2a409-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="2a409-229">Указывает на то, следует ли заказать агент виртуальной машины на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="2a409-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="2a409-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="2a409-231">The resource id of the Proximity Placement Group to use with this scale set.</span><span class="sxs-lookup"><span data-stu-id="2a409-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="2a409-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a409-232">-ResourceGroupName</span></span>
<span data-ttu-id="2a409-233">Имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="2a409-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="2a409-234">-ScaleInPolicy</span></span>
<span data-ttu-id="2a409-235">Правила, которые следует соблюдать при масштабирование в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="2a409-236">Возможные значения: Default, 'OldestVM' и 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="2a409-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="2a409-237">При масштабе набора виртуальных машин набор "По умолчанию" сначала будет балансироваться в разных зонах, если он является набором золального шкалы.</span><span class="sxs-lookup"><span data-stu-id="2a409-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="2a409-238">Затем он будет как можно остаток на балансе по всем доменам fault Domains.</span><span class="sxs-lookup"><span data-stu-id="2a409-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="2a409-239">В каждом домене ошибок будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2a409-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="2a409-240">При масштабирования набора виртуальных машин "OldestVM" будут выбраны старые виртуальные машины, которые не защищены от масштаба.</span><span class="sxs-lookup"><span data-stu-id="2a409-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="2a409-241">Для наборов шкалы виртуальной машины, задаваемой в золевом аппарате, сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="2a409-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="2a409-242">В каждой зоне выбираются старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="2a409-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="2a409-243">При масштабе масштабирования набора виртуальных машин будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2a409-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="2a409-244">Для наборов шкалы виртуальной машины, задаваемой в золевом аппарате, сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="2a409-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="2a409-245">В каждой зоне для удаления будут выбраны новые не защищенные виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="2a409-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2a409-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="2a409-247">Определяет группу одного размещения.</span><span class="sxs-lookup"><span data-stu-id="2a409-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="2a409-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="2a409-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="2a409-249">Указывает, что расширения не запускаются для лишних перезапроизводиных VMs.</span><span class="sxs-lookup"><span data-stu-id="2a409-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="2a409-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2a409-250">-SkuCapacity</span></span>
<span data-ttu-id="2a409-251">Количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="2a409-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2a409-252">-SkuName</span></span>
<span data-ttu-id="2a409-253">Определяет размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="2a409-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2a409-254">-SkuTier</span></span>
<span data-ttu-id="2a409-255">Определяет уровень службы VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="2a409-256">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a409-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a409-257">Стандартный</span><span class="sxs-lookup"><span data-stu-id="2a409-257">Standard</span></span>
- <span data-ttu-id="2a409-258">Базовая</span><span class="sxs-lookup"><span data-stu-id="2a409-258">Basic</span></span>

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

### <span data-ttu-id="2a409-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a409-259">-Tag</span></span>
<span data-ttu-id="2a409-260">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="2a409-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a409-261">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2a409-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a409-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2a409-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="2a409-263">Настраиваемая продолжительность удаления виртуальной машины (в минутах) может утверждать событие "Завершить запланированный", прежде чем событие будет утверждено автоматически (по времени).</span><span class="sxs-lookup"><span data-stu-id="2a409-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="2a409-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="2a409-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="2a409-265">Указывает, включено ли событие "Завершенное запланированное время".</span><span class="sxs-lookup"><span data-stu-id="2a409-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="2a409-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="2a409-266">-TimeZone</span></span>
<span data-ttu-id="2a409-267">Определяет часовой пояс для ос Windows.</span><span class="sxs-lookup"><span data-stu-id="2a409-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="2a409-268">Например, по \" тихоокеанскому времени. \"</span><span class="sxs-lookup"><span data-stu-id="2a409-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="2a409-269">Возможные значения могут [быть](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="2a409-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="2a409-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="2a409-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="2a409-271">Флаг, который позволяет или отключает возможность иметь один или несколько управляемых дисков данных с типом учетной UltraSSD_LRS в наборе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a409-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="2a409-272">Управляемые диски с типом учетной UltraSSD_LRS можно добавить на VMSS, только если это свойство включено.</span><span class="sxs-lookup"><span data-stu-id="2a409-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="2a409-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="2a409-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="2a409-274">В наборе масштабов указан режим обновления до виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2a409-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="2a409-275">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a409-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a409-276">Автоматически</span><span class="sxs-lookup"><span data-stu-id="2a409-276">Automatic</span></span>
- <span data-ttu-id="2a409-277">Вручную</span><span class="sxs-lookup"><span data-stu-id="2a409-277">Manual</span></span>
- <span data-ttu-id="2a409-278">Вкатегов</span><span class="sxs-lookup"><span data-stu-id="2a409-278">Rolling</span></span>

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

### <span data-ttu-id="2a409-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="2a409-279">-VhdContainer</span></span>
<span data-ttu-id="2a409-280">Определяет URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="2a409-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a409-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2a409-282">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="2a409-283">Чтобы получить объект VMSS, используйте Get-AzVmss..</span><span class="sxs-lookup"><span data-stu-id="2a409-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="2a409-284">Этот объект виртуальной машины содержит обновленное состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a409-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="2a409-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a409-285">-VMScaleSetName</span></span>
<span data-ttu-id="2a409-286">Указывает имя службы VMSS, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a409-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a409-287">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a409-287">-Confirm</span></span>
<span data-ttu-id="2a409-288">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a409-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a409-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a409-289">-WhatIf</span></span>
<span data-ttu-id="2a409-290">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a409-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a409-291">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a409-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a409-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a409-292">CommonParameters</span></span>
<span data-ttu-id="2a409-293">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a409-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a409-294">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a409-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a409-295">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a409-295">INPUTS</span></span>

### <span data-ttu-id="2a409-296">System.String</span><span class="sxs-lookup"><span data-stu-id="2a409-296">System.String</span></span>

### <span data-ttu-id="2a409-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a409-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2a409-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a409-298">System.Boolean</span></span>

## <span data-ttu-id="2a409-299">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a409-299">OUTPUTS</span></span>

### <span data-ttu-id="2a409-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a409-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2a409-301">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a409-301">NOTES</span></span>

## <span data-ttu-id="2a409-302">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a409-302">RELATED LINKS</span></span>

[<span data-ttu-id="2a409-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="2a409-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="2a409-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="2a409-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="2a409-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="2a409-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="2a409-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2a409-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


