---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: b669d415e88c16f7ddfe532f05bc754561b7ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980952"
---
# <span data-ttu-id="1b043-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="1b043-101">Get-AzVMSize</span></span>

## <span data-ttu-id="1b043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b043-102">SYNOPSIS</span></span>
<span data-ttu-id="1b043-103">Доступен размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b043-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="1b043-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b043-104">SYNTAX</span></span>

### <span data-ttu-id="1b043-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b043-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b043-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1b043-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b043-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1b043-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b043-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b043-108">DESCRIPTION</span></span>
<span data-ttu-id="1b043-109">Доступен размер виртуальной машины **с cmdlet Get-AzVMSize.**</span><span class="sxs-lookup"><span data-stu-id="1b043-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="1b043-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b043-110">EXAMPLES</span></span>

### <span data-ttu-id="1b043-111">Пример 1. Получить размеры виртуальной машины для расположения</span><span class="sxs-lookup"><span data-stu-id="1b043-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="1b043-112">Эта команда получает доступные размеры виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="1b043-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="1b043-113">Пример 2. Настройка размеров для набора доступности</span><span class="sxs-lookup"><span data-stu-id="1b043-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="1b043-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в наборе доступности AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="1b043-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="1b043-115">Пример 3. Получить размеры для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1b043-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="1b043-116">Эта команда имеет доступные размеры для существующей виртуальной машины с именем VirtualMa в 12.</span><span class="sxs-lookup"><span data-stu-id="1b043-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="1b043-117">Вы можете размеры этой виртуальной машины данной команды.</span><span class="sxs-lookup"><span data-stu-id="1b043-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="1b043-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b043-118">PARAMETERS</span></span>

### <span data-ttu-id="1b043-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="1b043-119">-AvailabilitySetName</span></span>
<span data-ttu-id="1b043-120">Определяет имя набора доступности, для которого этот cmdlet получает доступ к доступным размерам виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b043-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="1b043-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b043-121">-DefaultProfile</span></span>
<span data-ttu-id="1b043-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b043-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b043-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1b043-123">-Location</span></span>
<span data-ttu-id="1b043-124">Определяет расположение, для которого этот cmdlet получает доступ к доступным размерам виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b043-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="1b043-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b043-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b043-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b043-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1b043-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b043-127">-VMName</span></span>
<span data-ttu-id="1b043-128">Указывает имя виртуальной машины, размеры виртуальной машины, размер которого можно получить этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="1b043-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="1b043-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b043-129">CommonParameters</span></span>
<span data-ttu-id="1b043-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b043-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b043-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b043-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b043-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b043-132">INPUTS</span></span>

### <span data-ttu-id="1b043-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1b043-133">System.String</span></span>

## <span data-ttu-id="1b043-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b043-134">OUTPUTS</span></span>

### <span data-ttu-id="1b043-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseSize</span><span class="sxs-lookup"><span data-stu-id="1b043-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="1b043-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b043-136">NOTES</span></span>

## <span data-ttu-id="1b043-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b043-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b043-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1b043-138">Get-AzVM</span></span>](./Get-AzVM.md)


