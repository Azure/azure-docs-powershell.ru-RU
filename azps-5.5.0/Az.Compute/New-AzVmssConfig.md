---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211716"
---
# <span data-ttu-id="21144-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="21144-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="21144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21144-102">SYNOPSIS</span></span>
<span data-ttu-id="21144-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="21144-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21144-104">SYNTAX</span></span>

### <span data-ttu-id="21144-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21144-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="21144-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="21144-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="21144-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21144-107">DESCRIPTION</span></span>
<span data-ttu-id="21144-108">Для создания настраиваемого локального набора масштаба виртуальный руководитель (VMSS) создается настраиваемый объект **New-AzVmssConfig.**</span><span class="sxs-lookup"><span data-stu-id="21144-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="21144-109">Для настройки объекта VMSS необходимы другие cmdlets.</span><span class="sxs-lookup"><span data-stu-id="21144-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="21144-110">Вот такие cmdlets:</span><span class="sxs-lookup"><span data-stu-id="21144-110">These cmdlets are:</span></span>
- <span data-ttu-id="21144-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="21144-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="21144-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="21144-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="21144-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="21144-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="21144-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="21144-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="21144-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21144-115">EXAMPLES</span></span>

### <span data-ttu-id="21144-116">Пример 1. Создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="21144-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="21144-117">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="21144-118">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="21144-119">Вторая команда использует командлет **New-AzVmss** для создания VMSS, который использует объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="21144-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="21144-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="21144-120">Example 2</span></span>

<span data-ttu-id="21144-121">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="21144-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="21144-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="21144-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21144-123">PARAMETERS</span></span>

### <span data-ttu-id="21144-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="21144-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="21144-125">Время, на которое автоматические восстановления приостановлены из-за изменения состояния в VM.</span><span class="sxs-lookup"><span data-stu-id="21144-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="21144-126">Время отсрочки начинается после завершения изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="21144-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="21144-127">Это помогает избежать случайного или случайного восстановления.</span><span class="sxs-lookup"><span data-stu-id="21144-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="21144-128">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="21144-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="21144-129">Минимальный допустимый период отсрочки составляет 30 минут (PT30M), что также является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21144-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="21144-130">Максимальный допустимый период отсрочки составляет 90 минут (PT90M).</span><span class="sxs-lookup"><span data-stu-id="21144-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="21144-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="21144-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="21144-132">Определяет, следует ли автоматически применять обновления ОС для масштабирования экземпляров набора в скользячем режиме при обновлении изображения.</span><span class="sxs-lookup"><span data-stu-id="21144-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="21144-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="21144-133">-BootDiagnostic</span></span>
<span data-ttu-id="21144-134">Определяет профиль диагностики загрузки в масштабе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="21144-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21144-135">-DefaultProfile</span></span>
<span data-ttu-id="21144-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21144-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21144-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="21144-137">-DisableAutoRollback</span></span>
<span data-ttu-id="21144-138">Отключение автоматического отката для политики обновления автоматической ОС</span><span class="sxs-lookup"><span data-stu-id="21144-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="21144-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="21144-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="21144-140">Включает автоматическое восстановление с установленным масштабом виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="21144-141">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="21144-141">-EnableUltraSSD</span></span>
<span data-ttu-id="21144-142">Позволяет использовать один или несколько управляемых дисков данных с учетной записью UltraSSD_LRS типа учетной записи хранения в наборе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="21144-143">Управляемые диски с типом учетной UltraSSD_LRS можно добавить на VMSS, только если это свойство включено.</span><span class="sxs-lookup"><span data-stu-id="21144-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="21144-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="21144-144">-EncryptionAtHost</span></span>
<span data-ttu-id="21144-145">Этот параметр включает шифрование для всех дисков, включая диск Resource/Temp на самом хосте.</span><span class="sxs-lookup"><span data-stu-id="21144-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="21144-146">По умолчанию: шифрование на хосте будет отключено, если для этого свойства не установлено значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="21144-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="21144-147">-ВуассионПолиция</span><span class="sxs-lookup"><span data-stu-id="21144-147">-EvictionPolicy</span></span>
<span data-ttu-id="21144-148">Определяет политику присоединения к виртуальным машинам в наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="21144-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="21144-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="21144-149">-Extension</span></span>
<span data-ttu-id="21144-150">Указывает информационный объект расширения для VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="21144-151">Для добавления этого объекта можно использовать **cmdlet Add-AzVmssExtension.**</span><span class="sxs-lookup"><span data-stu-id="21144-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="21144-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="21144-152">-HealthProbeId</span></span>
<span data-ttu-id="21144-153">Определяет ИД экземпляра, используемого для определения состояния экземпляра в наборе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="21144-154">Шаблон HealthProbeId имеет форму '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/10/12/{имяФокнамя}".</span><span class="sxs-lookup"><span data-stu-id="21144-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="21144-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="21144-155">-IdentityId</span></span>
<span data-ttu-id="21144-156">Определяет список удостоверений пользователей, связанных с набором масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="21144-157">Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="21144-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="21144-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="21144-158">-IdentityType</span></span>
<span data-ttu-id="21144-159">Определяет тип удостоверения, используемого для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="21144-160">Тип SystemAssignedUserAssigned включает неявно созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="21144-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="21144-161">Тип "Нет" удаляет все удостоверения из набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="21144-162">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="21144-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21144-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="21144-163">SystemAssigned</span></span>
- <span data-ttu-id="21144-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="21144-164">UserAssigned</span></span>
- <span data-ttu-id="21144-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="21144-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="21144-166">Нет</span><span class="sxs-lookup"><span data-stu-id="21144-166">None</span></span>

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

### <span data-ttu-id="21144-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="21144-167">-LicenseType</span></span>
<span data-ttu-id="21144-168">Укажите тип лицензии, который будет выводить на себя.</span><span class="sxs-lookup"><span data-stu-id="21144-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="21144-169">-Location</span><span class="sxs-lookup"><span data-stu-id="21144-169">-Location</span></span>
<span data-ttu-id="21144-170">Указывает расположение Azure, в котором создается служба VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="21144-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="21144-171">-MaxPrice</span></span>
<span data-ttu-id="21144-172">Указывает максимальную цену, которую вы будете оплачивать spot VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="21144-173">Эта цена в долларах США.</span><span class="sxs-lookup"><span data-stu-id="21144-173">This price is in US Dollars.</span></span> <span data-ttu-id="21144-174">Эта цена будет сравниваться с текущей точечная цена для размера VM.</span><span class="sxs-lookup"><span data-stu-id="21144-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="21144-175">Кроме того, цены сравниваются во время создания или обновления spot VM/VMSS и операция будет работать только в том случае, если максимальное значение больше текущей цены Spot.</span><span class="sxs-lookup"><span data-stu-id="21144-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="21144-176">Максимальное значение будет также использоваться для создания точечная VM-или VMSS, если текущая цена за текущий момент выходит за пределы максимальной цены после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="21144-177">Возможные значения: любое десятичее значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="21144-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="21144-178">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="21144-178">Example: 0.01538.</span></span>  <span data-ttu-id="21144-179">-1 означает, что spot VM/VMSS не следует захламлять по ценам.</span><span class="sxs-lookup"><span data-stu-id="21144-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="21144-180">Кроме того, максимальная цена по умолчанию составляет -1, если она не предоставлена вами.</span><span class="sxs-lookup"><span data-stu-id="21144-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="21144-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="21144-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="21144-182">Определяет объект профиля сети, который содержит свойства сети для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="21144-183">Для добавления этого объекта можно использовать командлет **Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="21144-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="21144-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="21144-184">-OsProfile</span></span>
<span data-ttu-id="21144-185">Определяет объект профиля операционной системы, который содержит свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="21144-186">Для этого объекта можно использовать **cmdlet Set-AzVmssOsProfile.**</span><span class="sxs-lookup"><span data-stu-id="21144-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="21144-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="21144-187">-Overprovision</span></span>
<span data-ttu-id="21144-188">Указывает, является ли cmdlet перенастройка VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="21144-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="21144-189">-PlanName</span></span>
<span data-ttu-id="21144-190">Название плана.</span><span class="sxs-lookup"><span data-stu-id="21144-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="21144-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="21144-191">-PlanProduct</span></span>
<span data-ttu-id="21144-192">Продукт плана.</span><span class="sxs-lookup"><span data-stu-id="21144-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="21144-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="21144-193">-PlanPromotionCode</span></span>
<span data-ttu-id="21144-194">Определяет рекламный код плана.</span><span class="sxs-lookup"><span data-stu-id="21144-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="21144-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="21144-195">-PlanPublisher</span></span>
<span data-ttu-id="21144-196">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="21144-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="21144-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="21144-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="21144-198">Количество ошибок домена для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="21144-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="21144-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="21144-199">-Priority</span></span>
<span data-ttu-id="21144-200">Приоритет виртуального мачина в наборе шкал.</span><span class="sxs-lookup"><span data-stu-id="21144-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="21144-201">Поддерживаются только такие значения, как "Обычный", "Spot" и "Низкий".</span><span class="sxs-lookup"><span data-stu-id="21144-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="21144-202">"Обычный" — для обычных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="21144-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="21144-203">Spot — для spot virtual machine.</span><span class="sxs-lookup"><span data-stu-id="21144-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="21144-204">"Низкая" также для spot virtual machine, но заменяется spot.</span><span class="sxs-lookup"><span data-stu-id="21144-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="21144-205">Используйте "Spot" вместо "Низкий".</span><span class="sxs-lookup"><span data-stu-id="21144-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="21144-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="21144-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="21144-207">The resource id of the Proximity Placement Group to use with this scale set.</span><span class="sxs-lookup"><span data-stu-id="21144-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="21144-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="21144-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="21144-209">Определяет политику обновления.</span><span class="sxs-lookup"><span data-stu-id="21144-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="21144-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="21144-210">-ScaleInPolicy</span></span>
<span data-ttu-id="21144-211">Правила, которые следует соблюдать при масштабирование в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="21144-212">Возможные значения: Default, 'OldestVM' и 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="21144-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="21144-213">При масштабе набора виртуальных машин набор "По умолчанию" сначала будет балансироваться в разных зонах, если он является набором золонного масштаба.</span><span class="sxs-lookup"><span data-stu-id="21144-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="21144-214">Затем он будет как можно остаток на балансе по всем доменам fault Domains.</span><span class="sxs-lookup"><span data-stu-id="21144-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="21144-215">В каждом домене ошибок будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="21144-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="21144-216">При масштабирования набора виртуальных машин "OldestVM" будут выбраны старые виртуальные машины, которые не защищены от масштаба.</span><span class="sxs-lookup"><span data-stu-id="21144-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21144-217">Для наборов шкалы виртуальной машины в зоальбовом масштабе сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="21144-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21144-218">В каждой зоне выбираются старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="21144-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="21144-219">При масштабе масштабирования набора виртуальных машин будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="21144-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21144-220">Для наборов шкалы виртуальной машины в зоальбовом масштабе сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="21144-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21144-221">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="21144-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="21144-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="21144-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="21144-223">Определяет группу одного размещения.</span><span class="sxs-lookup"><span data-stu-id="21144-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="21144-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="21144-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="21144-225">Указывает, что расширения не запускаются для лишних перезапроизводиных VMs.</span><span class="sxs-lookup"><span data-stu-id="21144-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="21144-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="21144-226">-SkuCapacity</span></span>
<span data-ttu-id="21144-227">Количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="21144-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="21144-228">-SkuName</span></span>
<span data-ttu-id="21144-229">Определяет размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="21144-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="21144-230">-SkuTier</span></span>
<span data-ttu-id="21144-231">Определяет уровень службы VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="21144-232">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="21144-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21144-233">Стандартный</span><span class="sxs-lookup"><span data-stu-id="21144-233">Standard</span></span>
- <span data-ttu-id="21144-234">Базовая</span><span class="sxs-lookup"><span data-stu-id="21144-234">Basic</span></span>

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

### <span data-ttu-id="21144-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="21144-235">-StorageProfile</span></span>
<span data-ttu-id="21144-236">Определяет объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="21144-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="21144-237">Для этого объекта можно использовать **cmdlet Set-AzVmssStorageProfile.**</span><span class="sxs-lookup"><span data-stu-id="21144-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="21144-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="21144-238">-Tag</span></span>
<span data-ttu-id="21144-239">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="21144-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21144-240">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="21144-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="21144-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="21144-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="21144-242">Настраиваемая продолжительность удаления виртуальной машины (в минутах) может утвердить запланированное событие", прежде чем событие будет утверждено автоматически (по времени).</span><span class="sxs-lookup"><span data-stu-id="21144-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="21144-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="21144-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="21144-244">Enable the Terminate Scheduled events</span><span class="sxs-lookup"><span data-stu-id="21144-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="21144-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="21144-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="21144-246">В наборе масштабов указан режим обновления до виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="21144-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="21144-247">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="21144-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21144-248">Автоматически</span><span class="sxs-lookup"><span data-stu-id="21144-248">Automatic</span></span>
- <span data-ttu-id="21144-249">Вручную</span><span class="sxs-lookup"><span data-stu-id="21144-249">Manual</span></span>

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

### <span data-ttu-id="21144-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="21144-250">-Zone</span></span>
<span data-ttu-id="21144-251">Список зон для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21144-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="21144-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="21144-252">-ZoneBalance</span></span>
<span data-ttu-id="21144-253">Должен ли действовать строго даже распределение виртуальной машины через зоны x в случае простоя зоны.</span><span class="sxs-lookup"><span data-stu-id="21144-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="21144-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21144-254">-Confirm</span></span>
<span data-ttu-id="21144-255">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21144-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21144-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21144-256">-WhatIf</span></span>
<span data-ttu-id="21144-257">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21144-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21144-258">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="21144-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21144-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21144-259">CommonParameters</span></span>
<span data-ttu-id="21144-260">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21144-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21144-261">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21144-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21144-262">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21144-262">INPUTS</span></span>

### <span data-ttu-id="21144-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="21144-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="21144-264">System.String</span><span class="sxs-lookup"><span data-stu-id="21144-264">System.String</span></span>

### <span data-ttu-id="21144-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="21144-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="21144-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="21144-266">System.Int32</span></span>

### <span data-ttu-id="21144-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="21144-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="21144-268">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="21144-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="21144-269">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="21144-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="21144-270">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="21144-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="21144-271">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="21144-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="21144-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="21144-272">System.String[]</span></span>

### <span data-ttu-id="21144-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="21144-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="21144-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21144-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="21144-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="21144-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="21144-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="21144-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="21144-277">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21144-277">OUTPUTS</span></span>

### <span data-ttu-id="21144-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="21144-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="21144-279">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21144-279">NOTES</span></span>

## <span data-ttu-id="21144-280">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21144-280">RELATED LINKS</span></span>

[<span data-ttu-id="21144-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="21144-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="21144-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="21144-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="21144-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="21144-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="21144-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="21144-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="21144-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21144-285">New-AzVmss</span></span>](./New-AzVmss.md)
