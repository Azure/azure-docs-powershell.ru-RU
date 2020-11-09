---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311903"
---
# <span data-ttu-id="133a1-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-101">Update-AzVmss</span></span>

## <span data-ttu-id="133a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="133a1-102">SYNOPSIS</span></span>
<span data-ttu-id="133a1-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="133a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="133a1-104">SYNTAX</span></span>

### <span data-ttu-id="133a1-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="133a1-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="133a1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="133a1-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="133a1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="133a1-107">DESCRIPTION</span></span>
<span data-ttu-id="133a1-108">Командлет **Update-AzVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="133a1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="133a1-109">EXAMPLES</span></span>

### <span data-ttu-id="133a1-110">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="133a1-111">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="133a1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="133a1-112">PARAMETERS</span></span>

### <span data-ttu-id="133a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="133a1-113">-AsJob</span></span>
<span data-ttu-id="133a1-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="133a1-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="133a1-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="133a1-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="133a1-116">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="133a1-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="133a1-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="133a1-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="133a1-118">Количество времени, в течение которого автоматическое восстановление приостанавливается из-за изменения состояния в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="133a1-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="133a1-119">Льготный период начинается после изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="133a1-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="133a1-120">Это поможет избежать преждевременного и случайного восстановления.</span><span class="sxs-lookup"><span data-stu-id="133a1-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="133a1-121">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="133a1-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="133a1-122">Минимально допустимый льготный период составляет 30 минут (PT30M), который также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="133a1-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="133a1-123">Максимально допустимый льготный период составляет 90 минут (PT90M).</span><span class="sxs-lookup"><span data-stu-id="133a1-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="133a1-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="133a1-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="133a1-125">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="133a1-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="133a1-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="133a1-127">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="133a1-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="133a1-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="133a1-128">-CustomData</span></span>
<span data-ttu-id="133a1-129">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="133a1-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="133a1-130">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="133a1-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="133a1-131">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="133a1-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="133a1-132">Для использования Cloud-init для виртуальной машины, ознакомьтесь со сведениями о [настройке виртуальной машины Linux во время создания с помощью облака-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="133a1-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="133a1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133a1-133">-DefaultProfile</span></span>
<span data-ttu-id="133a1-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="133a1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133a1-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="133a1-135">-DisableAutoRollback</span></span>
<span data-ttu-id="133a1-136">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="133a1-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="133a1-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="133a1-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="133a1-138">Указывает, что этот командлет отключает проверку пароля для ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="133a1-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="133a1-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="133a1-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="133a1-140">Включение и отключение автоматического восстановления на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="133a1-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="133a1-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="133a1-142">Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="133a1-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="133a1-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="133a1-143">-EncryptionAtHost</span></span>
<span data-ttu-id="133a1-144">Этот параметр может использоваться пользователем в запросе на включение или отключение шифрования узла для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="133a1-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="133a1-145">-IdentityId</span></span>
<span data-ttu-id="133a1-146">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="133a1-147">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="133a1-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="133a1-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="133a1-148">-IdentityType</span></span>
<span data-ttu-id="133a1-149">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="133a1-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="133a1-150">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="133a1-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="133a1-151">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="133a1-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="133a1-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="133a1-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="133a1-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="133a1-153">SystemAssigned</span></span>
- <span data-ttu-id="133a1-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="133a1-154">UserAssigned</span></span>
- <span data-ttu-id="133a1-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="133a1-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="133a1-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="133a1-156">None</span></span>

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

### <span data-ttu-id="133a1-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="133a1-157">-ImageReferenceId</span></span>
<span data-ttu-id="133a1-158">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="133a1-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="133a1-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="133a1-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="133a1-160">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="133a1-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="133a1-161">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="133a1-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="133a1-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="133a1-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="133a1-163">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="133a1-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="133a1-164">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="133a1-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="133a1-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="133a1-165">-ImageReferenceSku</span></span>
<span data-ttu-id="133a1-166">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="133a1-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="133a1-167">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="133a1-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="133a1-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="133a1-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="133a1-169">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="133a1-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="133a1-170">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="133a1-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="133a1-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="133a1-171">-ImageUri</span></span>
<span data-ttu-id="133a1-172">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="133a1-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="133a1-173">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="133a1-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="133a1-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="133a1-174">-LicenseType</span></span>
<span data-ttu-id="133a1-175">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="133a1-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="133a1-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="133a1-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="133a1-177">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="133a1-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="133a1-178">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="133a1-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="133a1-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="133a1-179">StandardLRS</span></span>
- <span data-ttu-id="133a1-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="133a1-180">PremiumLRS</span></span>

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

### <span data-ttu-id="133a1-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="133a1-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="133a1-182">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="133a1-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="133a1-183">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="133a1-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="133a1-184">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="133a1-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="133a1-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="133a1-185">-MaxPrice</span></span>
<span data-ttu-id="133a1-186">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="133a1-187">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="133a1-187">This price is in US Dollars.</span></span> <span data-ttu-id="133a1-188">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="133a1-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="133a1-189">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="133a1-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="133a1-190">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="133a1-191">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="133a1-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="133a1-192">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="133a1-192">Example: 0.01538.</span></span>  <span data-ttu-id="133a1-193">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="133a1-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="133a1-194">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="133a1-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="133a1-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="133a1-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="133a1-196">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="133a1-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="133a1-197">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="133a1-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="133a1-198">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="133a1-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="133a1-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="133a1-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="133a1-200">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="133a1-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="133a1-201">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="133a1-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="133a1-202">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="133a1-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="133a1-203">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="133a1-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="133a1-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="133a1-204">-OsDiskCaching</span></span>
<span data-ttu-id="133a1-205">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="133a1-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="133a1-206">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="133a1-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="133a1-207">Ничего</span><span class="sxs-lookup"><span data-stu-id="133a1-207">None</span></span>
- <span data-ttu-id="133a1-208">Чтения</span><span class="sxs-lookup"><span data-stu-id="133a1-208">ReadOnly</span></span>
- <span data-ttu-id="133a1-209">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="133a1-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="133a1-210">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="133a1-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="133a1-211">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="133a1-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="133a1-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="133a1-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="133a1-213">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="133a1-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="133a1-214">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="133a1-214">-Overprovision</span></span>
<span data-ttu-id="133a1-215">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="133a1-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="133a1-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="133a1-217">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="133a1-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="133a1-218">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="133a1-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="133a1-219">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="133a1-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="133a1-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="133a1-220">-PlanName</span></span>
<span data-ttu-id="133a1-221">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="133a1-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="133a1-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="133a1-222">-PlanProduct</span></span>
<span data-ttu-id="133a1-223">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="133a1-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="133a1-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="133a1-224">-PlanPromotionCode</span></span>
<span data-ttu-id="133a1-225">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="133a1-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="133a1-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="133a1-226">-PlanPublisher</span></span>
<span data-ttu-id="133a1-227">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="133a1-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="133a1-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="133a1-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="133a1-229">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="133a1-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="133a1-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="133a1-231">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="133a1-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="133a1-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="133a1-232">-ResourceGroupName</span></span>
<span data-ttu-id="133a1-233">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="133a1-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="133a1-234">-ScaleInPolicy</span></span>
<span data-ttu-id="133a1-235">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="133a1-236">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="133a1-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="133a1-237">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="133a1-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="133a1-238">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="133a1-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="133a1-239">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="133a1-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="133a1-240">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="133a1-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="133a1-241">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="133a1-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="133a1-242">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="133a1-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="133a1-243">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="133a1-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="133a1-244">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="133a1-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="133a1-245">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="133a1-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="133a1-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="133a1-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="133a1-247">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="133a1-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="133a1-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="133a1-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="133a1-249">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="133a1-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="133a1-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="133a1-250">-SkuCapacity</span></span>
<span data-ttu-id="133a1-251">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="133a1-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="133a1-252">-SkuName</span></span>
<span data-ttu-id="133a1-253">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="133a1-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="133a1-254">-SkuTier</span></span>
<span data-ttu-id="133a1-255">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="133a1-256">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="133a1-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="133a1-257">Стандартная</span><span class="sxs-lookup"><span data-stu-id="133a1-257">Standard</span></span>
- <span data-ttu-id="133a1-258">Базового</span><span class="sxs-lookup"><span data-stu-id="133a1-258">Basic</span></span>

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

### <span data-ttu-id="133a1-259">-Тег</span><span class="sxs-lookup"><span data-stu-id="133a1-259">-Tag</span></span>
<span data-ttu-id="133a1-260">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="133a1-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="133a1-261">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="133a1-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="133a1-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="133a1-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="133a1-263">Настраиваемое время (в минутах) Удаление виртуальной машины может привести к утверждению запланированного события, прежде чем событие будет автоматически одобрено (время ожидания истекло).</span><span class="sxs-lookup"><span data-stu-id="133a1-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="133a1-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="133a1-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="133a1-265">Указывает, включено ли запланированное событие завершения или отключено.</span><span class="sxs-lookup"><span data-stu-id="133a1-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="133a1-266">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="133a1-266">-TimeZone</span></span>
<span data-ttu-id="133a1-267">Задает часовой пояс для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="133a1-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="133a1-268">Например, \" тихоокеанское время \" .</span><span class="sxs-lookup"><span data-stu-id="133a1-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="133a1-269">Возможные значения могут быть [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) значениями из часовых поясов, возвращаемых [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="133a1-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="133a1-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="133a1-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="133a1-271">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="133a1-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="133a1-272">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="133a1-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="133a1-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="133a1-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="133a1-274">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="133a1-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="133a1-275">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="133a1-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="133a1-276">Автоматически</span><span class="sxs-lookup"><span data-stu-id="133a1-276">Automatic</span></span>
- <span data-ttu-id="133a1-277">Вручную</span><span class="sxs-lookup"><span data-stu-id="133a1-277">Manual</span></span>
- <span data-ttu-id="133a1-278">За</span><span class="sxs-lookup"><span data-stu-id="133a1-278">Rolling</span></span>

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

### <span data-ttu-id="133a1-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="133a1-279">-VhdContainer</span></span>
<span data-ttu-id="133a1-280">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="133a1-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="133a1-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="133a1-282">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="133a1-283">Чтобы получить объект VMSS, используйте командлет Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="133a1-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="133a1-284">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="133a1-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="133a1-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="133a1-285">-VMScaleSetName</span></span>
<span data-ttu-id="133a1-286">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="133a1-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="133a1-287">-Confirm</span><span class="sxs-lookup"><span data-stu-id="133a1-287">-Confirm</span></span>
<span data-ttu-id="133a1-288">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="133a1-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133a1-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133a1-289">-WhatIf</span></span>
<span data-ttu-id="133a1-290">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="133a1-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133a1-291">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="133a1-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133a1-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133a1-292">CommonParameters</span></span>
<span data-ttu-id="133a1-293">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="133a1-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133a1-294">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="133a1-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133a1-295">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="133a1-295">INPUTS</span></span>

### <span data-ttu-id="133a1-296">System. String</span><span class="sxs-lookup"><span data-stu-id="133a1-296">System.String</span></span>

### <span data-ttu-id="133a1-297">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="133a1-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="133a1-298">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="133a1-298">System.Boolean</span></span>

## <span data-ttu-id="133a1-299">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="133a1-299">OUTPUTS</span></span>

### <span data-ttu-id="133a1-300">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="133a1-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="133a1-301">Пуск</span><span class="sxs-lookup"><span data-stu-id="133a1-301">NOTES</span></span>

## <span data-ttu-id="133a1-302">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="133a1-302">RELATED LINKS</span></span>

[<span data-ttu-id="133a1-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="133a1-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="133a1-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="133a1-306">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="133a1-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="133a1-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="133a1-309">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="133a1-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


