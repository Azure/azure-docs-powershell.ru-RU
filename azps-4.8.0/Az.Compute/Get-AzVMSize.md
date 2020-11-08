---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078416"
---
# <span data-ttu-id="d4102-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="d4102-101">Get-AzVMSize</span></span>

## <span data-ttu-id="d4102-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4102-102">SYNOPSIS</span></span>
<span data-ttu-id="d4102-103">Получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4102-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="d4102-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4102-104">SYNTAX</span></span>

### <span data-ttu-id="d4102-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4102-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4102-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4102-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4102-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d4102-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4102-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4102-108">DESCRIPTION</span></span>
<span data-ttu-id="d4102-109">Командлет **Get-AzVMSize** получает доступ к размерам виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4102-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="d4102-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4102-110">EXAMPLES</span></span>

### <span data-ttu-id="d4102-111">Пример 1: получение размеров виртуальных машин для местоположения</span><span class="sxs-lookup"><span data-stu-id="d4102-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="d4102-112">Эта команда получает доступные размеры для виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="d4102-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="d4102-113">Пример 2: получение размеров для группы доступности</span><span class="sxs-lookup"><span data-stu-id="d4102-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="d4102-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="d4102-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="d4102-115">Пример 3: получение размеров для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d4102-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="d4102-116">Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="d4102-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="d4102-117">Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.</span><span class="sxs-lookup"><span data-stu-id="d4102-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="d4102-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4102-118">PARAMETERS</span></span>

### <span data-ttu-id="d4102-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d4102-119">-AvailabilitySetName</span></span>
<span data-ttu-id="d4102-120">Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4102-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4102-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4102-121">-DefaultProfile</span></span>
<span data-ttu-id="d4102-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4102-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4102-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d4102-123">-Location</span></span>
<span data-ttu-id="d4102-124">Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4102-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4102-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4102-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4102-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4102-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4102-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4102-127">-VMName</span></span>
<span data-ttu-id="d4102-128">Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="d4102-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4102-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4102-129">CommonParameters</span></span>
<span data-ttu-id="d4102-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4102-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4102-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4102-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4102-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4102-132">INPUTS</span></span>

### <span data-ttu-id="d4102-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4102-133">System.String</span></span>

## <span data-ttu-id="d4102-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4102-134">OUTPUTS</span></span>

### <span data-ttu-id="d4102-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="d4102-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="d4102-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4102-136">NOTES</span></span>

## <span data-ttu-id="d4102-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4102-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4102-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4102-138">Get-AzVM</span></span>](./Get-AzVM.md)


