---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563720"
---
# <span data-ttu-id="965b2-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="965b2-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="965b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="965b2-102">SYNOPSIS</span></span>
<span data-ttu-id="965b2-103">Добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="965b2-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="965b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="965b2-104">SYNTAX</span></span>

### <span data-ttu-id="965b2-105">GetNicFromNicId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="965b2-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="965b2-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="965b2-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="965b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="965b2-107">DESCRIPTION</span></span>
<span data-ttu-id="965b2-108">Командлет **Add-AzureRmVMNetworkInterface** добавляет сетевой интерфейс на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="965b2-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="965b2-109">Вы можете добавить интерфейс при создании виртуальной машины или добавлении ее на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="965b2-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="965b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="965b2-110">EXAMPLES</span></span>

### <span data-ttu-id="965b2-111">Пример 1: Добавление сетевого интерфейса для новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="965b2-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="965b2-112">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="965b2-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="965b2-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="965b2-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="965b2-114">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="965b2-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="965b2-115">Пример 2: Добавление сетевого интерфейса на существующую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="965b2-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="965b2-116">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="965b2-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="965b2-117">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="965b2-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="965b2-118">Вторая команда добавляет сетевой интерфейс к виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="965b2-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="965b2-119">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="965b2-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="965b2-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="965b2-120">PARAMETERS</span></span>

### <span data-ttu-id="965b2-121">-ID</span><span class="sxs-lookup"><span data-stu-id="965b2-121">-Id</span></span>
<span data-ttu-id="965b2-122">Указывает идентификатор сетевого интерфейса для добавления на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="965b2-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="965b2-123">Вы можете использовать командлет [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) для получения сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="965b2-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="965b2-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="965b2-124">-NetworkInterface</span></span>
<span data-ttu-id="965b2-125">Указывает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="965b2-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="965b2-126">-Primary</span><span class="sxs-lookup"><span data-stu-id="965b2-126">-Primary</span></span>
<span data-ttu-id="965b2-127">Указывает на то, что этот командлет добавляет сетевой интерфейс в качестве основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="965b2-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="965b2-128">-VM</span><span class="sxs-lookup"><span data-stu-id="965b2-128">-VM</span></span>
<span data-ttu-id="965b2-129">Указывает локальный объект виртуальной машины, к которому нужно добавить сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="965b2-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="965b2-130">Чтобы создать виртуальную машину, используйте командлет **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="965b2-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="965b2-131">Чтобы получить текущую виртуальную машину, используйте командлет **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="965b2-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="965b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965b2-132">CommonParameters</span></span>
<span data-ttu-id="965b2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="965b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965b2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="965b2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965b2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="965b2-135">INPUTS</span></span>

### <span data-ttu-id="965b2-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="965b2-136">None</span></span>
<span data-ttu-id="965b2-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="965b2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="965b2-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="965b2-138">OUTPUTS</span></span>

## <span data-ttu-id="965b2-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="965b2-139">NOTES</span></span>

## <span data-ttu-id="965b2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="965b2-140">RELATED LINKS</span></span>

[<span data-ttu-id="965b2-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="965b2-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="965b2-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="965b2-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="965b2-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="965b2-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
