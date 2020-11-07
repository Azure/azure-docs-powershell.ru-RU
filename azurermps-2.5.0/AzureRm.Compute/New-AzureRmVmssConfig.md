---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914581"
---
# <span data-ttu-id="acb52-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="acb52-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="acb52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acb52-102">SYNOPSIS</span></span>
<span data-ttu-id="acb52-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acb52-104">SYNTAX</span></span>

### <span data-ttu-id="acb52-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acb52-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acb52-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb52-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
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

### <span data-ttu-id="acb52-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb52-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acb52-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acb52-108">DESCRIPTION</span></span>
<span data-ttu-id="acb52-109">Командлет **New-AzureRmVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="acb52-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="acb52-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="acb52-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="acb52-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="acb52-111">These cmdlets are:</span></span>

- <span data-ttu-id="acb52-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="acb52-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="acb52-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="acb52-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="acb52-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="acb52-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="acb52-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acb52-116">EXAMPLES</span></span>

### <span data-ttu-id="acb52-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="acb52-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="acb52-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="acb52-119">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="acb52-120">Вторая команда использует командлет **New-AzureRmVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="acb52-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="acb52-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acb52-121">PARAMETERS</span></span>

### <span data-ttu-id="acb52-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="acb52-122">-AssignIdentity</span></span>
<span data-ttu-id="acb52-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="acb52-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="acb52-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="acb52-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="acb52-125">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="acb52-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="acb52-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="acb52-126">-BootDiagnostic</span></span>
<span data-ttu-id="acb52-127">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="acb52-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="acb52-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-128">-DefaultProfile</span></span>
<span data-ttu-id="acb52-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acb52-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb52-130">-Расширение</span><span class="sxs-lookup"><span data-stu-id="acb52-130">-Extension</span></span>
<span data-ttu-id="acb52-131">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="acb52-132">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="acb52-132">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="acb52-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="acb52-133">-HealthProbeId</span></span>
<span data-ttu-id="acb52-134">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="acb52-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="acb52-135">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="acb52-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="acb52-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="acb52-136">-IdentityId</span></span>
<span data-ttu-id="acb52-137">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="acb52-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="acb52-138">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="acb52-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="acb52-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="acb52-139">-IdentityType</span></span>
<span data-ttu-id="acb52-140">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="acb52-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="acb52-141">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="acb52-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="acb52-142">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="acb52-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="acb52-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="acb52-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="acb52-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="acb52-144">SystemAssigned</span></span>
- <span data-ttu-id="acb52-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="acb52-145">UserAssigned</span></span>
- <span data-ttu-id="acb52-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="acb52-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="acb52-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="acb52-147">None</span></span>

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

### <span data-ttu-id="acb52-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="acb52-148">-LicenseType</span></span>
<span data-ttu-id="acb52-149">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="acb52-149">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="acb52-150">-Location</span><span class="sxs-lookup"><span data-stu-id="acb52-150">-Location</span></span>
<span data-ttu-id="acb52-151">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-151">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="acb52-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="acb52-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="acb52-153">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="acb52-154">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="acb52-154">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="acb52-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-155">-OsProfile</span></span>
<span data-ttu-id="acb52-156">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="acb52-157">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="acb52-157">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="acb52-158">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="acb52-158">-Overprovision</span></span>
<span data-ttu-id="acb52-159">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="acb52-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="acb52-160">-PlanName</span></span>
<span data-ttu-id="acb52-161">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="acb52-161">Specifies the plan name.</span></span>

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

### <span data-ttu-id="acb52-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="acb52-162">-PlanProduct</span></span>
<span data-ttu-id="acb52-163">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="acb52-163">Specifies the plan product.</span></span>

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

### <span data-ttu-id="acb52-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="acb52-164">-PlanPromotionCode</span></span>
<span data-ttu-id="acb52-165">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="acb52-165">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="acb52-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="acb52-166">-PlanPublisher</span></span>
<span data-ttu-id="acb52-167">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="acb52-167">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="acb52-168">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="acb52-168">-Priority</span></span>
<span data-ttu-id="acb52-169">Задает приоритет виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="acb52-169">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="acb52-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="acb52-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="acb52-171">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="acb52-171">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="acb52-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="acb52-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="acb52-173">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="acb52-173">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="acb52-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="acb52-174">-SkuCapacity</span></span>
<span data-ttu-id="acb52-175">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-175">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="acb52-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="acb52-176">-SkuName</span></span>
<span data-ttu-id="acb52-177">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-177">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="acb52-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="acb52-178">-SkuTier</span></span>
<span data-ttu-id="acb52-179">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="acb52-180">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="acb52-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="acb52-181">Стандартная</span><span class="sxs-lookup"><span data-stu-id="acb52-181">Standard</span></span>
- <span data-ttu-id="acb52-182">Базового</span><span class="sxs-lookup"><span data-stu-id="acb52-182">Basic</span></span>

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

### <span data-ttu-id="acb52-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-183">-StorageProfile</span></span>
<span data-ttu-id="acb52-184">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="acb52-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="acb52-185">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="acb52-185">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="acb52-186">-Тег</span><span class="sxs-lookup"><span data-stu-id="acb52-186">-Tag</span></span>
<span data-ttu-id="acb52-187">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="acb52-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="acb52-188">Например:</span><span class="sxs-lookup"><span data-stu-id="acb52-188">For example:</span></span>

<span data-ttu-id="acb52-189">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="acb52-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="acb52-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="acb52-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="acb52-191">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="acb52-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="acb52-192">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="acb52-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="acb52-193">Автоматически</span><span class="sxs-lookup"><span data-stu-id="acb52-193">Automatic</span></span>
- <span data-ttu-id="acb52-194">Вручную</span><span class="sxs-lookup"><span data-stu-id="acb52-194">Manual</span></span>

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

### <span data-ttu-id="acb52-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="acb52-195">-Zone</span></span>
<span data-ttu-id="acb52-196">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="acb52-196">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="acb52-197">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acb52-197">-Confirm</span></span>
<span data-ttu-id="acb52-198">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acb52-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acb52-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb52-199">-WhatIf</span></span>
<span data-ttu-id="acb52-200">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acb52-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acb52-201">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acb52-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acb52-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb52-202">CommonParameters</span></span>
<span data-ttu-id="acb52-203">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acb52-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb52-204">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb52-204">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb52-205">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acb52-205">INPUTS</span></span>

### <span data-ttu-id="acb52-206">Ничего</span><span class="sxs-lookup"><span data-stu-id="acb52-206">None</span></span>
<span data-ttu-id="acb52-207">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="acb52-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acb52-208">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acb52-208">OUTPUTS</span></span>

### <span data-ttu-id="acb52-209">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="acb52-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="acb52-210">Пуск</span><span class="sxs-lookup"><span data-stu-id="acb52-210">NOTES</span></span>

## <span data-ttu-id="acb52-211">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acb52-211">RELATED LINKS</span></span>

[<span data-ttu-id="acb52-212">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-212">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="acb52-213">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="acb52-213">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="acb52-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="acb52-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="acb52-215">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="acb52-215">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="acb52-216">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="acb52-216">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
