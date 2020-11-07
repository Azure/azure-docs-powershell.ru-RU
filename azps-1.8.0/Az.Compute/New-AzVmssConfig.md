---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731299"
---
# <span data-ttu-id="f6630-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f6630-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="f6630-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6630-102">SYNOPSIS</span></span>
<span data-ttu-id="f6630-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="f6630-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6630-104">SYNTAX</span></span>

### <span data-ttu-id="f6630-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6630-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6630-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6630-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6630-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6630-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6630-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6630-108">DESCRIPTION</span></span>
<span data-ttu-id="f6630-109">Командлет **New-AzVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f6630-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="f6630-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="f6630-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="f6630-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="f6630-111">These cmdlets are:</span></span>
- <span data-ttu-id="f6630-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="f6630-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="f6630-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6630-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="f6630-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f6630-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="f6630-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6630-116">EXAMPLES</span></span>

### <span data-ttu-id="f6630-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="f6630-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="f6630-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="f6630-119">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="f6630-120">Вторая команда использует командлет **New-AzVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="f6630-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="f6630-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6630-121">PARAMETERS</span></span>

### <span data-ttu-id="f6630-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f6630-122">-AssignIdentity</span></span>
<span data-ttu-id="f6630-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f6630-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f6630-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="f6630-125">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="f6630-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="f6630-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f6630-126">-BootDiagnostic</span></span>
<span data-ttu-id="f6630-127">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="f6630-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-128">-DefaultProfile</span></span>
<span data-ttu-id="f6630-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6630-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6630-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="f6630-130">-DisableAutoRollback</span></span>
<span data-ttu-id="f6630-131">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="f6630-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="f6630-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="f6630-132">-EnableUltraSSD</span></span>
<span data-ttu-id="f6630-133">Обеспечивает возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="f6630-134">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="f6630-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="f6630-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="f6630-135">-EvictionPolicy</span></span>
<span data-ttu-id="f6630-136">Задает политику вытеснения для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="f6630-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="f6630-137">-Расширение</span><span class="sxs-lookup"><span data-stu-id="f6630-137">-Extension</span></span>
<span data-ttu-id="f6630-138">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="f6630-139">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="f6630-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6630-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="f6630-140">-HealthProbeId</span></span>
<span data-ttu-id="f6630-141">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="f6630-142">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="f6630-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="f6630-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="f6630-143">-IdentityId</span></span>
<span data-ttu-id="f6630-144">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="f6630-145">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="f6630-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="f6630-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f6630-146">-IdentityType</span></span>
<span data-ttu-id="f6630-147">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6630-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="f6630-148">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="f6630-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="f6630-149">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6630-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="f6630-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6630-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6630-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f6630-151">SystemAssigned</span></span>
- <span data-ttu-id="f6630-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="f6630-152">UserAssigned</span></span>
- <span data-ttu-id="f6630-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="f6630-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="f6630-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="f6630-154">None</span></span>

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

### <span data-ttu-id="f6630-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f6630-155">-LicenseType</span></span>
<span data-ttu-id="f6630-156">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="f6630-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="f6630-157">-Location</span><span class="sxs-lookup"><span data-stu-id="f6630-157">-Location</span></span>
<span data-ttu-id="f6630-158">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="f6630-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6630-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="f6630-160">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="f6630-161">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f6630-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="f6630-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-162">-OsProfile</span></span>
<span data-ttu-id="f6630-163">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="f6630-164">Для задания этого объекта можно использовать командлет **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="f6630-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="f6630-165">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="f6630-165">-Overprovision</span></span>
<span data-ttu-id="f6630-166">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="f6630-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f6630-167">-PlanName</span></span>
<span data-ttu-id="f6630-168">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="f6630-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="f6630-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="f6630-169">-PlanProduct</span></span>
<span data-ttu-id="f6630-170">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="f6630-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="f6630-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="f6630-171">-PlanPromotionCode</span></span>
<span data-ttu-id="f6630-172">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="f6630-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="f6630-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f6630-173">-PlanPublisher</span></span>
<span data-ttu-id="f6630-174">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="f6630-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="f6630-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f6630-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f6630-176">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="f6630-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="f6630-177">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="f6630-177">-Priority</span></span>
<span data-ttu-id="f6630-178">Задает приоритет виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="f6630-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="f6630-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f6630-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="f6630-180">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="f6630-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="f6630-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f6630-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="f6630-182">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="f6630-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="f6630-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f6630-183">-SkuCapacity</span></span>
<span data-ttu-id="f6630-184">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="f6630-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f6630-185">-SkuName</span></span>
<span data-ttu-id="f6630-186">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="f6630-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f6630-187">-SkuTier</span></span>
<span data-ttu-id="f6630-188">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="f6630-189">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6630-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6630-190">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f6630-190">Standard</span></span>
- <span data-ttu-id="f6630-191">Базового</span><span class="sxs-lookup"><span data-stu-id="f6630-191">Basic</span></span>

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

### <span data-ttu-id="f6630-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-192">-StorageProfile</span></span>
<span data-ttu-id="f6630-193">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="f6630-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="f6630-194">Для задания этого объекта можно использовать командлет **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="f6630-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="f6630-195">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6630-195">-Tag</span></span>
<span data-ttu-id="f6630-196">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f6630-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f6630-197">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f6630-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f6630-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="f6630-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="f6630-199">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="f6630-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="f6630-200">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6630-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6630-201">Автоматически</span><span class="sxs-lookup"><span data-stu-id="f6630-201">Automatic</span></span>
- <span data-ttu-id="f6630-202">Вручную</span><span class="sxs-lookup"><span data-stu-id="f6630-202">Manual</span></span>

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

### <span data-ttu-id="f6630-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="f6630-203">-Zone</span></span>
<span data-ttu-id="f6630-204">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f6630-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f6630-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="f6630-205">-ZoneBalance</span></span>
<span data-ttu-id="f6630-206">Следует ли принудительно использовать межплатформенные зоны распространения на всех компьютерах в случае сбоя зоны.</span><span class="sxs-lookup"><span data-stu-id="f6630-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="f6630-207">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6630-207">-Confirm</span></span>
<span data-ttu-id="f6630-208">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6630-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6630-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6630-209">-WhatIf</span></span>
<span data-ttu-id="f6630-210">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6630-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6630-211">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6630-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6630-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6630-212">CommonParameters</span></span>
<span data-ttu-id="f6630-213">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6630-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6630-214">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6630-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6630-215">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6630-215">INPUTS</span></span>

### <span data-ttu-id="f6630-216">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6630-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f6630-217">System. String</span><span class="sxs-lookup"><span data-stu-id="f6630-217">System.String</span></span>

### <span data-ttu-id="f6630-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6630-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f6630-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6630-219">System.Int32</span></span>

### <span data-ttu-id="f6630-220">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6630-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f6630-221">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="f6630-222">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="f6630-223">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f6630-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="f6630-224">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="f6630-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="f6630-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="f6630-225">System.String[]</span></span>

### <span data-ttu-id="f6630-226">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f6630-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="f6630-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6630-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6630-228">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f6630-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="f6630-229">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6630-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f6630-230">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6630-230">OUTPUTS</span></span>

### <span data-ttu-id="f6630-231">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f6630-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f6630-232">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6630-232">NOTES</span></span>

## <span data-ttu-id="f6630-233">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6630-233">RELATED LINKS</span></span>

[<span data-ttu-id="f6630-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="f6630-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f6630-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="f6630-236">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6630-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="f6630-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f6630-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="f6630-238">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6630-238">New-AzVmss</span></span>](./New-AzVmss.md)
