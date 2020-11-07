---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: e65bfa607f9689a85f7734b1913bbabadd4dd115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721817"
---
# <span data-ttu-id="d7784-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d7784-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="d7784-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7784-102">SYNOPSIS</span></span>
<span data-ttu-id="d7784-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="d7784-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7784-104">SYNTAX</span></span>

### <span data-ttu-id="d7784-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7784-105">DefaultParameterSet (Default)</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7784-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7784-106">ExplicitIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7784-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7784-107">AssignIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7784-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7784-108">DESCRIPTION</span></span>
<span data-ttu-id="d7784-109">Командлет **New-AzVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d7784-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="d7784-110">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="d7784-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="d7784-111">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="d7784-111">These cmdlets are:</span></span>
- <span data-ttu-id="d7784-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="d7784-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="d7784-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7784-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="d7784-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d7784-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="d7784-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7784-116">EXAMPLES</span></span>

### <span data-ttu-id="d7784-117">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="d7784-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="d7784-118">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="d7784-119">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="d7784-120">Вторая команда использует командлет **New-AzVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="d7784-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="d7784-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7784-121">PARAMETERS</span></span>

### <span data-ttu-id="d7784-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d7784-122">-AssignIdentity</span></span>
<span data-ttu-id="d7784-123">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d7784-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d7784-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="d7784-125">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="d7784-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="d7784-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d7784-126">-BootDiagnostic</span></span>
<span data-ttu-id="d7784-127">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="d7784-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-128">-DefaultProfile</span></span>
<span data-ttu-id="d7784-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7784-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7784-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="d7784-130">-DisableAutoRollback</span></span>
<span data-ttu-id="d7784-131">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="d7784-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="d7784-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="d7784-132">-EnableUltraSSD</span></span>
<span data-ttu-id="d7784-133">Обеспечивает возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="d7784-134">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="d7784-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="d7784-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7784-135">-EvictionPolicy</span></span>
<span data-ttu-id="d7784-136">Задает политику вытеснения для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="d7784-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="d7784-137">-Расширение</span><span class="sxs-lookup"><span data-stu-id="d7784-137">-Extension</span></span>
<span data-ttu-id="d7784-138">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="d7784-139">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="d7784-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d7784-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="d7784-140">-HealthProbeId</span></span>
<span data-ttu-id="d7784-141">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="d7784-142">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="d7784-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="d7784-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="d7784-143">-IdentityId</span></span>
<span data-ttu-id="d7784-144">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="d7784-145">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="d7784-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="d7784-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d7784-146">-IdentityType</span></span>
<span data-ttu-id="d7784-147">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d7784-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="d7784-148">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="d7784-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="d7784-149">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d7784-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="d7784-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d7784-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7784-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d7784-151">SystemAssigned</span></span>
- <span data-ttu-id="d7784-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="d7784-152">UserAssigned</span></span>
- <span data-ttu-id="d7784-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="d7784-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="d7784-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="d7784-154">None</span></span>

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

### <span data-ttu-id="d7784-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d7784-155">-LicenseType</span></span>
<span data-ttu-id="d7784-156">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="d7784-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="d7784-157">-Location</span><span class="sxs-lookup"><span data-stu-id="d7784-157">-Location</span></span>
<span data-ttu-id="d7784-158">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="d7784-159">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="d7784-159">-MaxPrice</span></span>
<span data-ttu-id="d7784-160">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-160">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="d7784-161">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="d7784-161">This price is in US Dollars.</span></span> <span data-ttu-id="d7784-162">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="d7784-162">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="d7784-163">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="d7784-163">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="d7784-164">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-164">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="d7784-165">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="d7784-165">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="d7784-166">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="d7784-166">Example: 0.01538.</span></span>  <span data-ttu-id="d7784-167">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="d7784-167">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="d7784-168">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="d7784-168">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="d7784-169">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7784-169">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="d7784-170">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-170">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="d7784-171">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d7784-171">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d7784-172">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-172">-OsProfile</span></span>
<span data-ttu-id="d7784-173">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-173">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="d7784-174">Для задания этого объекта можно использовать командлет **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="d7784-174">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d7784-175">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="d7784-175">-Overprovision</span></span>
<span data-ttu-id="d7784-176">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-176">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="d7784-177">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d7784-177">-PlanName</span></span>
<span data-ttu-id="d7784-178">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="d7784-178">Specifies the plan name.</span></span>

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

### <span data-ttu-id="d7784-179">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d7784-179">-PlanProduct</span></span>
<span data-ttu-id="d7784-180">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="d7784-180">Specifies the plan product.</span></span>

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

### <span data-ttu-id="d7784-181">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d7784-181">-PlanPromotionCode</span></span>
<span data-ttu-id="d7784-182">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="d7784-182">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="d7784-183">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d7784-183">-PlanPublisher</span></span>
<span data-ttu-id="d7784-184">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="d7784-184">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="d7784-185">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="d7784-185">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="d7784-186">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="d7784-186">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="d7784-187">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d7784-187">-Priority</span></span>
<span data-ttu-id="d7784-188">Задает приоритет виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="d7784-188">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="d7784-189">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d7784-189">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="d7784-190">Идентификатор ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d7784-190">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="d7784-191">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d7784-191">-RollingUpgradePolicy</span></span>
<span data-ttu-id="d7784-192">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="d7784-192">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="d7784-193">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d7784-193">-SinglePlacementGroup</span></span>
<span data-ttu-id="d7784-194">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="d7784-194">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="d7784-195">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d7784-195">-SkuCapacity</span></span>
<span data-ttu-id="d7784-196">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-196">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="d7784-197">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7784-197">-SkuName</span></span>
<span data-ttu-id="d7784-198">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-198">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="d7784-199">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d7784-199">-SkuTier</span></span>
<span data-ttu-id="d7784-200">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-200">Specifies the tier of VMSS.</span></span> <span data-ttu-id="d7784-201">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d7784-201">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7784-202">Стандартная</span><span class="sxs-lookup"><span data-stu-id="d7784-202">Standard</span></span>
- <span data-ttu-id="d7784-203">Базового</span><span class="sxs-lookup"><span data-stu-id="d7784-203">Basic</span></span>

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

### <span data-ttu-id="d7784-204">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-204">-StorageProfile</span></span>
<span data-ttu-id="d7784-205">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7784-205">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="d7784-206">Для задания этого объекта можно использовать командлет **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="d7784-206">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d7784-207">-Тег</span><span class="sxs-lookup"><span data-stu-id="d7784-207">-Tag</span></span>
<span data-ttu-id="d7784-208">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d7784-208">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d7784-209">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d7784-209">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d7784-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d7784-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="d7784-211">Настраиваемое время (в минутах) Удаление виртуальной машины может привести к утверждению запланированного события, прежде чем событие будет автоматически одобрено (время ожидания истекло).</span><span class="sxs-lookup"><span data-stu-id="d7784-211">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="d7784-212">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="d7784-212">-TerminateScheduledEvents</span></span>
<span data-ttu-id="d7784-213">Включение событий, запланированных на завершение</span><span class="sxs-lookup"><span data-stu-id="d7784-213">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="d7784-214">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d7784-214">-UpgradePolicyMode</span></span>
<span data-ttu-id="d7784-215">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="d7784-215">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="d7784-216">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d7784-216">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7784-217">Автоматически</span><span class="sxs-lookup"><span data-stu-id="d7784-217">Automatic</span></span>
- <span data-ttu-id="d7784-218">Вручную</span><span class="sxs-lookup"><span data-stu-id="d7784-218">Manual</span></span>

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

### <span data-ttu-id="d7784-219">-Zone</span><span class="sxs-lookup"><span data-stu-id="d7784-219">-Zone</span></span>
<span data-ttu-id="d7784-220">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d7784-220">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d7784-221">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="d7784-221">-ZoneBalance</span></span>
<span data-ttu-id="d7784-222">Следует ли принудительно использовать межплатформенные зоны распространения на всех компьютерах в случае сбоя зоны.</span><span class="sxs-lookup"><span data-stu-id="d7784-222">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="d7784-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7784-223">-Confirm</span></span>
<span data-ttu-id="d7784-224">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7784-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7784-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7784-225">-WhatIf</span></span>
<span data-ttu-id="d7784-226">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7784-226">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7784-227">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7784-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7784-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7784-228">CommonParameters</span></span>
<span data-ttu-id="d7784-229">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7784-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7784-230">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7784-230">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7784-231">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7784-231">INPUTS</span></span>

### <span data-ttu-id="d7784-232">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7784-232">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d7784-233">System. String</span><span class="sxs-lookup"><span data-stu-id="d7784-233">System.String</span></span>

### <span data-ttu-id="d7784-234">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7784-234">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d7784-235">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d7784-235">System.Int32</span></span>

### <span data-ttu-id="d7784-236">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d7784-236">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d7784-237">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-237">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="d7784-238">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-238">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="d7784-239">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d7784-239">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="d7784-240">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="d7784-240">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="d7784-241">System. String []</span><span class="sxs-lookup"><span data-stu-id="d7784-241">System.String[]</span></span>

### <span data-ttu-id="d7784-242">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d7784-242">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="d7784-243">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7784-243">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d7784-244">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d7784-244">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="d7784-245">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d7784-245">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d7784-246">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7784-246">OUTPUTS</span></span>

### <span data-ttu-id="d7784-247">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7784-247">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d7784-248">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7784-248">NOTES</span></span>

## <span data-ttu-id="d7784-249">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7784-249">RELATED LINKS</span></span>

[<span data-ttu-id="d7784-250">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-250">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="d7784-251">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d7784-251">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="d7784-252">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7784-252">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="d7784-253">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d7784-253">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="d7784-254">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7784-254">New-AzVmss</span></span>](./New-AzVmss.md)
