---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734572"
---
# <span data-ttu-id="48b10-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="48b10-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="48b10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48b10-102">SYNOPSIS</span></span>
<span data-ttu-id="48b10-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48b10-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b10-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b10-105">DESCRIPTION</span></span>
<span data-ttu-id="48b10-106">Командлет **New-AzureRmVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="48b10-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="48b10-107">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="48b10-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="48b10-108">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="48b10-108">These cmdlets are:</span></span>

- <span data-ttu-id="48b10-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="48b10-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="48b10-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b10-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="48b10-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="48b10-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="48b10-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48b10-113">EXAMPLES</span></span>

### <span data-ttu-id="48b10-114">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="48b10-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="48b10-115">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="48b10-116">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="48b10-117">Вторая команда использует командлет **New-AzureRmVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="48b10-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="48b10-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48b10-118">PARAMETERS</span></span>

### <span data-ttu-id="48b10-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="48b10-119">-AssignIdentity</span></span>
<span data-ttu-id="48b10-120">Укажите учетную запись, назначенную системой, для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="48b10-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b10-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="48b10-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="48b10-122">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="48b10-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b10-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="48b10-123">-BootDiagnostic</span></span>
<span data-ttu-id="48b10-124">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="48b10-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="48b10-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-125">-DefaultProfile</span></span>
<span data-ttu-id="48b10-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48b10-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b10-127">-Расширение</span><span class="sxs-lookup"><span data-stu-id="48b10-127">-Extension</span></span>
<span data-ttu-id="48b10-128">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="48b10-129">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="48b10-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="48b10-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="48b10-130">-HealthProbeId</span></span>
<span data-ttu-id="48b10-131">Укажите идентификатор проверки подсистемы балансировки нагрузки, используемой для определения работоспособности экземпляра в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="48b10-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="48b10-132">HealthProbeId имеет вид "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".</span><span class="sxs-lookup"><span data-stu-id="48b10-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="48b10-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="48b10-133">-IdentityType</span></span>
<span data-ttu-id="48b10-134">Укажите удостоверение набора масштабов виртуальной машины, если оно настроено.</span><span class="sxs-lookup"><span data-stu-id="48b10-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b10-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="48b10-135">-LicenseType</span></span>
<span data-ttu-id="48b10-136">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="48b10-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="48b10-137">-Location</span><span class="sxs-lookup"><span data-stu-id="48b10-137">-Location</span></span>
<span data-ttu-id="48b10-138">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="48b10-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b10-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="48b10-140">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="48b10-141">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="48b10-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="48b10-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-142">-OsProfile</span></span>
<span data-ttu-id="48b10-143">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="48b10-144">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="48b10-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="48b10-145">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="48b10-145">-Overprovision</span></span>
<span data-ttu-id="48b10-146">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="48b10-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="48b10-147">-PlanName</span></span>
<span data-ttu-id="48b10-148">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="48b10-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="48b10-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="48b10-149">-PlanProduct</span></span>
<span data-ttu-id="48b10-150">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="48b10-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="48b10-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="48b10-151">-PlanPromotionCode</span></span>
<span data-ttu-id="48b10-152">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="48b10-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="48b10-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="48b10-153">-PlanPublisher</span></span>
<span data-ttu-id="48b10-154">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="48b10-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="48b10-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="48b10-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="48b10-156">Укажите политику восстановления.</span><span class="sxs-lookup"><span data-stu-id="48b10-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b10-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="48b10-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="48b10-158">Указывает политику чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="48b10-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="48b10-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="48b10-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="48b10-160">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="48b10-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="48b10-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="48b10-161">-SkuCapacity</span></span>
<span data-ttu-id="48b10-162">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b10-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="48b10-163">-SkuName</span></span>
<span data-ttu-id="48b10-164">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="48b10-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="48b10-165">-SkuTier</span></span>
<span data-ttu-id="48b10-166">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="48b10-167">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48b10-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48b10-168">Стандартная</span><span class="sxs-lookup"><span data-stu-id="48b10-168">Standard</span></span>
- <span data-ttu-id="48b10-169">Базового</span><span class="sxs-lookup"><span data-stu-id="48b10-169">Basic</span></span>

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

### <span data-ttu-id="48b10-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-170">-StorageProfile</span></span>
<span data-ttu-id="48b10-171">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="48b10-172">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="48b10-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="48b10-173">-Тег</span><span class="sxs-lookup"><span data-stu-id="48b10-173">-Tag</span></span>
<span data-ttu-id="48b10-174">Указывает теги, которые будут назначены для VMSS.</span><span class="sxs-lookup"><span data-stu-id="48b10-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="48b10-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="48b10-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="48b10-176">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="48b10-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="48b10-177">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48b10-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48b10-178">Автоматически</span><span class="sxs-lookup"><span data-stu-id="48b10-178">Automatic</span></span>
- <span data-ttu-id="48b10-179">Вручную</span><span class="sxs-lookup"><span data-stu-id="48b10-179">Manual</span></span>

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

### <span data-ttu-id="48b10-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="48b10-180">-Zone</span></span>
<span data-ttu-id="48b10-181">Указывает список зон для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="48b10-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="48b10-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48b10-182">-Confirm</span></span>
<span data-ttu-id="48b10-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48b10-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b10-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b10-184">-WhatIf</span></span>
<span data-ttu-id="48b10-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48b10-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48b10-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48b10-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b10-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b10-187">CommonParameters</span></span>
<span data-ttu-id="48b10-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48b10-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b10-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b10-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b10-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48b10-190">INPUTS</span></span>

## <span data-ttu-id="48b10-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b10-191">OUTPUTS</span></span>

### <span data-ttu-id="48b10-192">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="48b10-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="48b10-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="48b10-193">NOTES</span></span>

## <span data-ttu-id="48b10-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48b10-194">RELATED LINKS</span></span>

[<span data-ttu-id="48b10-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="48b10-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="48b10-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="48b10-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b10-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="48b10-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="48b10-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="48b10-199">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b10-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


