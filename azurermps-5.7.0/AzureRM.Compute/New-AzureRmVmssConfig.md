---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561899"
---
# <span data-ttu-id="8c4e0-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8c4e0-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="8c4e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4e0-103">Создает объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c4e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c4e0-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c4e0-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4e0-106">Командлет **New-AzureRmVmssConfig** создает настраиваемый локальный объект Virtual Configuration Manager (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8c4e0-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="8c4e0-107">Для настройки объекта VMSS необходимы другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="8c4e0-108">Ниже приведены эти командлеты.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-108">These cmdlets are:</span></span>

- <span data-ttu-id="8c4e0-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="8c4e0-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="8c4e0-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c4e0-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="8c4e0-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8c4e0-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8c4e0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c4e0-113">EXAMPLES</span></span>

### <span data-ttu-id="8c4e0-114">Пример 1: создание объекта конфигурации VMSS</span><span class="sxs-lookup"><span data-stu-id="8c4e0-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="8c4e0-115">В этом примере создается объект конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="8c4e0-116">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8c4e0-117">Вторая команда использует командлет **New-AzureRmVmss** для создания VMSS, использующего объект конфигурации VMSS, созданный в первой команде.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="8c4e0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c4e0-118">PARAMETERS</span></span>

### <span data-ttu-id="8c4e0-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c4e0-119">-BootDiagnostic</span></span>
<span data-ttu-id="8c4e0-120">Указывает, что установлен профиль диагностики загрузки для шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="8c4e0-121">-Расширение</span><span class="sxs-lookup"><span data-stu-id="8c4e0-121">-Extension</span></span>
<span data-ttu-id="8c4e0-122">Указывает объект расширения данных для VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="8c4e0-123">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssExtension** .</span><span class="sxs-lookup"><span data-stu-id="8c4e0-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="8c4e0-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8c4e0-124">-IdentityType</span></span>
<span data-ttu-id="8c4e0-125">Укажите удостоверение набора масштабов виртуальной машины, если оно настроено.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e0-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8c4e0-126">-LicenseType</span></span>
<span data-ttu-id="8c4e0-127">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="8c4e0-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8c4e0-128">-Location</span></span>
<span data-ttu-id="8c4e0-129">Указывает расположение Azure, в котором создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="8c4e0-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c4e0-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="8c4e0-131">Указывает объект сетевого профиля, который содержит сетевые свойства для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="8c4e0-132">Чтобы добавить этот объект, можно использовать командлет **Add-AzureRmVmssNetworkInterfaceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="8c4e0-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="8c4e0-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-133">-OsProfile</span></span>
<span data-ttu-id="8c4e0-134">Указывает объект профиля операционной системы, содержащий свойства операционной системы для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="8c4e0-135">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssOsProfile** .</span><span class="sxs-lookup"><span data-stu-id="8c4e0-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="8c4e0-136">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="8c4e0-136">-Overprovision</span></span>
<span data-ttu-id="8c4e0-137">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="8c4e0-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8c4e0-138">-PlanName</span></span>
<span data-ttu-id="8c4e0-139">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="8c4e0-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="8c4e0-140">-PlanProduct</span></span>
<span data-ttu-id="8c4e0-141">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="8c4e0-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="8c4e0-142">-PlanPromotionCode</span></span>
<span data-ttu-id="8c4e0-143">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="8c4e0-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8c4e0-144">-PlanPublisher</span></span>
<span data-ttu-id="8c4e0-145">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="8c4e0-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8c4e0-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="8c4e0-147">Укажите политику восстановления.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e0-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8c4e0-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="8c4e0-149">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="8c4e0-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8c4e0-150">-SkuCapacity</span></span>
<span data-ttu-id="8c4e0-151">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e0-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8c4e0-152">-SkuName</span></span>
<span data-ttu-id="8c4e0-153">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="8c4e0-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8c4e0-154">-SkuTier</span></span>
<span data-ttu-id="8c4e0-155">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="8c4e0-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8c4e0-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c4e0-157">Стандартная</span><span class="sxs-lookup"><span data-stu-id="8c4e0-157">Standard</span></span>
- <span data-ttu-id="8c4e0-158">Базового</span><span class="sxs-lookup"><span data-stu-id="8c4e0-158">Basic</span></span>

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

### <span data-ttu-id="8c4e0-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-159">-StorageProfile</span></span>
<span data-ttu-id="8c4e0-160">Указывает объект профиля хранилища, который содержит свойства диска для конфигурации VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="8c4e0-161">Для задания этого объекта можно использовать командлет **Set-AzureRmVmssStorageProfile** .</span><span class="sxs-lookup"><span data-stu-id="8c4e0-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="8c4e0-162">-Тег</span><span class="sxs-lookup"><span data-stu-id="8c4e0-162">-Tag</span></span>
<span data-ttu-id="8c4e0-163">Указывает теги, которые будут назначены для VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="8c4e0-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="8c4e0-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="8c4e0-165">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="8c4e0-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8c4e0-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c4e0-167">Автоматически</span><span class="sxs-lookup"><span data-stu-id="8c4e0-167">Automatic</span></span>
- <span data-ttu-id="8c4e0-168">Вручную</span><span class="sxs-lookup"><span data-stu-id="8c4e0-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e0-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c4e0-169">-Confirm</span></span>
<span data-ttu-id="8c4e0-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4e0-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4e0-171">-WhatIf</span></span>
<span data-ttu-id="8c4e0-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c4e0-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4e0-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4e0-174">CommonParameters</span></span>
<span data-ttu-id="8c4e0-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4e0-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4e0-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4e0-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c4e0-177">INPUTS</span></span>

### <span data-ttu-id="8c4e0-178">Ничего</span><span class="sxs-lookup"><span data-stu-id="8c4e0-178">None</span></span>
<span data-ttu-id="8c4e0-179">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c4e0-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c4e0-180">OUTPUTS</span></span>

### <span data-ttu-id="8c4e0-181">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8c4e0-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8c4e0-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c4e0-182">NOTES</span></span>

## <span data-ttu-id="8c4e0-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c4e0-183">RELATED LINKS</span></span>

[<span data-ttu-id="8c4e0-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="8c4e0-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e0-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="8c4e0-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c4e0-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="8c4e0-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8c4e0-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="8c4e0-188">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8c4e0-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


