---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065914"
---
# <span data-ttu-id="7ca08-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7ca08-101">New-AzVMConfig</span></span>

## <span data-ttu-id="7ca08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ca08-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca08-103">Создание настраиваемого объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="7ca08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ca08-104">SYNTAX</span></span>

### <span data-ttu-id="7ca08-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ca08-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ca08-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca08-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ca08-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca08-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ca08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ca08-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca08-109">Командлет **New-AzVMConfig** создает настраиваемый локальный объект виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca08-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="7ca08-110">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="7ca08-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="7ca08-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ca08-111">EXAMPLES</span></span>

### <span data-ttu-id="7ca08-112">Пример 1: создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7ca08-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="7ca08-113">Первая команда получает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7ca08-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="7ca08-114">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7ca08-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7ca08-115">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7ca08-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7ca08-116">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7ca08-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="7ca08-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ca08-117">PARAMETERS</span></span>

### <span data-ttu-id="7ca08-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7ca08-118">-AssignIdentity</span></span>
<span data-ttu-id="7ca08-119">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="7ca08-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7ca08-120">-AvailabilitySetId</span></span>
<span data-ttu-id="7ca08-121">Указывает идентификатор группы доступности.</span><span class="sxs-lookup"><span data-stu-id="7ca08-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="7ca08-122">Чтобы получить объект группы доступности, используйте командлет Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7ca08-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="7ca08-123">Объект "набор доступности" имеет свойство ID.</span><span class="sxs-lookup"><span data-stu-id="7ca08-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="7ca08-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca08-124">-DefaultProfile</span></span>
<span data-ttu-id="7ca08-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca08-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca08-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7ca08-126">-EnableUltraSSD</span></span>
<span data-ttu-id="7ca08-127">Позволяет иметь возможность использовать один или несколько дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7ca08-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="7ca08-128">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="7ca08-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="7ca08-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ca08-129">-EvictionPolicy</span></span>
<span data-ttu-id="7ca08-130">Политика вытеснения для виртуальной машины с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="7ca08-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="7ca08-131">Только поддерживаемое значение — "освободить".</span><span class="sxs-lookup"><span data-stu-id="7ca08-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="7ca08-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="7ca08-132">-HostId</span></span>
<span data-ttu-id="7ca08-133">Идентификатор узла</span><span class="sxs-lookup"><span data-stu-id="7ca08-133">The Id of Host</span></span>

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

### <span data-ttu-id="7ca08-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7ca08-134">-IdentityId</span></span>
<span data-ttu-id="7ca08-135">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7ca08-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7ca08-136">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="7ca08-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7ca08-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7ca08-137">-IdentityType</span></span>
<span data-ttu-id="7ca08-138">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="7ca08-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="7ca08-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7ca08-139">-LicenseType</span></span>
<span data-ttu-id="7ca08-140">Тип лицензии, предназначенный для использования собственного сценария лицензирования.</span><span class="sxs-lookup"><span data-stu-id="7ca08-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="7ca08-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7ca08-141">-MaxPrice</span></span>
<span data-ttu-id="7ca08-142">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ca08-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7ca08-143">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="7ca08-143">This price is in US Dollars.</span></span> <span data-ttu-id="7ca08-144">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="7ca08-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7ca08-145">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="7ca08-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7ca08-146">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ca08-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7ca08-147">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="7ca08-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7ca08-148">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="7ca08-148">Example: 0.01538.</span></span>  <span data-ttu-id="7ca08-149">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="7ca08-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7ca08-150">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="7ca08-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="7ca08-151">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="7ca08-151">-Priority</span></span>
<span data-ttu-id="7ca08-152">Приоритет виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="7ca08-153">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="7ca08-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="7ca08-154">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="7ca08-155">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="7ca08-156">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="7ca08-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="7ca08-157">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="7ca08-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="7ca08-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7ca08-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7ca08-159">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="7ca08-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="7ca08-160">-Теги</span><span class="sxs-lookup"><span data-stu-id="7ca08-160">-Tags</span></span>
<span data-ttu-id="7ca08-161">Теги, вложенные в ресурс.</span><span class="sxs-lookup"><span data-stu-id="7ca08-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="7ca08-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="7ca08-162">-VMName</span></span>
<span data-ttu-id="7ca08-163">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="7ca08-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="7ca08-164">-VMSize</span></span>
<span data-ttu-id="7ca08-165">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="7ca08-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="7ca08-166">-VmssId</span></span>
<span data-ttu-id="7ca08-167">Идентификатор набора масштабов виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7ca08-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="7ca08-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="7ca08-168">-Zone</span></span>
<span data-ttu-id="7ca08-169">Указывает список зон доступности для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ca08-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="7ca08-170">Допустимые значения зависят от возможностей региона.</span><span class="sxs-lookup"><span data-stu-id="7ca08-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="7ca08-171">Допустимые значения: 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="7ca08-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="7ca08-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca08-172">CommonParameters</span></span>
<span data-ttu-id="7ca08-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ca08-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca08-174">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ca08-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca08-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ca08-175">INPUTS</span></span>

### <span data-ttu-id="7ca08-176">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca08-176">System.String</span></span>

### <span data-ttu-id="7ca08-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="7ca08-177">System.String[]</span></span>

### <span data-ttu-id="7ca08-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ca08-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ca08-179">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ca08-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ca08-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ca08-180">OUTPUTS</span></span>

### <span data-ttu-id="7ca08-181">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7ca08-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7ca08-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ca08-182">NOTES</span></span>

## <span data-ttu-id="7ca08-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ca08-183">RELATED LINKS</span></span>

[<span data-ttu-id="7ca08-184">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ca08-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="7ca08-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7ca08-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7ca08-186">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7ca08-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="7ca08-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7ca08-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


