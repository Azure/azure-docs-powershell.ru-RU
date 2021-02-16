---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233348"
---
# <span data-ttu-id="a5dd8-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="a5dd8-101">Get-AzVMSize</span></span>

## <span data-ttu-id="a5dd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="a5dd8-103">Доступен размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="a5dd8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5dd8-104">SYNTAX</span></span>

### <span data-ttu-id="a5dd8-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5dd8-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5dd8-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a5dd8-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5dd8-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a5dd8-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5dd8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="a5dd8-109">Доступен размер виртуальной машины **с cmdlet Get-AzVMSize.**</span><span class="sxs-lookup"><span data-stu-id="a5dd8-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="a5dd8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="a5dd8-111">Пример 1. Получить размеры виртуальной машины для расположения</span><span class="sxs-lookup"><span data-stu-id="a5dd8-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="a5dd8-112">Эта команда получает доступные размеры виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="a5dd8-113">Пример 2. Получить размеры для набора доступности</span><span class="sxs-lookup"><span data-stu-id="a5dd8-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="a5dd8-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в наборе доступности AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="a5dd8-115">Пример 3. Получить размеры для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a5dd8-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="a5dd8-116">Эта команда имеет доступные размеры для существующей виртуальной машины с именем VirtualMa в 12.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="a5dd8-117">Вы можете размеры этой виртуальной машины данной команды.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="a5dd8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5dd8-118">PARAMETERS</span></span>

### <span data-ttu-id="a5dd8-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="a5dd8-119">-AvailabilitySetName</span></span>
<span data-ttu-id="a5dd8-120">Определяет имя набора доступности, для которого этот cmdlet получает доступ к доступным размерам виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="a5dd8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5dd8-121">-DefaultProfile</span></span>
<span data-ttu-id="a5dd8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5dd8-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a5dd8-123">-Location</span></span>
<span data-ttu-id="a5dd8-124">Определяет расположение, для которого этот cmdlet получает доступ к доступным размерам виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="a5dd8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5dd8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5dd8-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a5dd8-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="a5dd8-127">-VMName</span></span>
<span data-ttu-id="a5dd8-128">Указывает имя виртуальной машины, размеры виртуальной машины, размер которого можно получить этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="a5dd8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5dd8-129">CommonParameters</span></span>
<span data-ttu-id="a5dd8-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5dd8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5dd8-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5dd8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5dd8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5dd8-132">INPUTS</span></span>

### <span data-ttu-id="a5dd8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a5dd8-133">System.String</span></span>

## <span data-ttu-id="a5dd8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5dd8-134">OUTPUTS</span></span>

### <span data-ttu-id="a5dd8-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseSize</span><span class="sxs-lookup"><span data-stu-id="a5dd8-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="a5dd8-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5dd8-136">NOTES</span></span>

## <span data-ttu-id="a5dd8-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5dd8-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5dd8-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5dd8-138">Get-AzVM</span></span>](./Get-AzVM.md)


