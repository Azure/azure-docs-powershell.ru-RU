---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064764"
---
# <span data-ttu-id="62fb0-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="62fb0-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="62fb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="62fb0-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="62fb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62fb0-104">SYNTAX</span></span>

### <span data-ttu-id="62fb0-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62fb0-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62fb0-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="62fb0-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62fb0-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="62fb0-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62fb0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62fb0-108">DESCRIPTION</span></span>
<span data-ttu-id="62fb0-109">Командлет **New-AzVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="62fb0-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="62fb0-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="62fb0-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="62fb0-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="62fb0-111">These cmdlets are:</span></span>
- <span data-ttu-id="62fb0-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="62fb0-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="62fb0-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="62fb0-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="62fb0-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="62fb0-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="62fb0-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62fb0-116">EXAMPLES</span></span>

### <span data-ttu-id="62fb0-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="62fb0-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="62fb0-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="62fb0-119">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="62fb0-120">Вторая команда использует командлет **New-AzVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="62fb0-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="62fb0-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62fb0-121">PARAMETERS</span></span>

### <span data-ttu-id="62fb0-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="62fb0-122">-AssignIdentity</span></span>
<span data-ttu-id="62fb0-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="62fb0-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="62fb0-125">Количество времени, в течение которого автоматическое восстановление приостанавливается из-за изменения состояния в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="62fb0-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="62fb0-126">Льготный период начинается после изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="62fb0-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="62fb0-127">Это поможет избежать преждевременного и случайного восстановления.</span><span class="sxs-lookup"><span data-stu-id="62fb0-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="62fb0-128">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="62fb0-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="62fb0-129">Значение по умолчанию — 5 минут (PT5M).</span><span class="sxs-lookup"><span data-stu-id="62fb0-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="62fb0-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="62fb0-131">Процент (емкость масштабируемости) виртуальных машин, которые будут одновременны восстановлены.</span><span class="sxs-lookup"><span data-stu-id="62fb0-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="62fb0-132">По умолчанию используется значение 20%.</span><span class="sxs-lookup"><span data-stu-id="62fb0-132">The default value is 20%.</span></span>

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

### <span data-ttu-id="62fb0-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="62fb0-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="62fb0-134">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="62fb0-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="62fb0-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="62fb0-135">-BootDiagnostic</span></span>
<span data-ttu-id="62fb0-136">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-137">-DefaultProfile</span></span>
<span data-ttu-id="62fb0-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62fb0-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62fb0-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="62fb0-139">-DisableAutoRollback</span></span>
<span data-ttu-id="62fb0-140">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="62fb0-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="62fb0-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="62fb0-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="62fb0-142">Включает автоматическое восстановление на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="62fb0-143">-EnableUltraSSD</span></span>
<span data-ttu-id="62fb0-144">Обеспечивает возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="62fb0-145">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="62fb0-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="62fb0-146">-EvictionPolicy</span></span>
<span data-ttu-id="62fb0-147">Задает политику вытеснения для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="62fb0-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-148">-Расширение</span><span class="sxs-lookup"><span data-stu-id="62fb0-148">-Extension</span></span>
<span data-ttu-id="62fb0-149">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="62fb0-150">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="62fb0-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="62fb0-151">-HealthProbeId</span></span>
<span data-ttu-id="62fb0-152">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="62fb0-153">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="62fb0-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="62fb0-154">-IdentityId</span></span>
<span data-ttu-id="62fb0-155">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="62fb0-156">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="62fb0-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="62fb0-157">-IdentityType</span></span>
<span data-ttu-id="62fb0-158">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62fb0-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="62fb0-159">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="62fb0-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="62fb0-160">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62fb0-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="62fb0-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62fb0-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62fb0-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="62fb0-162">SystemAssigned</span></span>
- <span data-ttu-id="62fb0-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="62fb0-163">UserAssigned</span></span>
- <span data-ttu-id="62fb0-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="62fb0-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="62fb0-165">Ничего</span><span class="sxs-lookup"><span data-stu-id="62fb0-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62fb0-166">-LicenseType</span></span>
<span data-ttu-id="62fb0-167">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="62fb0-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-168">-Location</span><span class="sxs-lookup"><span data-stu-id="62fb0-168">-Location</span></span>
<span data-ttu-id="62fb0-169">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="62fb0-170">-MaxPrice</span></span>
<span data-ttu-id="62fb0-171">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="62fb0-172">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="62fb0-172">This price is in US Dollars.</span></span> <span data-ttu-id="62fb0-173">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="62fb0-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="62fb0-174">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="62fb0-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="62fb0-175">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="62fb0-176">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="62fb0-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="62fb0-177">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="62fb0-177">Example: 0.01538.</span></span>  <span data-ttu-id="62fb0-178">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="62fb0-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="62fb0-179">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="62fb0-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="62fb0-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="62fb0-181">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="62fb0-182">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="62fb0-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-183">-OsProfile</span></span>
<span data-ttu-id="62fb0-184">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="62fb0-185">Для задания этого объекта можно использовать командлет **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="62fb0-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-186">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="62fb0-186">-Overprovision</span></span>
<span data-ttu-id="62fb0-187">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="62fb0-188">-PlanName</span></span>
<span data-ttu-id="62fb0-189">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="62fb0-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="62fb0-190">-PlanProduct</span></span>
<span data-ttu-id="62fb0-191">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="62fb0-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="62fb0-192">-PlanPromotionCode</span></span>
<span data-ttu-id="62fb0-193">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="62fb0-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="62fb0-194">-PlanPublisher</span></span>
<span data-ttu-id="62fb0-195">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="62fb0-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="62fb0-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="62fb0-197">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="62fb0-197">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="62fb0-198">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="62fb0-198">-Priority</span></span>
<span data-ttu-id="62fb0-199">Приоритет виртуального machien в множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="62fb0-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="62fb0-200">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="62fb0-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="62fb0-201">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62fb0-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="62fb0-202">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="62fb0-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="62fb0-203">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="62fb0-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="62fb0-204">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="62fb0-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="62fb0-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="62fb0-206">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="62fb0-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="62fb0-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="62fb0-208">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="62fb0-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="62fb0-209">-ScaleInPolicy</span></span>
<span data-ttu-id="62fb0-210">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="62fb0-211">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="62fb0-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="62fb0-212">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="62fb0-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="62fb0-213">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="62fb0-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="62fb0-214">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="62fb0-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="62fb0-215">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="62fb0-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="62fb0-216">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="62fb0-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="62fb0-217">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="62fb0-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="62fb0-218">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="62fb0-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="62fb0-219">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="62fb0-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="62fb0-220">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="62fb0-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="62fb0-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="62fb0-222">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="62fb0-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="62fb0-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="62fb0-224">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="62fb0-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="62fb0-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="62fb0-225">-SkuCapacity</span></span>
<span data-ttu-id="62fb0-226">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="62fb0-227">-SkuName</span></span>
<span data-ttu-id="62fb0-228">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="62fb0-229">-SkuTier</span></span>
<span data-ttu-id="62fb0-230">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="62fb0-231">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62fb0-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62fb0-232">Стандартная</span><span class="sxs-lookup"><span data-stu-id="62fb0-232">Standard</span></span>
- <span data-ttu-id="62fb0-233">Базового</span><span class="sxs-lookup"><span data-stu-id="62fb0-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-234">-StorageProfile</span></span>
<span data-ttu-id="62fb0-235">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="62fb0-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="62fb0-236">Для задания этого объекта можно использовать командлет **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="62fb0-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-237">-Тег</span><span class="sxs-lookup"><span data-stu-id="62fb0-237">-Tag</span></span>
<span data-ttu-id="62fb0-238">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="62fb0-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="62fb0-239">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="62fb0-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="62fb0-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="62fb0-241">Настраиваемое время (в минутах) Удаление виртуальной машины может привести к утверждению запланированного события, прежде чем событие будет автоматически одобрено (время ожидания истекло).</span><span class="sxs-lookup"><span data-stu-id="62fb0-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="62fb0-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="62fb0-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="62fb0-243">Включение событий, запланированных на завершение</span><span class="sxs-lookup"><span data-stu-id="62fb0-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="62fb0-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="62fb0-245">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="62fb0-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="62fb0-246">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62fb0-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62fb0-247">Автоматически</span><span class="sxs-lookup"><span data-stu-id="62fb0-247">Automatic</span></span>
- <span data-ttu-id="62fb0-248">Вручную</span><span class="sxs-lookup"><span data-stu-id="62fb0-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-249">-Zone</span><span class="sxs-lookup"><span data-stu-id="62fb0-249">-Zone</span></span>
<span data-ttu-id="62fb0-250">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="62fb0-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fb0-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="62fb0-251">-ZoneBalance</span></span>
<span data-ttu-id="62fb0-252">Следует ли принудительно использовать межплатформенные зоны распространения на всех компьютерах в случае сбоя зоны.</span><span class="sxs-lookup"><span data-stu-id="62fb0-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="62fb0-253">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62fb0-253">-Confirm</span></span>
<span data-ttu-id="62fb0-254">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62fb0-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62fb0-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62fb0-255">-WhatIf</span></span>
<span data-ttu-id="62fb0-256">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62fb0-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62fb0-257">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62fb0-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62fb0-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fb0-258">CommonParameters</span></span>
<span data-ttu-id="62fb0-259">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62fb0-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fb0-260">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62fb0-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fb0-261">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62fb0-261">INPUTS</span></span>

### <span data-ttu-id="62fb0-262">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62fb0-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62fb0-263">System. String</span><span class="sxs-lookup"><span data-stu-id="62fb0-263">System.String</span></span>

### <span data-ttu-id="62fb0-264">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62fb0-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62fb0-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62fb0-265">System.Int32</span></span>

### <span data-ttu-id="62fb0-266">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62fb0-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="62fb0-267">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="62fb0-268">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="62fb0-269">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="62fb0-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="62fb0-270">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="62fb0-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="62fb0-271">System. String []</span><span class="sxs-lookup"><span data-stu-id="62fb0-271">System.String[]</span></span>

### <span data-ttu-id="62fb0-272">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="62fb0-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="62fb0-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62fb0-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="62fb0-274">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="62fb0-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="62fb0-275">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62fb0-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="62fb0-276">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62fb0-276">OUTPUTS</span></span>

### <span data-ttu-id="62fb0-277">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="62fb0-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="62fb0-278">Пуск</span><span class="sxs-lookup"><span data-stu-id="62fb0-278">NOTES</span></span>

## <span data-ttu-id="62fb0-279">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62fb0-279">RELATED LINKS</span></span>

[<span data-ttu-id="62fb0-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="62fb0-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="62fb0-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="62fb0-282">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="62fb0-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="62fb0-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="62fb0-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="62fb0-284">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62fb0-284">New-AzVmss</span></span>](./New-AzVmss.md)
