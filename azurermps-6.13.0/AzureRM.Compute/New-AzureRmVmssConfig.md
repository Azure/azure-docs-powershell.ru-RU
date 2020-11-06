---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561040"
---
# <span data-ttu-id="b994a-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b994a-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="b994a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b994a-102">SYNOPSIS</span></span>
<span data-ttu-id="b994a-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b994a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b994a-104">SYNTAX</span></span>

### <span data-ttu-id="b994a-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b994a-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b994a-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b994a-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
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

### <span data-ttu-id="b994a-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b994a-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b994a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b994a-108">DESCRIPTION</span></span>
<span data-ttu-id="b994a-109">Командлет **New-AzureRmVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b994a-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="b994a-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="b994a-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="b994a-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="b994a-111">These cmdlets are:</span></span>
- <span data-ttu-id="b994a-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="b994a-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="b994a-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b994a-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="b994a-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b994a-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="b994a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b994a-116">EXAMPLES</span></span>

### <span data-ttu-id="b994a-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="b994a-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="b994a-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="b994a-119">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="b994a-120">Вторая команда использует командлет **New-AzureRmVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="b994a-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="b994a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b994a-121">PARAMETERS</span></span>

### <span data-ttu-id="b994a-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b994a-122">-AssignIdentity</span></span>
<span data-ttu-id="b994a-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b994a-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b994a-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="b994a-125">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="b994a-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="b994a-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b994a-126">-BootDiagnostic</span></span>
<span data-ttu-id="b994a-127">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="b994a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-128">-DefaultProfile</span></span>
<span data-ttu-id="b994a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b994a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b994a-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="b994a-130">-DisableAutoRollback</span></span>
<span data-ttu-id="b994a-131">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="b994a-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="b994a-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="b994a-132">-EnableUltraSSD</span></span>
<span data-ttu-id="b994a-133">Обеспечивает возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="b994a-134">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="b994a-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="b994a-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b994a-135">-EvictionPolicy</span></span>
<span data-ttu-id="b994a-136">Задает политику вытеснения для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="b994a-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="b994a-137">-Расширение</span><span class="sxs-lookup"><span data-stu-id="b994a-137">-Extension</span></span>
<span data-ttu-id="b994a-138">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="b994a-139">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="b994a-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="b994a-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="b994a-140">-HealthProbeId</span></span>
<span data-ttu-id="b994a-141">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="b994a-142">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="b994a-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="b994a-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="b994a-143">-IdentityId</span></span>
<span data-ttu-id="b994a-144">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="b994a-145">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="b994a-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b994a-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b994a-146">-IdentityType</span></span>
<span data-ttu-id="b994a-147">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b994a-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="b994a-148">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="b994a-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="b994a-149">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b994a-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="b994a-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b994a-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b994a-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b994a-151">SystemAssigned</span></span>
- <span data-ttu-id="b994a-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="b994a-152">UserAssigned</span></span>
- <span data-ttu-id="b994a-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="b994a-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="b994a-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="b994a-154">None</span></span>

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

### <span data-ttu-id="b994a-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b994a-155">-LicenseType</span></span>
<span data-ttu-id="b994a-156">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b994a-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="b994a-157">-Location</span><span class="sxs-lookup"><span data-stu-id="b994a-157">-Location</span></span>
<span data-ttu-id="b994a-158">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="b994a-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b994a-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="b994a-160">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="b994a-161">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b994a-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="b994a-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-162">-OsProfile</span></span>
<span data-ttu-id="b994a-163">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="b994a-164">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="b994a-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="b994a-165">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="b994a-165">-Overprovision</span></span>
<span data-ttu-id="b994a-166">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="b994a-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b994a-167">-PlanName</span></span>
<span data-ttu-id="b994a-168">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="b994a-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="b994a-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b994a-169">-PlanProduct</span></span>
<span data-ttu-id="b994a-170">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="b994a-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="b994a-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="b994a-171">-PlanPromotionCode</span></span>
<span data-ttu-id="b994a-172">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="b994a-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="b994a-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b994a-173">-PlanPublisher</span></span>
<span data-ttu-id="b994a-174">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="b994a-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="b994a-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="b994a-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="b994a-176">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="b994a-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="b994a-177">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="b994a-177">-Priority</span></span>
<span data-ttu-id="b994a-178">Задает приоритет виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="b994a-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="b994a-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b994a-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="b994a-180">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="b994a-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="b994a-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b994a-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="b994a-182">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="b994a-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="b994a-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b994a-183">-SkuCapacity</span></span>
<span data-ttu-id="b994a-184">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="b994a-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b994a-185">-SkuName</span></span>
<span data-ttu-id="b994a-186">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="b994a-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b994a-187">-SkuTier</span></span>
<span data-ttu-id="b994a-188">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="b994a-189">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b994a-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b994a-190">Стандартная</span><span class="sxs-lookup"><span data-stu-id="b994a-190">Standard</span></span>
- <span data-ttu-id="b994a-191">Базового</span><span class="sxs-lookup"><span data-stu-id="b994a-191">Basic</span></span>

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

### <span data-ttu-id="b994a-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-192">-StorageProfile</span></span>
<span data-ttu-id="b994a-193">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="b994a-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="b994a-194">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="b994a-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="b994a-195">-Тег</span><span class="sxs-lookup"><span data-stu-id="b994a-195">-Tag</span></span>
<span data-ttu-id="b994a-196">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b994a-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b994a-197">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b994a-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b994a-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b994a-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="b994a-199">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="b994a-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="b994a-200">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b994a-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b994a-201">Автоматически</span><span class="sxs-lookup"><span data-stu-id="b994a-201">Automatic</span></span>
- <span data-ttu-id="b994a-202">Вручную</span><span class="sxs-lookup"><span data-stu-id="b994a-202">Manual</span></span>

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

### <span data-ttu-id="b994a-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="b994a-203">-Zone</span></span>
<span data-ttu-id="b994a-204">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b994a-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b994a-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="b994a-205">-ZoneBalance</span></span>
<span data-ttu-id="b994a-206">Следует ли принудительно использовать межплатформенные зоны распространения на всех компьютерах в случае сбоя зоны.</span><span class="sxs-lookup"><span data-stu-id="b994a-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="b994a-207">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b994a-207">-Confirm</span></span>
<span data-ttu-id="b994a-208">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b994a-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b994a-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b994a-209">-WhatIf</span></span>
<span data-ttu-id="b994a-210">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b994a-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b994a-211">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b994a-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b994a-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b994a-212">CommonParameters</span></span>
<span data-ttu-id="b994a-213">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b994a-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b994a-214">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b994a-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b994a-215">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b994a-215">INPUTS</span></span>

### <span data-ttu-id="b994a-216">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b994a-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b994a-217">System. String</span><span class="sxs-lookup"><span data-stu-id="b994a-217">System.String</span></span>

### <span data-ttu-id="b994a-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b994a-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b994a-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b994a-219">System.Int32</span></span>

### <span data-ttu-id="b994a-220">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b994a-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b994a-221">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="b994a-222">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="b994a-223">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b994a-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="b994a-224">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="b994a-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="b994a-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="b994a-225">System.String[]</span></span>

### <span data-ttu-id="b994a-226">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b994a-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="b994a-227">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b994a-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="b994a-228">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b994a-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b994a-229">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b994a-229">OUTPUTS</span></span>

### <span data-ttu-id="b994a-230">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b994a-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b994a-231">Пуск</span><span class="sxs-lookup"><span data-stu-id="b994a-231">NOTES</span></span>

## <span data-ttu-id="b994a-232">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b994a-232">RELATED LINKS</span></span>

[<span data-ttu-id="b994a-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="b994a-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="b994a-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="b994a-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b994a-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="b994a-236">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b994a-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="b994a-237">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b994a-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
