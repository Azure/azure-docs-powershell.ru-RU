---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405812"
---
# <span data-ttu-id="c26f7-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c26f7-101">New-AzVMConfig</span></span>

## <span data-ttu-id="c26f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c26f7-103">Создает настраиваемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="c26f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c26f7-104">SYNTAX</span></span>

### <span data-ttu-id="c26f7-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c26f7-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c26f7-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c26f7-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26f7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26f7-107">DESCRIPTION</span></span>
<span data-ttu-id="c26f7-108">С **его использованием** создается настраиваемый объект локальной виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="c26f7-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="c26f7-109">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="c26f7-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="c26f7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c26f7-110">EXAMPLES</span></span>

### <span data-ttu-id="c26f7-111">Пример 1. Создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="c26f7-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="c26f7-112">Первая команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="c26f7-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="c26f7-113">Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="c26f7-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c26f7-114">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c26f7-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c26f7-115">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c26f7-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="c26f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c26f7-116">PARAMETERS</span></span>

### <span data-ttu-id="c26f7-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="c26f7-117">-AvailabilitySetId</span></span>
<span data-ttu-id="c26f7-118">Определяет ИД набора доступности.</span><span class="sxs-lookup"><span data-stu-id="c26f7-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="c26f7-119">Чтобы получить объект набора доступности, воспользуйтесь Get-AzAvailabilitySet управления.</span><span class="sxs-lookup"><span data-stu-id="c26f7-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="c26f7-120">Объект набора доступности содержит свойство "ИД".</span><span class="sxs-lookup"><span data-stu-id="c26f7-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="c26f7-121">Для максимального повышения доступности виртуальные машины, указанные в том же наборе доступности, выделены для разных узлов.</span><span class="sxs-lookup"><span data-stu-id="c26f7-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="c26f7-122">Дополнительные сведения о наборах доступности см. в документе ["Управление доступностью виртуальных машин".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="c26f7-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="c26f7-123">Дополнительные сведения о запланированном техническом обслуживании Azure см. в сведениях о запланированном техническом обслуживании [виртуальных машин в Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="c26f7-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="c26f7-124">В настоящее время VM можно добавить только в набор доступности во время создания.</span><span class="sxs-lookup"><span data-stu-id="c26f7-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="c26f7-125">Набор доступности, в который добавляется проектный проект, должен быть в той же группе ресурсов, что и для ресурса, настроенного для доступности.</span><span class="sxs-lookup"><span data-stu-id="c26f7-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="c26f7-126">Существующий VM-клиент невозможно добавить в набор доступности.</span><span class="sxs-lookup"><span data-stu-id="c26f7-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="c26f7-127">Это свойство не может существовать вместе со ссылкой на non-null.virtualMascaleeScaleSet.</span><span class="sxs-lookup"><span data-stu-id="c26f7-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26f7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26f7-128">-DefaultProfile</span></span>
<span data-ttu-id="c26f7-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c26f7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26f7-130">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="c26f7-130">-EnableUltraSSD</span></span>
<span data-ttu-id="c26f7-131">Позволяет использовать один или несколько управляемых дисков данных с учетной записью UltraSSD_LRS типа учетной записи хранения на VM.</span><span class="sxs-lookup"><span data-stu-id="c26f7-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="c26f7-132">Управляемые диски с типом учетной UltraSSD_LRS можно добавить на виртуальную машину, только если это свойство включено.</span><span class="sxs-lookup"><span data-stu-id="c26f7-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="c26f7-133">-ВехионПолиция</span><span class="sxs-lookup"><span data-stu-id="c26f7-133">-EvictionPolicy</span></span>
<span data-ttu-id="c26f7-134">Политика присоединения к виртуальной машине Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="c26f7-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="c26f7-135">Поддерживаются значения Deallocate и Delete.</span><span class="sxs-lookup"><span data-stu-id="c26f7-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="c26f7-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="c26f7-136">-HostId</span></span>
<span data-ttu-id="c26f7-137">ИД хоста</span><span class="sxs-lookup"><span data-stu-id="c26f7-137">The Id of Host</span></span>

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

### <span data-ttu-id="c26f7-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c26f7-138">-IdentityId</span></span>
<span data-ttu-id="c26f7-139">Определяет список удостоверений пользователей, связанных с набором масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c26f7-140">Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="c26f7-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="c26f7-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c26f7-141">-IdentityType</span></span>
<span data-ttu-id="c26f7-142">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="c26f7-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26f7-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c26f7-143">-LicenseType</span></span>
<span data-ttu-id="c26f7-144">Тип лицензии, который указывает на то, что изображение или диск для виртуальной машины были лицензированы локально.</span><span class="sxs-lookup"><span data-stu-id="c26f7-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="c26f7-145">Возможные значения для Windows Server:</span><span class="sxs-lookup"><span data-stu-id="c26f7-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="c26f7-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="c26f7-146">Windows_Client</span></span>
- <span data-ttu-id="c26f7-147">Windows_Server возможности операционной системы Linux Server:</span><span class="sxs-lookup"><span data-stu-id="c26f7-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="c26f7-148">RHEL_BYOS (для RHEL)</span><span class="sxs-lookup"><span data-stu-id="c26f7-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="c26f7-149">SLES_BYOS (для SUSE)</span><span class="sxs-lookup"><span data-stu-id="c26f7-149">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26f7-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="c26f7-150">-MaxPrice</span></span>
<span data-ttu-id="c26f7-151">Указывает максимальную цену, которую вы будете оплачивать для службы VM или VMSS с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c26f7-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="c26f7-152">Эта цена в долларах США.</span><span class="sxs-lookup"><span data-stu-id="c26f7-152">This price is in US Dollars.</span></span> <span data-ttu-id="c26f7-153">Эта цена будет сравниваться с текущей низкой ценой приоритета для размера VM.</span><span class="sxs-lookup"><span data-stu-id="c26f7-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="c26f7-154">Кроме того, цены сравниваются во время создания или обновления низкой приоритетной VM-или VMSS и операция будет работать только в том случае, если максимальная цена больше текущей цены с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c26f7-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="c26f7-155">Максимальное значение maxPrice также будет использоваться для создания обетовки VM или VMSS с низким приоритетом, если текущая цена с низким приоритетом выходит за пределы максимальной цены после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="c26f7-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="c26f7-156">Возможные значения: любое десятичее значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="c26f7-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="c26f7-157">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="c26f7-157">Example: 0.01538.</span></span>  <span data-ttu-id="c26f7-158">-1 указывает на то, что не следует захламлять VM или VMSS с низким приоритетом по ценам.</span><span class="sxs-lookup"><span data-stu-id="c26f7-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="c26f7-159">Кроме того, максимальная цена по умолчанию составляет -1, если она не предоставлена вами.</span><span class="sxs-lookup"><span data-stu-id="c26f7-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="c26f7-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c26f7-160">-EncryptionAtHost</span></span>
<span data-ttu-id="c26f7-161">Свойство EncryptionAtHost может использоваться пользователем в запросе для того, чтобы включить или отключить шифрование хоста для набора виртуальных машин или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="c26f7-162">Это позволит шифровать все диски, включая диск Resource/Temp на самом хосте.</span><span class="sxs-lookup"><span data-stu-id="c26f7-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="c26f7-163">По умолчанию: шифрование на хосте будет отключено, если для этого свойства не установлено значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="c26f7-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="c26f7-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="c26f7-164">-Priority</span></span>
<span data-ttu-id="c26f7-165">Приоритет виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="c26f7-166">Поддерживаются только такие значения, как "Обычный", "Spot" и "Низкий".</span><span class="sxs-lookup"><span data-stu-id="c26f7-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="c26f7-167">"Обычный" — для обычных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c26f7-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="c26f7-168">Spot — для spot virtual machine.</span><span class="sxs-lookup"><span data-stu-id="c26f7-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="c26f7-169">"Низкая" также для spot virtual machine, но заменяется spot.</span><span class="sxs-lookup"><span data-stu-id="c26f7-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="c26f7-170">Используйте "Spot" вместо "Низкий".</span><span class="sxs-lookup"><span data-stu-id="c26f7-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="c26f7-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c26f7-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="c26f7-172">ИД ресурса группы расположения близости, который можно использовать с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="c26f7-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="c26f7-173">-Теги</span><span class="sxs-lookup"><span data-stu-id="c26f7-173">-Tags</span></span>
<span data-ttu-id="c26f7-174">Теги, прикрепленные к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c26f7-174">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26f7-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="c26f7-175">-VMName</span></span>
<span data-ttu-id="c26f7-176">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-176">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26f7-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="c26f7-177">-VMSize</span></span>
<span data-ttu-id="c26f7-178">Определяет размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="c26f7-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="c26f7-179">-VmssId</span></span>
<span data-ttu-id="c26f7-180">The Id of virtual machine scale set</span><span class="sxs-lookup"><span data-stu-id="c26f7-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="c26f7-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="c26f7-181">-Zone</span></span>
<span data-ttu-id="c26f7-182">Определяет список зон доступности для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c26f7-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="c26f7-183">Допустимые значения зависят от возможностей региона.</span><span class="sxs-lookup"><span data-stu-id="c26f7-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="c26f7-184">Допустимые значения обычно составляет 1,2,3.</span><span class="sxs-lookup"><span data-stu-id="c26f7-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="c26f7-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26f7-185">CommonParameters</span></span>
<span data-ttu-id="c26f7-186">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26f7-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26f7-187">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c26f7-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26f7-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c26f7-188">INPUTS</span></span>

### <span data-ttu-id="c26f7-189">System.String</span><span class="sxs-lookup"><span data-stu-id="c26f7-189">System.String</span></span>

### <span data-ttu-id="c26f7-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c26f7-190">System.String[]</span></span>

### <span data-ttu-id="c26f7-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c26f7-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c26f7-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c26f7-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c26f7-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c26f7-193">OUTPUTS</span></span>

### <span data-ttu-id="c26f7-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="c26f7-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c26f7-195">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c26f7-195">NOTES</span></span>

## <span data-ttu-id="c26f7-196">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c26f7-196">RELATED LINKS</span></span>

[<span data-ttu-id="c26f7-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c26f7-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="c26f7-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c26f7-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="c26f7-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="c26f7-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="c26f7-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c26f7-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


