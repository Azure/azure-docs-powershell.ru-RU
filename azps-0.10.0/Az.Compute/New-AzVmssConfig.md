---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911452"
---
# <span data-ttu-id="2f71f-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2f71f-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="2f71f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f71f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f71f-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="2f71f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f71f-104">SYNTAX</span></span>

### <span data-ttu-id="2f71f-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f71f-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f71f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f71f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f71f-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f71f-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f71f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f71f-108">DESCRIPTION</span></span>
<span data-ttu-id="2f71f-109">Командлет **New-AzVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2f71f-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="2f71f-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="2f71f-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="2f71f-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="2f71f-111">These cmdlets are:</span></span>

- <span data-ttu-id="2f71f-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="2f71f-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="2f71f-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f71f-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="2f71f-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2f71f-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="2f71f-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f71f-116">EXAMPLES</span></span>

### <span data-ttu-id="2f71f-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="2f71f-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="2f71f-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="2f71f-119">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="2f71f-120">Вторая команда использует командлет **New-AzVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="2f71f-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="2f71f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f71f-121">PARAMETERS</span></span>

### <span data-ttu-id="2f71f-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2f71f-122">-AssignIdentity</span></span>
<span data-ttu-id="2f71f-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2f71f-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2f71f-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="2f71f-125">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="2f71f-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2f71f-126">-BootDiagnostic</span></span>
<span data-ttu-id="2f71f-127">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2f71f-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-128">-DefaultProfile</span></span>
<span data-ttu-id="2f71f-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f71f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f71f-130">-Расширение</span><span class="sxs-lookup"><span data-stu-id="2f71f-130">-Extension</span></span>
<span data-ttu-id="2f71f-131">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="2f71f-132">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="2f71f-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="2f71f-133">-HealthProbeId</span></span>
<span data-ttu-id="2f71f-134">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2f71f-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="2f71f-135">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="2f71f-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2f71f-136">-IdentityId</span></span>
<span data-ttu-id="2f71f-137">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2f71f-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2f71f-138">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="2f71f-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2f71f-139">-IdentityType</span></span>
<span data-ttu-id="2f71f-140">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f71f-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="2f71f-141">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="2f71f-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="2f71f-142">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f71f-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="2f71f-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f71f-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f71f-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2f71f-144">SystemAssigned</span></span>
- <span data-ttu-id="2f71f-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="2f71f-145">UserAssigned</span></span>
- <span data-ttu-id="2f71f-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="2f71f-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="2f71f-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f71f-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2f71f-148">-LicenseType</span></span>
<span data-ttu-id="2f71f-149">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="2f71f-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-150">-Location</span><span class="sxs-lookup"><span data-stu-id="2f71f-150">-Location</span></span>
<span data-ttu-id="2f71f-151">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f71f-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="2f71f-153">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="2f71f-154">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="2f71f-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-155">-OsProfile</span></span>
<span data-ttu-id="2f71f-156">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="2f71f-157">Для задания этого объекта можно использовать командлет **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="2f71f-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-158">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="2f71f-158">-Overprovision</span></span>
<span data-ttu-id="2f71f-159">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2f71f-160">-PlanName</span></span>
<span data-ttu-id="2f71f-161">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="2f71f-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="2f71f-162">-PlanProduct</span></span>
<span data-ttu-id="2f71f-163">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="2f71f-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="2f71f-164">-PlanPromotionCode</span></span>
<span data-ttu-id="2f71f-165">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="2f71f-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2f71f-166">-PlanPublisher</span></span>
<span data-ttu-id="2f71f-167">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="2f71f-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-168">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="2f71f-168">-Priority</span></span>
<span data-ttu-id="2f71f-169">Задает приоритет виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="2f71f-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="2f71f-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="2f71f-171">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="2f71f-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2f71f-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="2f71f-173">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="2f71f-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2f71f-174">-SkuCapacity</span></span>
<span data-ttu-id="2f71f-175">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2f71f-176">-SkuName</span></span>
<span data-ttu-id="2f71f-177">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2f71f-178">-SkuTier</span></span>
<span data-ttu-id="2f71f-179">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="2f71f-180">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f71f-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f71f-181">Стандартная</span><span class="sxs-lookup"><span data-stu-id="2f71f-181">Standard</span></span>
- <span data-ttu-id="2f71f-182">Базового</span><span class="sxs-lookup"><span data-stu-id="2f71f-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-183">-StorageProfile</span></span>
<span data-ttu-id="2f71f-184">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f71f-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="2f71f-185">Для задания этого объекта можно использовать командлет **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="2f71f-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-186">-Тег</span><span class="sxs-lookup"><span data-stu-id="2f71f-186">-Tag</span></span>
<span data-ttu-id="2f71f-187">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2f71f-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f71f-188">Например:</span><span class="sxs-lookup"><span data-stu-id="2f71f-188">For example:</span></span>

<span data-ttu-id="2f71f-189">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2f71f-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="2f71f-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="2f71f-191">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="2f71f-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="2f71f-192">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f71f-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f71f-193">Автоматически</span><span class="sxs-lookup"><span data-stu-id="2f71f-193">Automatic</span></span>
- <span data-ttu-id="2f71f-194">Вручную</span><span class="sxs-lookup"><span data-stu-id="2f71f-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="2f71f-195">-Zone</span></span>
<span data-ttu-id="2f71f-196">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2f71f-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f71f-197">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f71f-197">-Confirm</span></span>
<span data-ttu-id="2f71f-198">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f71f-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f71f-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f71f-199">-WhatIf</span></span>
<span data-ttu-id="2f71f-200">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f71f-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f71f-201">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f71f-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f71f-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f71f-202">CommonParameters</span></span>
<span data-ttu-id="2f71f-203">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f71f-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f71f-204">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f71f-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f71f-205">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f71f-205">INPUTS</span></span>

### <span data-ttu-id="2f71f-206">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f71f-206">None</span></span>
<span data-ttu-id="2f71f-207">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f71f-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f71f-208">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f71f-208">OUTPUTS</span></span>

### <span data-ttu-id="2f71f-209">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2f71f-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2f71f-210">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f71f-210">NOTES</span></span>

## <span data-ttu-id="2f71f-211">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f71f-211">RELATED LINKS</span></span>

[<span data-ttu-id="2f71f-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="2f71f-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2f71f-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="2f71f-214">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f71f-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="2f71f-215">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2f71f-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="2f71f-216">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2f71f-216">New-AzVmss</span></span>](./New-AzVmss.md)
