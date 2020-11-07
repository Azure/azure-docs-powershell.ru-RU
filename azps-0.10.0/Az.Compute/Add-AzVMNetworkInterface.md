---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911599"
---
# <span data-ttu-id="f4441-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f4441-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="f4441-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4441-102">SYNOPSIS</span></span>
<span data-ttu-id="f4441-103">Добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f4441-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="f4441-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4441-104">SYNTAX</span></span>

### <span data-ttu-id="f4441-105">GetNicFromNicId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4441-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4441-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="f4441-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4441-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4441-107">DESCRIPTION</span></span>
<span data-ttu-id="f4441-108">Командлет **Add-AzVMNetworkInterface** добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f4441-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="f4441-109">Вы можете добавить интерфейс при создании виртуальной машины или добавлении ее на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f4441-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="f4441-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4441-110">EXAMPLES</span></span>

### <span data-ttu-id="f4441-111">Пример 1: Добавление сетевого интерфейса для новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f4441-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="f4441-112">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f4441-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f4441-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f4441-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="f4441-114">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f4441-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="f4441-115">Пример 2: Добавление сетевого интерфейса на существующую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="f4441-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="f4441-116">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="f4441-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="f4441-117">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f4441-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f4441-118">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f4441-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="f4441-119">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4441-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="f4441-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4441-120">PARAMETERS</span></span>

### <span data-ttu-id="f4441-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4441-121">-DefaultProfile</span></span>
<span data-ttu-id="f4441-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4441-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4441-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f4441-123">-Id</span></span>
<span data-ttu-id="f4441-124">Указывает идентификатор сетевого интерфейса для добавления на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f4441-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="f4441-125">Вы можете использовать командлет [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) для получения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f4441-125">You can use the [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4441-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f4441-126">-NetworkInterface</span></span>
<span data-ttu-id="f4441-127">Указывает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f4441-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4441-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="f4441-128">-Primary</span></span>
<span data-ttu-id="f4441-129">Указывает на то, что этот командлет добавляет сетевой интерфейс в качестве основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f4441-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4441-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f4441-130">-VM</span></span>
<span data-ttu-id="f4441-131">Указывает локальный объект виртуальной машины, к которому нужно добавить сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f4441-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="f4441-132">Чтобы создать виртуальную машину, используйте командлет **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="f4441-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="f4441-133">Чтобы получить текущую виртуальную машину, используйте командлет **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="f4441-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4441-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4441-134">CommonParameters</span></span>
<span data-ttu-id="f4441-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4441-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4441-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4441-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4441-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4441-137">INPUTS</span></span>

### <span data-ttu-id="f4441-138">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Networking. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="f4441-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="f4441-139">Параметр "NetworkInterface" принимает значение типа "System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Networking. Models. PSNetworkInterface]" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4441-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="f4441-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f4441-140">PSVirtualMachine</span></span>
<span data-ttu-id="f4441-141">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4441-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="f4441-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4441-142">OUTPUTS</span></span>

### <span data-ttu-id="f4441-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f4441-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f4441-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4441-144">NOTES</span></span>

## <span data-ttu-id="f4441-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4441-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4441-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f4441-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="f4441-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f4441-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f4441-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4441-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
