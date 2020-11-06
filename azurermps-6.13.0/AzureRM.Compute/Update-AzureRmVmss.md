---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566529"
---
# <span data-ttu-id="5d1dd-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="5d1dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d1dd-103">Обновляет состояние VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d1dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d1dd-104">SYNTAX</span></span>

### <span data-ttu-id="5d1dd-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d1dd-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1dd-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d1dd-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d1dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d1dd-107">DESCRIPTION</span></span>
<span data-ttu-id="5d1dd-108">Командлет **Update-AzureRmVmss** обновляет состояние набора масштабов виртуальных машин (VMSS) в состояние ЛОКАЛЬНОГО объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="5d1dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d1dd-109">EXAMPLES</span></span>

### <span data-ttu-id="5d1dd-110">Пример 1: обновление состояния VMSS до состояния локального объекта VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="5d1dd-111">Эта команда обновляет состояние VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001, в состояние локального объекта VMSS $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="5d1dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d1dd-112">PARAMETERS</span></span>

### <span data-ttu-id="5d1dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d1dd-113">-AsJob</span></span>
<span data-ttu-id="5d1dd-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5d1dd-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5d1dd-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="5d1dd-116">Определяет, должны ли обновления ОС автоматически применяться к экземплярам наборов масштабируемых элементов в более поздних версиях, когда становится доступно более новая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="5d1dd-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="5d1dd-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="5d1dd-118">Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5d1dd-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="5d1dd-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="5d1dd-120">Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="5d1dd-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="5d1dd-121">-CustomData</span></span>
<span data-ttu-id="5d1dd-122">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="5d1dd-123">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="5d1dd-124">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="5d1dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d1dd-125">-DefaultProfile</span></span>
<span data-ttu-id="5d1dd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d1dd-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="5d1dd-127">-DisableAutoRollback</span></span>
<span data-ttu-id="5d1dd-128">Отключение автоматического отката для политики автоматического обновления ОС</span><span class="sxs-lookup"><span data-stu-id="5d1dd-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="5d1dd-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="5d1dd-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="5d1dd-130">Указывает, что этот командлет отключает проверку пароля для ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="5d1dd-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="5d1dd-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="5d1dd-132">Указывает, включены ли на виртуальных машинах Windows в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="5d1dd-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5d1dd-133">-IdentityId</span></span>
<span data-ttu-id="5d1dd-134">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5d1dd-135">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="5d1dd-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5d1dd-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5d1dd-136">-IdentityType</span></span>
<span data-ttu-id="5d1dd-137">Указывает тип удостоверения, используемого для набора шкал виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="5d1dd-138">Тип "SystemAssignedUserAssigned" включает в себя и неявное созданное удостоверение, и набор идентификаторов, назначенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="5d1dd-139">Тип "нет" приведет к удалению всех удостоверений из установленной шкалы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="5d1dd-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5d1dd-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1dd-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5d1dd-141">SystemAssigned</span></span>
- <span data-ttu-id="5d1dd-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="5d1dd-142">UserAssigned</span></span>
- <span data-ttu-id="5d1dd-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="5d1dd-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="5d1dd-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d1dd-144">None</span></span>

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

### <span data-ttu-id="5d1dd-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="5d1dd-145">-ImageReferenceId</span></span>
<span data-ttu-id="5d1dd-146">Указывает идентификатор ссылки на изображение.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="5d1dd-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="5d1dd-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="5d1dd-148">Указывает тип предложения для образа виртуальной машины (VMImage).</span><span class="sxs-lookup"><span data-stu-id="5d1dd-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="5d1dd-149">Чтобы получить предложение с изображением, используйте командлет Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="5d1dd-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="5d1dd-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="5d1dd-151">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5d1dd-152">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5d1dd-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="5d1dd-153">-ImageReferenceSku</span></span>
<span data-ttu-id="5d1dd-154">Указывает SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="5d1dd-155">Чтобы получить SKU, используйте командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="5d1dd-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="5d1dd-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="5d1dd-157">Указывает версию VMImage.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="5d1dd-158">Чтобы использовать последнюю версию, укажите значение, которое не определено в последней версии.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="5d1dd-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="5d1dd-159">-ImageUri</span></span>
<span data-ttu-id="5d1dd-160">Указывает URI большого двоичного объекта для пользовательского изображения.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="5d1dd-161">VMSS создает диск операционной системы в том же контейнере пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="5d1dd-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d1dd-162">-LicenseType</span></span>
<span data-ttu-id="5d1dd-163">Укажите тип лицензии, чтобы присвоить себе собственный сценарий лицензирования.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5d1dd-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5d1dd-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="5d1dd-165">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="5d1dd-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5d1dd-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1dd-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="5d1dd-167">StandardLRS</span></span>
- <span data-ttu-id="5d1dd-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="5d1dd-168">PremiumLRS</span></span>

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

### <span data-ttu-id="5d1dd-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5d1dd-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="5d1dd-170">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="5d1dd-171">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="5d1dd-172">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5d1dd-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5d1dd-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="5d1dd-174">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="5d1dd-175">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="5d1dd-176">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5d1dd-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="5d1dd-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="5d1dd-178">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="5d1dd-179">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="5d1dd-180">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="5d1dd-181">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="5d1dd-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="5d1dd-182">-OsDiskCaching</span></span>
<span data-ttu-id="5d1dd-183">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="5d1dd-184">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5d1dd-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1dd-185">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d1dd-185">None</span></span>
- <span data-ttu-id="5d1dd-186">Чтения</span><span class="sxs-lookup"><span data-stu-id="5d1dd-186">ReadOnly</span></span>
- <span data-ttu-id="5d1dd-187">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="5d1dd-188">Если вы измените значение кэширования, командлет перезагрузит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="5d1dd-189">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="5d1dd-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="5d1dd-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="5d1dd-191">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="5d1dd-192">-Превышена подготовка</span><span class="sxs-lookup"><span data-stu-id="5d1dd-192">-Overprovision</span></span>
<span data-ttu-id="5d1dd-193">Указывает, переопределяет ли командлет переVMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="5d1dd-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="5d1dd-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="5d1dd-195">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="5d1dd-196">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="5d1dd-197">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="5d1dd-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="5d1dd-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5d1dd-198">-PlanName</span></span>
<span data-ttu-id="5d1dd-199">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="5d1dd-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5d1dd-200">-PlanProduct</span></span>
<span data-ttu-id="5d1dd-201">Указывает продукт плана.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="5d1dd-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5d1dd-202">-PlanPromotionCode</span></span>
<span data-ttu-id="5d1dd-203">Указывает код продвижения плана.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="5d1dd-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5d1dd-204">-PlanPublisher</span></span>
<span data-ttu-id="5d1dd-205">Указывает издателя плана.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="5d1dd-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="5d1dd-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="5d1dd-207">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах Windows в VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="5d1dd-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d1dd-208">-ResourceGroupName</span></span>
<span data-ttu-id="5d1dd-209">Указывает имя группы ресурсов, к которой принадлежит VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1dd-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5d1dd-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="5d1dd-211">Указывает одну группу размещения.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="5d1dd-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5d1dd-212">-SkuCapacity</span></span>
<span data-ttu-id="5d1dd-213">Задает количество экземпляров в VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="5d1dd-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5d1dd-214">-SkuName</span></span>
<span data-ttu-id="5d1dd-215">Задает размер всех экземпляров VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="5d1dd-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5d1dd-216">-SkuTier</span></span>
<span data-ttu-id="5d1dd-217">Указывает уровень VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="5d1dd-218">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5d1dd-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1dd-219">Стандартная</span><span class="sxs-lookup"><span data-stu-id="5d1dd-219">Standard</span></span>
- <span data-ttu-id="5d1dd-220">Базового</span><span class="sxs-lookup"><span data-stu-id="5d1dd-220">Basic</span></span>

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

### <span data-ttu-id="5d1dd-221">-Тег</span><span class="sxs-lookup"><span data-stu-id="5d1dd-221">-Tag</span></span>
<span data-ttu-id="5d1dd-222">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d1dd-223">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5d1dd-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5d1dd-224">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="5d1dd-224">-TimeZone</span></span>
<span data-ttu-id="5d1dd-225">Задает часовой пояс для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="5d1dd-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="5d1dd-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="5d1dd-227">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="5d1dd-228">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять в VMSS только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="5d1dd-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5d1dd-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="5d1dd-230">Заданный режим перехода на виртуальные машины в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="5d1dd-231">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5d1dd-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1dd-232">Автоматически</span><span class="sxs-lookup"><span data-stu-id="5d1dd-232">Automatic</span></span>
- <span data-ttu-id="5d1dd-233">Вручную</span><span class="sxs-lookup"><span data-stu-id="5d1dd-233">Manual</span></span>
- <span data-ttu-id="5d1dd-234">За</span><span class="sxs-lookup"><span data-stu-id="5d1dd-234">Rolling</span></span>

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

### <span data-ttu-id="5d1dd-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="5d1dd-235">-VhdContainer</span></span>
<span data-ttu-id="5d1dd-236">Указывает URL-адреса контейнеров, которые используются для хранения дисков операционной системы для VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="5d1dd-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d1dd-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5d1dd-238">Указывает локальный объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="5d1dd-239">Чтобы получить объект VMSS, используйте командлет Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="5d1dd-240">Этот объект виртуальной машины включает обновленное состояние для VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1dd-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5d1dd-241">-VMScaleSetName</span></span>
<span data-ttu-id="5d1dd-242">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1dd-243">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d1dd-243">-Confirm</span></span>
<span data-ttu-id="5d1dd-244">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d1dd-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d1dd-245">-WhatIf</span></span>
<span data-ttu-id="5d1dd-246">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d1dd-247">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d1dd-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1dd-248">CommonParameters</span></span>
<span data-ttu-id="5d1dd-249">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d1dd-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1dd-250">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d1dd-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1dd-251">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d1dd-251">INPUTS</span></span>

### <span data-ttu-id="5d1dd-252">System. String</span><span class="sxs-lookup"><span data-stu-id="5d1dd-252">System.String</span></span>

### <span data-ttu-id="5d1dd-253">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d1dd-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="5d1dd-254">Параметры: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d1dd-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="5d1dd-255">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d1dd-255">OUTPUTS</span></span>

### <span data-ttu-id="5d1dd-256">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d1dd-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5d1dd-257">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d1dd-257">NOTES</span></span>

## <span data-ttu-id="5d1dd-258">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d1dd-258">RELATED LINKS</span></span>

[<span data-ttu-id="5d1dd-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-260">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-262">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-264">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="5d1dd-265">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d1dd-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


