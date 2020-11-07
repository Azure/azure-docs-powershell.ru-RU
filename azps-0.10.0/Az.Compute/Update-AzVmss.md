---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911309"
---
# <span data-ttu-id="a155a-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-101">Update-AzVmss</span></span>

## <span data-ttu-id="a155a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a155a-102">SYNOPSIS</span></span>
<span data-ttu-id="a155a-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="a155a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a155a-104">SYNTAX</span></span>

### <span data-ttu-id="a155a-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a155a-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a155a-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a155a-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a155a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a155a-107">DESCRIPTION</span></span>
<span data-ttu-id="a155a-108">Командлет **Update-AzVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="a155a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a155a-109">EXAMPLES</span></span>

### <span data-ttu-id="a155a-110">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="a155a-111">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="a155a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a155a-112">PARAMETERS</span></span>

### <span data-ttu-id="a155a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a155a-113">-AsJob</span></span>
<span data-ttu-id="a155a-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a155a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a155a-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a155a-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="a155a-116">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="a155a-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="a155a-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="a155a-118">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a155a-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="a155a-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="a155a-120">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="a155a-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="a155a-121">-CustomData</span></span>
<span data-ttu-id="a155a-122">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="a155a-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="a155a-123">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a155a-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="a155a-124">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="a155a-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a155a-125">-DefaultProfile</span></span>
<span data-ttu-id="a155a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a155a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a155a-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="a155a-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="a155a-128">Указывает, что этот командлет отключает проверку пароля для ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="a155a-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="a155a-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="a155a-130">Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="a155a-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a155a-131">-IdentityId</span></span>
<span data-ttu-id="a155a-132">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a155a-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a155a-133">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="a155a-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a155a-134">-IdentityType</span></span>
<span data-ttu-id="a155a-135">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a155a-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="a155a-136">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="a155a-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="a155a-137">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a155a-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="a155a-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a155a-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a155a-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a155a-139">SystemAssigned</span></span>
- <span data-ttu-id="a155a-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="a155a-140">UserAssigned</span></span>
- <span data-ttu-id="a155a-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="a155a-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="a155a-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="a155a-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="a155a-143">-ImageReferenceId</span></span>
<span data-ttu-id="a155a-144">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="a155a-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="a155a-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="a155a-146">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="a155a-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="a155a-147">Чтобы получить предложение с изображением, используйте командлет Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="a155a-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="a155a-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="a155a-149">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="a155a-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a155a-150">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="a155a-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="a155a-151">-ImageReferenceSku</span></span>
<span data-ttu-id="a155a-152">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="a155a-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="a155a-153">Чтобы получить SKU, используйте командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="a155a-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="a155a-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="a155a-155">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="a155a-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="a155a-156">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="a155a-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="a155a-157">-ImageUri</span></span>
<span data-ttu-id="a155a-158">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="a155a-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="a155a-159">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="a155a-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a155a-160">-LicenseType</span></span>
<span data-ttu-id="a155a-161">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="a155a-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a155a-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="a155a-163">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="a155a-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="a155a-164">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a155a-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a155a-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="a155a-165">StandardLRS</span></span>
- <span data-ttu-id="a155a-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="a155a-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a155a-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="a155a-168">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="a155a-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="a155a-169">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="a155a-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="a155a-170">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="a155a-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a155a-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="a155a-172">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="a155a-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="a155a-173">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="a155a-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="a155a-174">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="a155a-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a155a-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="a155a-176">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a155a-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="a155a-177">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="a155a-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="a155a-178">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="a155a-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="a155a-179">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="a155a-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="a155a-180">-OsDiskCaching</span></span>
<span data-ttu-id="a155a-181">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a155a-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="a155a-182">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a155a-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a155a-183">Ничего</span><span class="sxs-lookup"><span data-stu-id="a155a-183">None</span></span>
- <span data-ttu-id="a155a-184">Чтения</span><span class="sxs-lookup"><span data-stu-id="a155a-184">ReadOnly</span></span>
- <span data-ttu-id="a155a-185">Операцию</span><span class="sxs-lookup"><span data-stu-id="a155a-185">ReadWrite</span></span>

<span data-ttu-id="a155a-186">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a155a-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="a155a-187">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a155a-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="a155a-188">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="a155a-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a155a-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a155a-190">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a155a-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-191">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="a155a-191">-Overprovision</span></span>
<span data-ttu-id="a155a-192">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="a155a-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="a155a-194">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="a155a-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="a155a-195">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="a155a-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="a155a-196">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="a155a-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a155a-197">-PlanName</span></span>
<span data-ttu-id="a155a-198">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="a155a-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="a155a-199">-PlanProduct</span></span>
<span data-ttu-id="a155a-200">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="a155a-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="a155a-201">-PlanPromotionCode</span></span>
<span data-ttu-id="a155a-202">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="a155a-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a155a-203">-PlanPublisher</span></span>
<span data-ttu-id="a155a-204">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="a155a-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="a155a-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="a155a-206">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a155a-207">-ResourceGroupName</span></span>
<span data-ttu-id="a155a-208">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a155a-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="a155a-210">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="a155a-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a155a-211">-SkuCapacity</span></span>
<span data-ttu-id="a155a-212">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a155a-213">-SkuName</span></span>
<span data-ttu-id="a155a-214">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a155a-215">-SkuTier</span></span>
<span data-ttu-id="a155a-216">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="a155a-217">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a155a-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a155a-218">Стандартная</span><span class="sxs-lookup"><span data-stu-id="a155a-218">Standard</span></span>
- <span data-ttu-id="a155a-219">Базового</span><span class="sxs-lookup"><span data-stu-id="a155a-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-220">-Тег</span><span class="sxs-lookup"><span data-stu-id="a155a-220">-Tag</span></span>
<span data-ttu-id="a155a-221">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a155a-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a155a-222">Например:</span><span class="sxs-lookup"><span data-stu-id="a155a-222">For example:</span></span>

<span data-ttu-id="a155a-223">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a155a-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-224">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="a155a-224">-TimeZone</span></span>
<span data-ttu-id="a155a-225">Задает часовой пояс для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="a155a-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a155a-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="a155a-227">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="a155a-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="a155a-228">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a155a-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a155a-229">Автоматически</span><span class="sxs-lookup"><span data-stu-id="a155a-229">Automatic</span></span>
- <span data-ttu-id="a155a-230">Вручную</span><span class="sxs-lookup"><span data-stu-id="a155a-230">Manual</span></span>
- <span data-ttu-id="a155a-231">За</span><span class="sxs-lookup"><span data-stu-id="a155a-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="a155a-232">-VhdContainer</span></span>
<span data-ttu-id="a155a-233">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a155a-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a155a-235">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="a155a-236">Чтобы получить объект VMSS, используйте командлет Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a155a-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="a155a-237">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="a155a-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a155a-238">-VMScaleSetName</span></span>
<span data-ttu-id="a155a-239">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a155a-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-240">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a155a-240">-Confirm</span></span>
<span data-ttu-id="a155a-241">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a155a-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a155a-242">-WhatIf</span></span>
<span data-ttu-id="a155a-243">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a155a-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a155a-244">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a155a-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155a-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a155a-245">CommonParameters</span></span>
<span data-ttu-id="a155a-246">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a155a-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a155a-247">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a155a-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a155a-248">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a155a-248">INPUTS</span></span>

### <span data-ttu-id="a155a-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a155a-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a155a-250">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a155a-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a155a-251">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a155a-251">OUTPUTS</span></span>

### <span data-ttu-id="a155a-252">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a155a-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a155a-253">Пуск</span><span class="sxs-lookup"><span data-stu-id="a155a-253">NOTES</span></span>

## <span data-ttu-id="a155a-254">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a155a-254">RELATED LINKS</span></span>

[<span data-ttu-id="a155a-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a155a-256">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="a155a-257">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a155a-258">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a155a-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a155a-260">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a155a-261">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a155a-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


