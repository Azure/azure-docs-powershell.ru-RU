---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 46a0ffcaece93328447405f78af2af0785b329c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911506"
---
# <span data-ttu-id="e60de-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="e60de-101">Get-AzVMSize</span></span>

## <span data-ttu-id="e60de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e60de-102">SYNOPSIS</span></span>
<span data-ttu-id="e60de-103">Получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e60de-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="e60de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e60de-104">SYNTAX</span></span>

### <span data-ttu-id="e60de-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e60de-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e60de-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e60de-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e60de-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e60de-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e60de-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e60de-108">DESCRIPTION</span></span>
<span data-ttu-id="e60de-109">Командлет **Get-AzVMSize** получает доступ к размерам виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e60de-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="e60de-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e60de-110">EXAMPLES</span></span>

### <span data-ttu-id="e60de-111">Пример 1: получение размеров виртуальных машин для местоположения</span><span class="sxs-lookup"><span data-stu-id="e60de-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="e60de-112">Эта команда получает доступные размеры для виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="e60de-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="e60de-113">Пример 2: получение размеров для группы доступности</span><span class="sxs-lookup"><span data-stu-id="e60de-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="e60de-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="e60de-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="e60de-115">Пример 3: получение размеров для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e60de-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="e60de-116">Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="e60de-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="e60de-117">Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.</span><span class="sxs-lookup"><span data-stu-id="e60de-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="e60de-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e60de-118">PARAMETERS</span></span>

### <span data-ttu-id="e60de-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="e60de-119">-AvailabilitySetName</span></span>
<span data-ttu-id="e60de-120">Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e60de-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60de-121">-DefaultProfile</span></span>
<span data-ttu-id="e60de-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e60de-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60de-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e60de-123">-Location</span></span>
<span data-ttu-id="e60de-124">Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e60de-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e60de-125">-ResourceGroupName</span></span>
<span data-ttu-id="e60de-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e60de-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60de-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="e60de-127">-VMName</span></span>
<span data-ttu-id="e60de-128">Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="e60de-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60de-129">CommonParameters</span></span>
<span data-ttu-id="e60de-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e60de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60de-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60de-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60de-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e60de-132">INPUTS</span></span>

### <span data-ttu-id="e60de-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="e60de-133">None</span></span>
<span data-ttu-id="e60de-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e60de-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e60de-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e60de-135">OUTPUTS</span></span>

### <span data-ttu-id="e60de-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="e60de-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="e60de-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e60de-137">NOTES</span></span>

## <span data-ttu-id="e60de-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e60de-138">RELATED LINKS</span></span>

[<span data-ttu-id="e60de-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e60de-139">Get-AzVM</span></span>](./Get-AzVM.md)


