---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
ms.openlocfilehash: 77e4de344e3dd89eac09b1ebefb6ba49071dcbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915401"
---
# <span data-ttu-id="84278-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="84278-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="84278-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84278-102">SYNOPSIS</span></span>
<span data-ttu-id="84278-103">Получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="84278-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84278-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84278-104">SYNTAX</span></span>

### <span data-ttu-id="84278-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84278-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84278-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="84278-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84278-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="84278-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84278-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84278-108">DESCRIPTION</span></span>
<span data-ttu-id="84278-109">Командлет **Get-AzureRmVMSize** получает доступ к размерам виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="84278-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="84278-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84278-110">EXAMPLES</span></span>

### <span data-ttu-id="84278-111">Пример 1: получение размеров виртуальных машин для местоположения</span><span class="sxs-lookup"><span data-stu-id="84278-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="84278-112">Эта команда получает доступные размеры для виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="84278-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="84278-113">Пример 2: получение размеров для группы доступности</span><span class="sxs-lookup"><span data-stu-id="84278-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="84278-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="84278-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="84278-115">Пример 3: получение размеров для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="84278-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="84278-116">Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="84278-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="84278-117">Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.</span><span class="sxs-lookup"><span data-stu-id="84278-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="84278-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84278-118">PARAMETERS</span></span>

### <span data-ttu-id="84278-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="84278-119">-AvailabilitySetName</span></span>
<span data-ttu-id="84278-120">Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="84278-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="84278-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84278-121">-DefaultProfile</span></span>
<span data-ttu-id="84278-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84278-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84278-123">-Location</span><span class="sxs-lookup"><span data-stu-id="84278-123">-Location</span></span>
<span data-ttu-id="84278-124">Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="84278-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="84278-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84278-125">-ResourceGroupName</span></span>
<span data-ttu-id="84278-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="84278-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="84278-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="84278-127">-VMName</span></span>
<span data-ttu-id="84278-128">Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="84278-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="84278-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84278-129">CommonParameters</span></span>
<span data-ttu-id="84278-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84278-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84278-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84278-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84278-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84278-132">INPUTS</span></span>

### <span data-ttu-id="84278-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="84278-133">None</span></span>
<span data-ttu-id="84278-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="84278-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84278-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84278-135">OUTPUTS</span></span>

### <span data-ttu-id="84278-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="84278-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="84278-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="84278-137">NOTES</span></span>

## <span data-ttu-id="84278-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84278-138">RELATED LINKS</span></span>

[<span data-ttu-id="84278-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="84278-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


