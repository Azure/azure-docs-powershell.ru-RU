---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316195"
---
# <span data-ttu-id="ecc02-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ecc02-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="ecc02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecc02-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc02-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="ecc02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecc02-104">SYNTAX</span></span>

### <span data-ttu-id="ecc02-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecc02-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc02-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc02-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecc02-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecc02-107">DESCRIPTION</span></span>
<span data-ttu-id="ecc02-108">Командлет **New-AzVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ecc02-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="ecc02-109">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="ecc02-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="ecc02-110">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="ecc02-110">These cmdlets are:</span></span>
- <span data-ttu-id="ecc02-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="ecc02-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="ecc02-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecc02-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ecc02-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ecc02-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="ecc02-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecc02-115">EXAMPLES</span></span>

### <span data-ttu-id="ecc02-116">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="ecc02-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="ecc02-117">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="ecc02-118">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="ecc02-119">Вторая команда использует командлет **New-AzVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="ecc02-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="ecc02-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ecc02-120">Example 2</span></span>

<span data-ttu-id="ecc02-121">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="ecc02-122">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="ecc02-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="ecc02-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecc02-123">PARAMETERS</span></span>

### <span data-ttu-id="ecc02-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="ecc02-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="ecc02-125">Количество времени, в течение которого автоматическое восстановление приостанавливается из-за изменения состояния в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ecc02-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="ecc02-126">Льготный период начинается после изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="ecc02-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="ecc02-127">Это поможет избежать преждевременного и случайного восстановления.</span><span class="sxs-lookup"><span data-stu-id="ecc02-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="ecc02-128">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ecc02-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="ecc02-129">Минимально допустимый льготный период составляет 30 минут (PT30M), который также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecc02-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="ecc02-130">Максимально допустимый льготный период составляет 90 минут (PT90M).</span><span class="sxs-lookup"><span data-stu-id="ecc02-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="ecc02-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ecc02-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="ecc02-132">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="ecc02-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ecc02-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ecc02-133">-BootDiagnostic</span></span>
<span data-ttu-id="ecc02-134">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ecc02-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-135">-DefaultProfile</span></span>
<span data-ttu-id="ecc02-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc02-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc02-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ecc02-137">-DisableAutoRollback</span></span>
<span data-ttu-id="ecc02-138">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="ecc02-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ecc02-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="ecc02-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="ecc02-140">Включает автоматическое восстановление на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ecc02-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ecc02-141">-EnableUltraSSD</span></span>
<span data-ttu-id="ecc02-142">Обеспечивает возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ecc02-143">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="ecc02-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ecc02-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ecc02-144">-EncryptionAtHost</span></span>
<span data-ttu-id="ecc02-145">Этот параметр включит шифрование для всех дисков, включая ресурс/временный диск на узле.</span><span class="sxs-lookup"><span data-stu-id="ecc02-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="ecc02-146">По умолчанию: шифрование на узле будет отключено, если это свойство не имеет значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ecc02-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="ecc02-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecc02-147">-EvictionPolicy</span></span>
<span data-ttu-id="ecc02-148">Задает политику вытеснения для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="ecc02-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="ecc02-149">-Расширение</span><span class="sxs-lookup"><span data-stu-id="ecc02-149">-Extension</span></span>
<span data-ttu-id="ecc02-150">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="ecc02-151">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="ecc02-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ecc02-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="ecc02-152">-HealthProbeId</span></span>
<span data-ttu-id="ecc02-153">Указывает идентификатор средства проверки подсистемы балансировки нагрузки, используемого для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="ecc02-154">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="ecc02-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="ecc02-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ecc02-155">-IdentityId</span></span>
<span data-ttu-id="ecc02-156">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ecc02-157">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="ecc02-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ecc02-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ecc02-158">-IdentityType</span></span>
<span data-ttu-id="ecc02-159">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecc02-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ecc02-160">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="ecc02-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ecc02-161">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecc02-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ecc02-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ecc02-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecc02-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ecc02-163">SystemAssigned</span></span>
- <span data-ttu-id="ecc02-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ecc02-164">UserAssigned</span></span>
- <span data-ttu-id="ecc02-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ecc02-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ecc02-166">Ничего</span><span class="sxs-lookup"><span data-stu-id="ecc02-166">None</span></span>

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

### <span data-ttu-id="ecc02-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ecc02-167">-LicenseType</span></span>
<span data-ttu-id="ecc02-168">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ecc02-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ecc02-169">-Location</span><span class="sxs-lookup"><span data-stu-id="ecc02-169">-Location</span></span>
<span data-ttu-id="ecc02-170">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ecc02-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ecc02-171">-MaxPrice</span></span>
<span data-ttu-id="ecc02-172">Максимальная цена, которую вы хотите заплатить за точку (VM) или VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="ecc02-173">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="ecc02-173">This price is in US Dollars.</span></span> <span data-ttu-id="ecc02-174">Эта цена будет сравниваться с текущей ценой по размеру ВМ.</span><span class="sxs-lookup"><span data-stu-id="ecc02-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="ecc02-175">Кроме того, цены проверяются во время создания или обновления плашечных виртуальных машин или VMSS, а операция будет выполнена только в том случае, если maxPrice больше текущей точки.</span><span class="sxs-lookup"><span data-stu-id="ecc02-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="ecc02-176">MaxPrice также будет использоваться для удаления точки ВМ/VMSS, если текущая цена точки выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ecc02-177">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="ecc02-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ecc02-178">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ecc02-178">Example: 0.01538.</span></span>  <span data-ttu-id="ecc02-179">-1 указывает на то, что точки VM и VMSS не должны выключаться для целей цены.</span><span class="sxs-lookup"><span data-stu-id="ecc02-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ecc02-180">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="ecc02-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ecc02-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecc02-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ecc02-182">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ecc02-183">Чтобы добавить этот объект, можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ecc02-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ecc02-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-184">-OsProfile</span></span>
<span data-ttu-id="ecc02-185">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ecc02-186">Для задания этого объекта можно использовать командлет **Set-AzVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="ecc02-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ecc02-187">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="ecc02-187">-Overprovision</span></span>
<span data-ttu-id="ecc02-188">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ecc02-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ecc02-189">-PlanName</span></span>
<span data-ttu-id="ecc02-190">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="ecc02-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ecc02-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ecc02-191">-PlanProduct</span></span>
<span data-ttu-id="ecc02-192">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="ecc02-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ecc02-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ecc02-193">-PlanPromotionCode</span></span>
<span data-ttu-id="ecc02-194">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="ecc02-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ecc02-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ecc02-195">-PlanPublisher</span></span>
<span data-ttu-id="ecc02-196">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="ecc02-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ecc02-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ecc02-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ecc02-198">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="ecc02-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="ecc02-199">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="ecc02-199">-Priority</span></span>
<span data-ttu-id="ecc02-200">Приоритет виртуального machien в множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="ecc02-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="ecc02-201">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="ecc02-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ecc02-202">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecc02-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ecc02-203">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecc02-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ecc02-204">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="ecc02-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ecc02-205">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="ecc02-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="ecc02-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ecc02-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ecc02-207">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="ecc02-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="ecc02-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ecc02-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="ecc02-209">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="ecc02-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="ecc02-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ecc02-210">-ScaleInPolicy</span></span>
<span data-ttu-id="ecc02-211">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ecc02-212">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="ecc02-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ecc02-213">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="ecc02-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ecc02-214">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="ecc02-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ecc02-215">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ecc02-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ecc02-216">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="ecc02-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ecc02-217">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="ecc02-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ecc02-218">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="ecc02-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ecc02-219">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="ecc02-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ecc02-220">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="ecc02-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ecc02-221">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="ecc02-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="ecc02-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ecc02-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="ecc02-223">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="ecc02-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ecc02-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ecc02-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ecc02-225">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="ecc02-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="ecc02-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ecc02-226">-SkuCapacity</span></span>
<span data-ttu-id="ecc02-227">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ecc02-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ecc02-228">-SkuName</span></span>
<span data-ttu-id="ecc02-229">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ecc02-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ecc02-230">-SkuTier</span></span>
<span data-ttu-id="ecc02-231">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="ecc02-232">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ecc02-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecc02-233">Стандартная</span><span class="sxs-lookup"><span data-stu-id="ecc02-233">Standard</span></span>
- <span data-ttu-id="ecc02-234">Базового</span><span class="sxs-lookup"><span data-stu-id="ecc02-234">Basic</span></span>

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

### <span data-ttu-id="ecc02-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-235">-StorageProfile</span></span>
<span data-ttu-id="ecc02-236">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecc02-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ecc02-237">Для задания этого объекта можно использовать командлет **Set-AzVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="ecc02-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ecc02-238">-Тег</span><span class="sxs-lookup"><span data-stu-id="ecc02-238">-Tag</span></span>
<span data-ttu-id="ecc02-239">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="ecc02-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ecc02-240">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ecc02-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ecc02-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ecc02-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ecc02-242">Настраиваемое время (в минутах) Удаление виртуальной машины может привести к утверждению запланированного события, прежде чем событие будет автоматически одобрено (время ожидания истекло).</span><span class="sxs-lookup"><span data-stu-id="ecc02-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ecc02-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ecc02-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ecc02-244">Включение событий, запланированных на завершение</span><span class="sxs-lookup"><span data-stu-id="ecc02-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="ecc02-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ecc02-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="ecc02-246">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="ecc02-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ecc02-247">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ecc02-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecc02-248">Автоматически</span><span class="sxs-lookup"><span data-stu-id="ecc02-248">Automatic</span></span>
- <span data-ttu-id="ecc02-249">Вручную</span><span class="sxs-lookup"><span data-stu-id="ecc02-249">Manual</span></span>

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

### <span data-ttu-id="ecc02-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="ecc02-250">-Zone</span></span>
<span data-ttu-id="ecc02-251">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ecc02-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ecc02-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="ecc02-252">-ZoneBalance</span></span>
<span data-ttu-id="ecc02-253">Следует ли принудительно использовать межплатформенные зоны распространения на всех компьютерах в случае сбоя зоны.</span><span class="sxs-lookup"><span data-stu-id="ecc02-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="ecc02-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecc02-254">-Confirm</span></span>
<span data-ttu-id="ecc02-255">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecc02-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc02-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc02-256">-WhatIf</span></span>
<span data-ttu-id="ecc02-257">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecc02-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecc02-258">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecc02-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc02-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc02-259">CommonParameters</span></span>
<span data-ttu-id="ecc02-260">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecc02-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc02-261">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc02-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc02-262">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecc02-262">INPUTS</span></span>

### <span data-ttu-id="ecc02-263">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ecc02-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ecc02-264">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc02-264">System.String</span></span>

### <span data-ttu-id="ecc02-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecc02-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ecc02-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ecc02-266">System.Int32</span></span>

### <span data-ttu-id="ecc02-267">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. UpgradeMode, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ecc02-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ecc02-268">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="ecc02-269">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="ecc02-270">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ecc02-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="ecc02-271">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="ecc02-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="ecc02-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="ecc02-272">System.String[]</span></span>

### <span data-ttu-id="ecc02-273">Microsoft. Azure. Management. COMPUTE. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ecc02-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="ecc02-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ecc02-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ecc02-275">Microsoft. Azure. Management. COMPUTE. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ecc02-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="ecc02-276">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. ResourceIdentityType, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ecc02-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ecc02-277">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecc02-277">OUTPUTS</span></span>

### <span data-ttu-id="ecc02-278">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ecc02-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ecc02-279">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecc02-279">NOTES</span></span>

## <span data-ttu-id="ecc02-280">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecc02-280">RELATED LINKS</span></span>

[<span data-ttu-id="ecc02-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="ecc02-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="ecc02-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecc02-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ecc02-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ecc02-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="ecc02-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecc02-285">New-AzVmss</span></span>](./New-AzVmss.md)
