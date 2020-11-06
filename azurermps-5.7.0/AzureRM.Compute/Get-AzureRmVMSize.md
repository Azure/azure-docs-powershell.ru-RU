---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565565"
---
# <span data-ttu-id="b7f22-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="b7f22-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="b7f22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7f22-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f22-103">Получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b7f22-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7f22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7f22-104">SYNTAX</span></span>

### <span data-ttu-id="b7f22-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7f22-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="b7f22-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b7f22-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="b7f22-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b7f22-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="b7f22-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f22-108">DESCRIPTION</span></span>
<span data-ttu-id="b7f22-109">Командлет **Get-AzureRmVMSize** получает доступ к размерам виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b7f22-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="b7f22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7f22-110">EXAMPLES</span></span>

### <span data-ttu-id="b7f22-111">Пример 1: получение размеров виртуальных машин для местоположения</span><span class="sxs-lookup"><span data-stu-id="b7f22-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="b7f22-112">Эта команда получает доступные размеры для виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="b7f22-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="b7f22-113">Пример 2: получение размеров для группы доступности</span><span class="sxs-lookup"><span data-stu-id="b7f22-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="b7f22-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="b7f22-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="b7f22-115">Пример 3: получение размеров для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="b7f22-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="b7f22-116">Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="b7f22-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="b7f22-117">Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.</span><span class="sxs-lookup"><span data-stu-id="b7f22-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="b7f22-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7f22-118">PARAMETERS</span></span>

### <span data-ttu-id="b7f22-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b7f22-119">-AvailabilitySetName</span></span>
<span data-ttu-id="b7f22-120">Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b7f22-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="b7f22-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b7f22-121">-Location</span></span>
<span data-ttu-id="b7f22-122">Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b7f22-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="b7f22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f22-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7f22-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7f22-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b7f22-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b7f22-125">-VMName</span></span>
<span data-ttu-id="b7f22-126">Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="b7f22-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="b7f22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f22-127">CommonParameters</span></span>
<span data-ttu-id="b7f22-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7f22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f22-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f22-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f22-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7f22-130">INPUTS</span></span>

### <span data-ttu-id="b7f22-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7f22-131">None</span></span>
<span data-ttu-id="b7f22-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b7f22-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7f22-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f22-133">OUTPUTS</span></span>

## <span data-ttu-id="b7f22-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7f22-134">NOTES</span></span>

## <span data-ttu-id="b7f22-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7f22-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7f22-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7f22-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


