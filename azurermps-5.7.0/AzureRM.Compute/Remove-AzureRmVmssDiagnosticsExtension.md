---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563739"
---
# <span data-ttu-id="8dc20-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8dc20-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="8dc20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dc20-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc20-103">Удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dc20-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dc20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dc20-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc20-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc20-106">Командлет **Remove-AzureRmVmssDiagnosticsExtension** удаляет расширение диагностики из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8dc20-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8dc20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dc20-107">EXAMPLES</span></span>

### <span data-ttu-id="8dc20-108">Пример 1: удаление расширения диагностики из VMSS</span><span class="sxs-lookup"><span data-stu-id="8dc20-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="8dc20-109">Эта команда удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dc20-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="8dc20-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc20-110">PARAMETERS</span></span>

### <span data-ttu-id="8dc20-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dc20-111">-Name</span></span>
<span data-ttu-id="8dc20-112">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="8dc20-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc20-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8dc20-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8dc20-114">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="8dc20-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="8dc20-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc20-115">-Confirm</span></span>
<span data-ttu-id="8dc20-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc20-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc20-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc20-117">-WhatIf</span></span>
<span data-ttu-id="8dc20-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc20-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8dc20-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dc20-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc20-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc20-120">CommonParameters</span></span>
<span data-ttu-id="8dc20-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dc20-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc20-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc20-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc20-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dc20-123">INPUTS</span></span>

### <span data-ttu-id="8dc20-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="8dc20-124">None</span></span>
<span data-ttu-id="8dc20-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8dc20-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dc20-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc20-126">OUTPUTS</span></span>

###  
<span data-ttu-id="8dc20-127">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8dc20-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8dc20-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dc20-128">NOTES</span></span>

## <span data-ttu-id="8dc20-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc20-129">RELATED LINKS</span></span>

[<span data-ttu-id="8dc20-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8dc20-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="8dc20-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8dc20-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="8dc20-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8dc20-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


