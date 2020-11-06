---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563640"
---
# <span data-ttu-id="3c6f2-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c6f2-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="3c6f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6f2-103">Удаляет конфигурацию сетевого интерфейса из VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c6f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c6f2-104">SYNTAX</span></span>

### <span data-ttu-id="3c6f2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c6f2-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6f2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c6f2-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c6f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="3c6f2-108">Командлет **Remove-AzureRmVmssNetworkInterfaceConfiguration** удаляет конфигурацию сетевого интерфейса из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3c6f2-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3c6f2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c6f2-109">EXAMPLES</span></span>

### <span data-ttu-id="3c6f2-110">Пример 1: Удаление конфигурации интерфейса</span><span class="sxs-lookup"><span data-stu-id="3c6f2-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="3c6f2-111">Первая команда получает объект VMSS с помощью командлета Get-AzureRmVmss и сохраняет его в переменной $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="3c6f2-112">Вторая команда удаляет конфигурацию сетевого интерфейса с именем ContosoVmssInterface02 из комплекта в $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="3c6f2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c6f2-113">PARAMETERS</span></span>

### <span data-ttu-id="3c6f2-114">-ID</span><span class="sxs-lookup"><span data-stu-id="3c6f2-114">-Id</span></span>
<span data-ttu-id="3c6f2-115">Указывает идентификатор конфигурации сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6f2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c6f2-116">-Name</span></span>
<span data-ttu-id="3c6f2-117">Указывает имя конфигурации сетевого интерфейса, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6f2-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3c6f2-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3c6f2-119">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6f2-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c6f2-120">-Confirm</span></span>
<span data-ttu-id="3c6f2-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c6f2-122">-WhatIf</span></span>
<span data-ttu-id="3c6f2-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c6f2-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6f2-125">CommonParameters</span></span>
<span data-ttu-id="3c6f2-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6f2-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c6f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6f2-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c6f2-128">INPUTS</span></span>

### <span data-ttu-id="3c6f2-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c6f2-129">None</span></span>
<span data-ttu-id="3c6f2-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3c6f2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c6f2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c6f2-131">OUTPUTS</span></span>

## <span data-ttu-id="3c6f2-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c6f2-132">NOTES</span></span>

## <span data-ttu-id="3c6f2-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c6f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c6f2-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c6f2-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="3c6f2-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c6f2-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


