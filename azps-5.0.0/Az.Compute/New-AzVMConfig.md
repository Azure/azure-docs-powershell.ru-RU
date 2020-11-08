---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248406"
---
# <span data-ttu-id="5fe87-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5fe87-101">New-AzVMConfig</span></span>

## <span data-ttu-id="5fe87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fe87-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe87-103">Создание настраиваемого объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="5fe87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fe87-104">SYNTAX</span></span>

### <span data-ttu-id="5fe87-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fe87-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe87-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fe87-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe87-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe87-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe87-108">Командлет **New-AzVMConfig** создает настраиваемый локальный объект виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe87-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="5fe87-109">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="5fe87-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="5fe87-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fe87-110">EXAMPLES</span></span>

### <span data-ttu-id="5fe87-111">Пример 1: создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5fe87-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="5fe87-112">Первая команда получает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fe87-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5fe87-113">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5fe87-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5fe87-114">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5fe87-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5fe87-115">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fe87-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="5fe87-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fe87-116">PARAMETERS</span></span>

### <span data-ttu-id="5fe87-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5fe87-117">-AvailabilitySetId</span></span>
<span data-ttu-id="5fe87-118">Указывает идентификатор группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5fe87-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="5fe87-119">Чтобы получить объект группы доступности, используйте командлет Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fe87-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="5fe87-120">Объект "набор доступности" имеет свойство ID.</span><span class="sxs-lookup"><span data-stu-id="5fe87-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="5fe87-121">Виртуальные машины, указанные в одной группе доступности, выделяются на разные узлы для максимизации доступности.</span><span class="sxs-lookup"><span data-stu-id="5fe87-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="5fe87-122">Дополнительные сведения о наборах доступности можно найти [в разделе Управление доступом виртуальных машин](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="5fe87-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="5fe87-123">Дополнительные сведения о запланированном обслуживании Azure можно найти [в разделе Планирование обслуживания виртуальных машин в Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="5fe87-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="5fe87-124">В настоящее время VM может быть добавлена в набор доступности только в момент создания.</span><span class="sxs-lookup"><span data-stu-id="5fe87-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="5fe87-125">Группа доступности, на которую добавляется виртуальная машина, должна находиться в той же группе ресурсов, что и ресурс "Настройка доступности".</span><span class="sxs-lookup"><span data-stu-id="5fe87-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="5fe87-126">Невозможно добавить существующую виртуальную машину в группу доступности.</span><span class="sxs-lookup"><span data-stu-id="5fe87-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="5fe87-127">Это свойство не может существовать вместе со свойствами, не являющимися null. ссылка virtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="5fe87-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="5fe87-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe87-128">-DefaultProfile</span></span>
<span data-ttu-id="5fe87-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe87-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe87-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5fe87-130">-EnableUltraSSD</span></span>
<span data-ttu-id="5fe87-131">Позволяет иметь возможность использовать один или несколько дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5fe87-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="5fe87-132">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="5fe87-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="5fe87-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5fe87-133">-EvictionPolicy</span></span>
<span data-ttu-id="5fe87-134">Политика вытеснения для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe87-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="5fe87-135">Поддерживаются значения "освободить" и "Удалить".</span><span class="sxs-lookup"><span data-stu-id="5fe87-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="5fe87-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="5fe87-136">-HostId</span></span>
<span data-ttu-id="5fe87-137">Идентификатор узла</span><span class="sxs-lookup"><span data-stu-id="5fe87-137">The Id of Host</span></span>

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

### <span data-ttu-id="5fe87-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5fe87-138">-IdentityId</span></span>
<span data-ttu-id="5fe87-139">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5fe87-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5fe87-140">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="5fe87-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5fe87-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5fe87-141">-IdentityType</span></span>
<span data-ttu-id="5fe87-142">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="5fe87-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="5fe87-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5fe87-143">-LicenseType</span></span>
<span data-ttu-id="5fe87-144">Тип лицензии, предназначенный для использования собственного сценария лицензирования.</span><span class="sxs-lookup"><span data-stu-id="5fe87-144">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5fe87-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5fe87-145">-MaxPrice</span></span>
<span data-ttu-id="5fe87-146">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="5fe87-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="5fe87-147">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="5fe87-147">This price is in US Dollars.</span></span> <span data-ttu-id="5fe87-148">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="5fe87-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="5fe87-149">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="5fe87-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="5fe87-150">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="5fe87-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="5fe87-151">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="5fe87-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="5fe87-152">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="5fe87-152">Example: 0.01538.</span></span>  <span data-ttu-id="5fe87-153">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="5fe87-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="5fe87-154">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="5fe87-154">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="5fe87-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="5fe87-155">-EncryptionAtHost</span></span>
<span data-ttu-id="5fe87-156">Свойство EncryptionAtHost может использоваться пользователем в запросе для включения или отключения шифрования узла для установленной виртуальной машины или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="5fe87-157">Это позволит включить шифрование для всех дисков, включая ресурс/временный диск на узле.</span><span class="sxs-lookup"><span data-stu-id="5fe87-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="5fe87-158">По умолчанию: шифрование на узле будет отключено, если это свойство не имеет значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="5fe87-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="5fe87-159">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="5fe87-159">-Priority</span></span>
<span data-ttu-id="5fe87-160">Приоритет виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="5fe87-161">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="5fe87-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5fe87-162">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5fe87-163">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5fe87-164">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="5fe87-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5fe87-165">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="5fe87-165">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="5fe87-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5fe87-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5fe87-167">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="5fe87-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="5fe87-168">-Теги</span><span class="sxs-lookup"><span data-stu-id="5fe87-168">-Tags</span></span>
<span data-ttu-id="5fe87-169">Теги, вложенные в ресурс.</span><span class="sxs-lookup"><span data-stu-id="5fe87-169">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="5fe87-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="5fe87-170">-VMName</span></span>
<span data-ttu-id="5fe87-171">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-171">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="5fe87-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5fe87-172">-VMSize</span></span>
<span data-ttu-id="5fe87-173">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="5fe87-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="5fe87-174">-VmssId</span></span>
<span data-ttu-id="5fe87-175">Идентификатор набора масштабов виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5fe87-175">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="5fe87-176">-Zone</span><span class="sxs-lookup"><span data-stu-id="5fe87-176">-Zone</span></span>
<span data-ttu-id="5fe87-177">Указывает список зон доступности для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fe87-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="5fe87-178">Допустимые значения зависят от возможностей региона.</span><span class="sxs-lookup"><span data-stu-id="5fe87-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="5fe87-179">Допустимые значения: 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="5fe87-179">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="5fe87-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe87-180">CommonParameters</span></span>
<span data-ttu-id="5fe87-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fe87-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe87-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fe87-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe87-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fe87-183">INPUTS</span></span>

### <span data-ttu-id="5fe87-184">System. String</span><span class="sxs-lookup"><span data-stu-id="5fe87-184">System.String</span></span>

### <span data-ttu-id="5fe87-185">System. String []</span><span class="sxs-lookup"><span data-stu-id="5fe87-185">System.String[]</span></span>

### <span data-ttu-id="5fe87-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5fe87-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5fe87-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5fe87-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fe87-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe87-188">OUTPUTS</span></span>

### <span data-ttu-id="5fe87-189">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5fe87-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5fe87-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fe87-190">NOTES</span></span>

## <span data-ttu-id="5fe87-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fe87-191">RELATED LINKS</span></span>

[<span data-ttu-id="5fe87-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5fe87-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="5fe87-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5fe87-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="5fe87-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5fe87-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="5fe87-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5fe87-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


