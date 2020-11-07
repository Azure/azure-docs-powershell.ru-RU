---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: a7e84ee56e09e2008d76ccd9177d320be7ada96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733169"
---
# <span data-ttu-id="23f17-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="23f17-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="23f17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23f17-102">SYNOPSIS</span></span>
<span data-ttu-id="23f17-103">Добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="23f17-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23f17-104">SYNTAX</span></span>

### <span data-ttu-id="23f17-105">GetNicFromNicId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23f17-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23f17-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="23f17-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f17-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f17-107">DESCRIPTION</span></span>
<span data-ttu-id="23f17-108">Командлет **Add-AzureRmVMNetworkInterface** добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="23f17-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="23f17-109">Вы можете добавить интерфейс при создании виртуальной машины или добавлении ее на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="23f17-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="23f17-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23f17-110">EXAMPLES</span></span>

### <span data-ttu-id="23f17-111">Пример 1: Добавление сетевого интерфейса для новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="23f17-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="23f17-112">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23f17-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="23f17-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="23f17-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="23f17-114">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23f17-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="23f17-115">Пример 2: Добавление сетевого интерфейса на существующую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="23f17-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="23f17-116">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="23f17-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="23f17-117">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23f17-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="23f17-118">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23f17-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="23f17-119">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="23f17-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="23f17-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23f17-120">PARAMETERS</span></span>

### <span data-ttu-id="23f17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f17-121">-DefaultProfile</span></span>
<span data-ttu-id="23f17-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23f17-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f17-123">-ID</span><span class="sxs-lookup"><span data-stu-id="23f17-123">-Id</span></span>
<span data-ttu-id="23f17-124">Указывает идентификатор сетевого интерфейса для добавления на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="23f17-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="23f17-125">Вы можете использовать командлет [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) для получения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="23f17-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="23f17-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="23f17-126">-NetworkInterface</span></span>
<span data-ttu-id="23f17-127">Указывает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="23f17-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="23f17-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="23f17-128">-Primary</span></span>
<span data-ttu-id="23f17-129">Указывает на то, что этот командлет добавляет сетевой интерфейс в качестве основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="23f17-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="23f17-130">-VM</span><span class="sxs-lookup"><span data-stu-id="23f17-130">-VM</span></span>
<span data-ttu-id="23f17-131">Указывает локальный объект виртуальной машины, к которому нужно добавить сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="23f17-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="23f17-132">Чтобы создать виртуальную машину, используйте командлет **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="23f17-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="23f17-133">Чтобы получить текущую виртуальную машину, используйте командлет **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="23f17-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="23f17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f17-134">CommonParameters</span></span>
<span data-ttu-id="23f17-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23f17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f17-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f17-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f17-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23f17-137">INPUTS</span></span>

### <span data-ttu-id="23f17-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="23f17-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="23f17-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23f17-139">System.String</span></span>

### <span data-ttu-id="23f17-140">System. Collections. Generic. List "1 [[Microsoft. Azure. Management. internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. System. Common. Network, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="23f17-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="23f17-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23f17-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23f17-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f17-142">OUTPUTS</span></span>

### <span data-ttu-id="23f17-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="23f17-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="23f17-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="23f17-144">NOTES</span></span>

## <span data-ttu-id="23f17-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23f17-145">RELATED LINKS</span></span>

[<span data-ttu-id="23f17-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="23f17-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="23f17-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="23f17-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="23f17-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="23f17-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
