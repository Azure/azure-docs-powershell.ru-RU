---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074587"
---
# <span data-ttu-id="68f71-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-101">Update-AzVmss</span></span>

## <span data-ttu-id="68f71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68f71-102">SYNOPSIS</span></span>
<span data-ttu-id="68f71-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="68f71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68f71-104">SYNTAX</span></span>

### <span data-ttu-id="68f71-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68f71-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68f71-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f71-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68f71-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68f71-107">DESCRIPTION</span></span>
<span data-ttu-id="68f71-108">Командлет **Update-AzVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="68f71-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68f71-109">EXAMPLES</span></span>

### <span data-ttu-id="68f71-110">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="68f71-111">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="68f71-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68f71-112">PARAMETERS</span></span>

### <span data-ttu-id="68f71-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68f71-113">-AsJob</span></span>
<span data-ttu-id="68f71-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="68f71-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="68f71-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="68f71-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="68f71-116">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="68f71-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="68f71-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="68f71-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="68f71-118">Количество времени, в течение которого автоматическое восстановление приостанавливается из-за изменения состояния в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="68f71-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="68f71-119">Льготный период начинается после изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="68f71-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="68f71-120">Это поможет избежать преждевременного и случайного восстановления.</span><span class="sxs-lookup"><span data-stu-id="68f71-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="68f71-121">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="68f71-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="68f71-122">Значение по умолчанию — 5 минут (PT5M).</span><span class="sxs-lookup"><span data-stu-id="68f71-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="68f71-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="68f71-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="68f71-124">Процент (емкость масштабируемости) виртуальных машин, которые будут одновременны восстановлены.</span><span class="sxs-lookup"><span data-stu-id="68f71-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="68f71-125">По умолчанию используется значение 20%.</span><span class="sxs-lookup"><span data-stu-id="68f71-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="68f71-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="68f71-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="68f71-127">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f71-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="68f71-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="68f71-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="68f71-129">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="68f71-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="68f71-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="68f71-130">-CustomData</span></span>
<span data-ttu-id="68f71-131">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="68f71-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="68f71-132">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="68f71-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="68f71-133">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="68f71-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="68f71-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f71-134">-DefaultProfile</span></span>
<span data-ttu-id="68f71-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68f71-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68f71-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="68f71-136">-DisableAutoRollback</span></span>
<span data-ttu-id="68f71-137">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="68f71-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="68f71-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="68f71-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="68f71-139">Указывает, что этот командлет отключает проверку пароля для ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="68f71-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="68f71-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="68f71-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="68f71-141">Включение и отключение автоматического восстановления на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f71-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="68f71-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="68f71-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="68f71-143">Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="68f71-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="68f71-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="68f71-144">-IdentityId</span></span>
<span data-ttu-id="68f71-145">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f71-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="68f71-146">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="68f71-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="68f71-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="68f71-147">-IdentityType</span></span>
<span data-ttu-id="68f71-148">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68f71-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="68f71-149">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="68f71-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="68f71-150">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68f71-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="68f71-151">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68f71-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68f71-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="68f71-152">SystemAssigned</span></span>
- <span data-ttu-id="68f71-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="68f71-153">UserAssigned</span></span>
- <span data-ttu-id="68f71-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="68f71-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="68f71-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="68f71-155">None</span></span>

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

### <span data-ttu-id="68f71-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="68f71-156">-ImageReferenceId</span></span>
<span data-ttu-id="68f71-157">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="68f71-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="68f71-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="68f71-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="68f71-159">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="68f71-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="68f71-160">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="68f71-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="68f71-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="68f71-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="68f71-162">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="68f71-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="68f71-163">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="68f71-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="68f71-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="68f71-164">-ImageReferenceSku</span></span>
<span data-ttu-id="68f71-165">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="68f71-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="68f71-166">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="68f71-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="68f71-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="68f71-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="68f71-168">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="68f71-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="68f71-169">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="68f71-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="68f71-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="68f71-170">-ImageUri</span></span>
<span data-ttu-id="68f71-171">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="68f71-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="68f71-172">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="68f71-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="68f71-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="68f71-173">-LicenseType</span></span>
<span data-ttu-id="68f71-174">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="68f71-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="68f71-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="68f71-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="68f71-176">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="68f71-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="68f71-177">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68f71-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68f71-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="68f71-178">StandardLRS</span></span>
- <span data-ttu-id="68f71-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="68f71-179">PremiumLRS</span></span>

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

### <span data-ttu-id="68f71-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="68f71-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="68f71-181">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="68f71-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="68f71-182">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="68f71-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="68f71-183">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="68f71-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="68f71-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="68f71-184">-MaxPrice</span></span>
<span data-ttu-id="68f71-185">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="68f71-186">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="68f71-186">This price is in US Dollars.</span></span> <span data-ttu-id="68f71-187">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="68f71-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="68f71-188">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="68f71-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="68f71-189">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="68f71-190">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="68f71-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="68f71-191">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="68f71-191">Example: 0.01538.</span></span>  <span data-ttu-id="68f71-192">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="68f71-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="68f71-193">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="68f71-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="68f71-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="68f71-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="68f71-195">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="68f71-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="68f71-196">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="68f71-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="68f71-197">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="68f71-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="68f71-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="68f71-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="68f71-199">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="68f71-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="68f71-200">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="68f71-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="68f71-201">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="68f71-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="68f71-202">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="68f71-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="68f71-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="68f71-203">-OsDiskCaching</span></span>
<span data-ttu-id="68f71-204">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="68f71-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="68f71-205">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68f71-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68f71-206">Ничего</span><span class="sxs-lookup"><span data-stu-id="68f71-206">None</span></span>
- <span data-ttu-id="68f71-207">Чтения</span><span class="sxs-lookup"><span data-stu-id="68f71-207">ReadOnly</span></span>
- <span data-ttu-id="68f71-208">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="68f71-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="68f71-209">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="68f71-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="68f71-210">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="68f71-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="68f71-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="68f71-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="68f71-212">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="68f71-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="68f71-213">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="68f71-213">-Overprovision</span></span>
<span data-ttu-id="68f71-214">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="68f71-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="68f71-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="68f71-216">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="68f71-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="68f71-217">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="68f71-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="68f71-218">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="68f71-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="68f71-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="68f71-219">-PlanName</span></span>
<span data-ttu-id="68f71-220">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="68f71-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="68f71-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="68f71-221">-PlanProduct</span></span>
<span data-ttu-id="68f71-222">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="68f71-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="68f71-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="68f71-223">-PlanPromotionCode</span></span>
<span data-ttu-id="68f71-224">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="68f71-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="68f71-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="68f71-225">-PlanPublisher</span></span>
<span data-ttu-id="68f71-226">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="68f71-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="68f71-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="68f71-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="68f71-228">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="68f71-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="68f71-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="68f71-230">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="68f71-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="68f71-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f71-231">-ResourceGroupName</span></span>
<span data-ttu-id="68f71-232">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="68f71-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="68f71-233">-ScaleInPolicy</span></span>
<span data-ttu-id="68f71-234">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f71-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="68f71-235">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="68f71-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="68f71-236">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="68f71-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="68f71-237">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="68f71-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="68f71-238">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="68f71-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="68f71-239">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="68f71-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="68f71-240">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="68f71-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="68f71-241">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="68f71-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="68f71-242">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="68f71-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="68f71-243">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="68f71-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="68f71-244">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="68f71-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="68f71-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="68f71-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="68f71-246">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="68f71-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="68f71-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="68f71-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="68f71-248">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="68f71-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="68f71-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="68f71-249">-SkuCapacity</span></span>
<span data-ttu-id="68f71-250">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="68f71-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="68f71-251">-SkuName</span></span>
<span data-ttu-id="68f71-252">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="68f71-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="68f71-253">-SkuTier</span></span>
<span data-ttu-id="68f71-254">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="68f71-255">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68f71-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68f71-256">Стандартная</span><span class="sxs-lookup"><span data-stu-id="68f71-256">Standard</span></span>
- <span data-ttu-id="68f71-257">Базового</span><span class="sxs-lookup"><span data-stu-id="68f71-257">Basic</span></span>

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

### <span data-ttu-id="68f71-258">-Тег</span><span class="sxs-lookup"><span data-stu-id="68f71-258">-Tag</span></span>
<span data-ttu-id="68f71-259">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="68f71-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="68f71-260">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="68f71-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="68f71-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="68f71-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="68f71-262">Настраиваемое время (в минутах) Удаление виртуальной машины может привести к утверждению запланированного события, прежде чем событие будет автоматически одобрено (время ожидания истекло).</span><span class="sxs-lookup"><span data-stu-id="68f71-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="68f71-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="68f71-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="68f71-264">Указывает, включено ли запланированное событие завершения или отключено.</span><span class="sxs-lookup"><span data-stu-id="68f71-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="68f71-265">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="68f71-265">-TimeZone</span></span>
<span data-ttu-id="68f71-266">Задает часовой пояс для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="68f71-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="68f71-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="68f71-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="68f71-268">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f71-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="68f71-269">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="68f71-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="68f71-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="68f71-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="68f71-271">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="68f71-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="68f71-272">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68f71-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68f71-273">Автоматически</span><span class="sxs-lookup"><span data-stu-id="68f71-273">Automatic</span></span>
- <span data-ttu-id="68f71-274">Вручную</span><span class="sxs-lookup"><span data-stu-id="68f71-274">Manual</span></span>
- <span data-ttu-id="68f71-275">За</span><span class="sxs-lookup"><span data-stu-id="68f71-275">Rolling</span></span>

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

### <span data-ttu-id="68f71-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="68f71-276">-VhdContainer</span></span>
<span data-ttu-id="68f71-277">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="68f71-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68f71-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="68f71-279">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="68f71-280">Чтобы получить объект VMSS, используйте командлет Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="68f71-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="68f71-281">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="68f71-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="68f71-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="68f71-282">-VMScaleSetName</span></span>
<span data-ttu-id="68f71-283">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="68f71-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="68f71-284">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68f71-284">-Confirm</span></span>
<span data-ttu-id="68f71-285">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68f71-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f71-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f71-286">-WhatIf</span></span>
<span data-ttu-id="68f71-287">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68f71-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f71-288">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68f71-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f71-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f71-289">CommonParameters</span></span>
<span data-ttu-id="68f71-290">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68f71-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f71-291">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68f71-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f71-292">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68f71-292">INPUTS</span></span>

### <span data-ttu-id="68f71-293">System. String</span><span class="sxs-lookup"><span data-stu-id="68f71-293">System.String</span></span>

### <span data-ttu-id="68f71-294">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68f71-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="68f71-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68f71-295">System.Boolean</span></span>

## <span data-ttu-id="68f71-296">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68f71-296">OUTPUTS</span></span>

### <span data-ttu-id="68f71-297">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68f71-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="68f71-298">Пуск</span><span class="sxs-lookup"><span data-stu-id="68f71-298">NOTES</span></span>

## <span data-ttu-id="68f71-299">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68f71-299">RELATED LINKS</span></span>

[<span data-ttu-id="68f71-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="68f71-301">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="68f71-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="68f71-303">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="68f71-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="68f71-305">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="68f71-306">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68f71-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


