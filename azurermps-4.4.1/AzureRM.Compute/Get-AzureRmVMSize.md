---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 33abc50f4cc336230e1c6f4ef14d12f51b22af83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570456"
---
# <span data-ttu-id="8d772-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="8d772-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="8d772-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d772-102">SYNOPSIS</span></span>
<span data-ttu-id="8d772-103">Получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8d772-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d772-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d772-104">SYNTAX</span></span>

### <span data-ttu-id="8d772-105">ListVirtualMachineSizeParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d772-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d772-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8d772-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d772-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d772-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d772-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d772-108">DESCRIPTION</span></span>
<span data-ttu-id="8d772-109">Командлет **Get-AzureRmVMSize** получает доступ к размерам виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8d772-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="8d772-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d772-110">EXAMPLES</span></span>

### <span data-ttu-id="8d772-111">Пример 1: получение размеров виртуальных машин для местоположения</span><span class="sxs-lookup"><span data-stu-id="8d772-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="8d772-112">Эта команда получает доступные размеры для виртуальных машин в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="8d772-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="8d772-113">Пример 2: получение размеров для группы доступности</span><span class="sxs-lookup"><span data-stu-id="8d772-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="8d772-114">Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="8d772-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="8d772-115">Пример 3: получение размеров для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8d772-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="8d772-116">Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="8d772-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="8d772-117">Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.</span><span class="sxs-lookup"><span data-stu-id="8d772-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="8d772-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d772-118">PARAMETERS</span></span>

### <span data-ttu-id="8d772-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="8d772-119">-AvailabilitySetName</span></span>
<span data-ttu-id="8d772-120">Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8d772-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="8d772-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d772-121">-DefaultProfile</span></span>
<span data-ttu-id="8d772-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d772-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d772-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8d772-123">-Location</span></span>
<span data-ttu-id="8d772-124">Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8d772-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="8d772-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d772-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d772-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d772-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8d772-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d772-127">-VMName</span></span>
<span data-ttu-id="8d772-128">Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="8d772-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="8d772-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d772-129">CommonParameters</span></span>
<span data-ttu-id="8d772-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d772-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d772-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d772-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d772-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d772-132">INPUTS</span></span>

## <span data-ttu-id="8d772-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d772-133">OUTPUTS</span></span>

## <span data-ttu-id="8d772-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d772-134">NOTES</span></span>

## <span data-ttu-id="8d772-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d772-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d772-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d772-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


