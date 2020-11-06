---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563643"
---
# <span data-ttu-id="24612-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24612-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="24612-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24612-102">SYNOPSIS</span></span>
<span data-ttu-id="24612-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="24612-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24612-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24612-104">SYNTAX</span></span>

### <span data-ttu-id="24612-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24612-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24612-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24612-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24612-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24612-107">DESCRIPTION</span></span>
<span data-ttu-id="24612-108">Командлет **Remove-AzureRmVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="24612-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="24612-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24612-109">EXAMPLES</span></span>

## <span data-ttu-id="24612-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24612-110">PARAMETERS</span></span>

### <span data-ttu-id="24612-111">-ID</span><span class="sxs-lookup"><span data-stu-id="24612-111">-Id</span></span>
<span data-ttu-id="24612-112">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="24612-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="24612-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24612-113">-Name</span></span>
<span data-ttu-id="24612-114">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="24612-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="24612-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24612-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="24612-116">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="24612-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="24612-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24612-117">-Confirm</span></span>
<span data-ttu-id="24612-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24612-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24612-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24612-119">-WhatIf</span></span>
<span data-ttu-id="24612-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24612-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24612-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24612-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24612-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24612-122">CommonParameters</span></span>
<span data-ttu-id="24612-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24612-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24612-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24612-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24612-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24612-125">INPUTS</span></span>

### <span data-ttu-id="24612-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="24612-126">None</span></span>
<span data-ttu-id="24612-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="24612-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24612-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24612-128">OUTPUTS</span></span>

### <span data-ttu-id="24612-129">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="24612-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="24612-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="24612-130">NOTES</span></span>

## <span data-ttu-id="24612-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24612-131">RELATED LINKS</span></span>

[<span data-ttu-id="24612-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24612-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
