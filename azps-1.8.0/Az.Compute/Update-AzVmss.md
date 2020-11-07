---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731194"
---
# <span data-ttu-id="89345-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-101">Update-AzVmss</span></span>

## <span data-ttu-id="89345-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89345-102">SYNOPSIS</span></span>
<span data-ttu-id="89345-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="89345-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89345-104">SYNTAX</span></span>

### <span data-ttu-id="89345-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89345-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89345-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="89345-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89345-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89345-107">DESCRIPTION</span></span>
<span data-ttu-id="89345-108">Командлет **Update-AzVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="89345-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89345-109">EXAMPLES</span></span>

### <span data-ttu-id="89345-110">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="89345-111">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="89345-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89345-112">PARAMETERS</span></span>

### <span data-ttu-id="89345-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89345-113">-AsJob</span></span>
<span data-ttu-id="89345-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89345-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="89345-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="89345-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="89345-116">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="89345-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="89345-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="89345-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="89345-118">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="89345-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="89345-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="89345-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="89345-120">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="89345-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="89345-121">-CustomData</span></span>
<span data-ttu-id="89345-122">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="89345-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="89345-123">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="89345-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="89345-124">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="89345-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89345-125">-DefaultProfile</span></span>
<span data-ttu-id="89345-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89345-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89345-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="89345-127">-DisableAutoRollback</span></span>
<span data-ttu-id="89345-128">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="89345-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="89345-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="89345-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="89345-130">Указывает, что этот командлет отключает проверку пароля для ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="89345-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="89345-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="89345-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="89345-132">Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="89345-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="89345-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="89345-133">-IdentityId</span></span>
<span data-ttu-id="89345-134">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="89345-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="89345-135">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="89345-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="89345-136">-IdentityType</span></span>
<span data-ttu-id="89345-137">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89345-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="89345-138">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="89345-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="89345-139">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89345-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="89345-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="89345-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89345-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="89345-141">SystemAssigned</span></span>
- <span data-ttu-id="89345-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="89345-142">UserAssigned</span></span>
- <span data-ttu-id="89345-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="89345-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="89345-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="89345-144">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="89345-145">-ImageReferenceId</span></span>
<span data-ttu-id="89345-146">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="89345-146">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="89345-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="89345-148">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="89345-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="89345-149">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="89345-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="89345-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="89345-151">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="89345-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="89345-152">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="89345-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="89345-153">-ImageReferenceSku</span></span>
<span data-ttu-id="89345-154">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="89345-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="89345-155">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="89345-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="89345-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="89345-157">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="89345-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="89345-158">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="89345-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="89345-159">-ImageUri</span></span>
<span data-ttu-id="89345-160">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="89345-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="89345-161">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="89345-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="89345-162">-LicenseType</span></span>
<span data-ttu-id="89345-163">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="89345-163">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="89345-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="89345-165">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="89345-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="89345-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="89345-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89345-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="89345-167">StandardLRS</span></span>
- <span data-ttu-id="89345-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="89345-168">PremiumLRS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="89345-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="89345-170">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="89345-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="89345-171">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="89345-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="89345-172">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="89345-172">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="89345-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="89345-174">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="89345-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="89345-175">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="89345-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="89345-176">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="89345-176">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="89345-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="89345-178">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="89345-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="89345-179">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="89345-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="89345-180">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="89345-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="89345-181">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="89345-181">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="89345-182">-OsDiskCaching</span></span>
<span data-ttu-id="89345-183">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="89345-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="89345-184">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="89345-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89345-185">Ничего</span><span class="sxs-lookup"><span data-stu-id="89345-185">None</span></span>
- <span data-ttu-id="89345-186">Чтения</span><span class="sxs-lookup"><span data-stu-id="89345-186">ReadOnly</span></span>
- <span data-ttu-id="89345-187">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="89345-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="89345-188">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="89345-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="89345-189">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="89345-189">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="89345-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="89345-191">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="89345-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="89345-192">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="89345-192">-Overprovision</span></span>
<span data-ttu-id="89345-193">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="89345-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="89345-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="89345-195">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="89345-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="89345-196">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="89345-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="89345-197">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="89345-197">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="89345-198">-PlanName</span></span>
<span data-ttu-id="89345-199">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="89345-199">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="89345-200">-PlanProduct</span></span>
<span data-ttu-id="89345-201">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="89345-201">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="89345-202">-PlanPromotionCode</span></span>
<span data-ttu-id="89345-203">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="89345-203">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="89345-204">-PlanPublisher</span></span>
<span data-ttu-id="89345-205">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="89345-205">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="89345-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="89345-207">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="89345-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89345-208">-ResourceGroupName</span></span>
<span data-ttu-id="89345-209">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89345-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="89345-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="89345-211">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="89345-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="89345-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="89345-212">-SkuCapacity</span></span>
<span data-ttu-id="89345-213">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-213">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="89345-214">-SkuName</span></span>
<span data-ttu-id="89345-215">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-215">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="89345-216">-SkuTier</span></span>
<span data-ttu-id="89345-217">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="89345-218">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="89345-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89345-219">Стандартная</span><span class="sxs-lookup"><span data-stu-id="89345-219">Standard</span></span>
- <span data-ttu-id="89345-220">Базового</span><span class="sxs-lookup"><span data-stu-id="89345-220">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-221">-Тег</span><span class="sxs-lookup"><span data-stu-id="89345-221">-Tag</span></span>
<span data-ttu-id="89345-222">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="89345-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="89345-223">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="89345-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-224">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="89345-224">-TimeZone</span></span>
<span data-ttu-id="89345-225">Задает часовой пояс для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="89345-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="89345-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="89345-227">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="89345-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="89345-228">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="89345-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89345-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="89345-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="89345-230">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="89345-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="89345-231">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="89345-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89345-232">Автоматически</span><span class="sxs-lookup"><span data-stu-id="89345-232">Automatic</span></span>
- <span data-ttu-id="89345-233">Вручную</span><span class="sxs-lookup"><span data-stu-id="89345-233">Manual</span></span>
- <span data-ttu-id="89345-234">За</span><span class="sxs-lookup"><span data-stu-id="89345-234">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="89345-235">-VhdContainer</span></span>
<span data-ttu-id="89345-236">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89345-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="89345-238">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="89345-239">Чтобы получить объект VMSS, используйте командлет Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="89345-239">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="89345-240">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="89345-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89345-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89345-241">-VMScaleSetName</span></span>
<span data-ttu-id="89345-242">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="89345-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89345-243">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89345-243">-Confirm</span></span>
<span data-ttu-id="89345-244">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89345-244">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89345-245">-WhatIf</span></span>
<span data-ttu-id="89345-246">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89345-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89345-247">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89345-247">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89345-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89345-248">CommonParameters</span></span>
<span data-ttu-id="89345-249">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89345-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89345-250">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89345-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89345-251">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89345-251">INPUTS</span></span>

### <span data-ttu-id="89345-252">System. String</span><span class="sxs-lookup"><span data-stu-id="89345-252">System.String</span></span>

### <span data-ttu-id="89345-253">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89345-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="89345-254">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89345-254">System.Boolean</span></span>

## <span data-ttu-id="89345-255">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89345-255">OUTPUTS</span></span>

### <span data-ttu-id="89345-256">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89345-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="89345-257">Пуск</span><span class="sxs-lookup"><span data-stu-id="89345-257">NOTES</span></span>

## <span data-ttu-id="89345-258">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89345-258">RELATED LINKS</span></span>

[<span data-ttu-id="89345-259">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-259">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="89345-260">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-260">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="89345-261">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-261">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="89345-262">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-262">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="89345-263">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-263">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="89345-264">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-264">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="89345-265">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89345-265">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


