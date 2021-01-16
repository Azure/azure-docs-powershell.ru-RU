---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509257"
---
# <span data-ttu-id="8c53e-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8c53e-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="8c53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c53e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c53e-103">Добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8c53e-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="8c53e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c53e-104">SYNTAX</span></span>

### <span data-ttu-id="8c53e-105">GetNicFromNicId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c53e-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c53e-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="8c53e-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c53e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c53e-107">DESCRIPTION</span></span>
<span data-ttu-id="8c53e-108">Командлет **Add-AzVMNetworkInterface** добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8c53e-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="8c53e-109">Вы можете добавить интерфейс при создании виртуальной машины или его добавлении в существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8c53e-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="8c53e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c53e-110">EXAMPLES</span></span>

### <span data-ttu-id="8c53e-111">Пример 1. Добавление сетевого интерфейса на новую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="8c53e-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="8c53e-112">Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="8c53e-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8c53e-113">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8c53e-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8c53e-114">Вторая команда добавляет сетевой интерфейс к виртуальной машине, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8c53e-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="8c53e-115">Пример 2. Добавление сетевого интерфейса к существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="8c53e-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="8c53e-116">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью **командлета Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="8c53e-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="8c53e-117">Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8c53e-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8c53e-118">Вторая команда добавляет сетевой интерфейс к виртуальной машине, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8c53e-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8c53e-119">Последняя команда обновляет состояние виртуальной машины, которая хранится в $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8c53e-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="8c53e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c53e-120">PARAMETERS</span></span>

### <span data-ttu-id="8c53e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c53e-121">-DefaultProfile</span></span>
<span data-ttu-id="8c53e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c53e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c53e-123">-Id</span><span class="sxs-lookup"><span data-stu-id="8c53e-123">-Id</span></span>
<span data-ttu-id="8c53e-124">Определяет ИД сетевого интерфейса, который нужно добавить на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8c53e-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="8c53e-125">Для получения сетевого интерфейса можно использовать командлет [Get-AzNetworkInterface.](/powershell/module/az.network/get-aznetworkinterface)</span><span class="sxs-lookup"><span data-stu-id="8c53e-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c53e-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8c53e-126">-NetworkInterface</span></span>
<span data-ttu-id="8c53e-127">Определяет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8c53e-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="8c53e-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="8c53e-128">-Primary</span></span>
<span data-ttu-id="8c53e-129">Указывает на то, что этот cmdlet добавляет сетевой интерфейс в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="8c53e-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c53e-130">-VM</span><span class="sxs-lookup"><span data-stu-id="8c53e-130">-VM</span></span>
<span data-ttu-id="8c53e-131">Определяет объект локальной виртуальной машины, к которому нужно добавить сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8c53e-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="8c53e-132">Чтобы создать виртуальную машину, воспользуйтесь **cmdlet New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="8c53e-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="8c53e-133">Чтобы получить виртуальную машину, воспользуйтесь **cmdlet get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="8c53e-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c53e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c53e-134">CommonParameters</span></span>
<span data-ttu-id="8c53e-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c53e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c53e-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c53e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c53e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c53e-137">INPUTS</span></span>

### <span data-ttu-id="8c53e-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="8c53e-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8c53e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8c53e-139">System.String</span></span>

### <span data-ttu-id="8c53e-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8c53e-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8c53e-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c53e-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c53e-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c53e-142">OUTPUTS</span></span>

### <span data-ttu-id="8c53e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="8c53e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8c53e-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c53e-144">NOTES</span></span>

## <span data-ttu-id="8c53e-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c53e-145">RELATED LINKS</span></span>

[<span data-ttu-id="8c53e-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8c53e-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="8c53e-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8c53e-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8c53e-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8c53e-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
