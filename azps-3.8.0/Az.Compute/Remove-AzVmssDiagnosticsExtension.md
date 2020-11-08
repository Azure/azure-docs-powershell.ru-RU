---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073658"
---
# <span data-ttu-id="9d901-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="9d901-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d901-102">SYNOPSIS</span></span>
<span data-ttu-id="9d901-103">Удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d901-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="9d901-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d901-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d901-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d901-105">DESCRIPTION</span></span>
<span data-ttu-id="9d901-106">Командлет **Remove-AzVmssDiagnosticsExtension** удаляет расширение диагностики из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9d901-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9d901-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d901-107">EXAMPLES</span></span>

### <span data-ttu-id="9d901-108">Пример 1: удаление расширения диагностики из VMSS</span><span class="sxs-lookup"><span data-stu-id="9d901-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="9d901-109">Эта команда удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d901-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="9d901-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d901-110">PARAMETERS</span></span>

### <span data-ttu-id="9d901-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d901-111">-DefaultProfile</span></span>
<span data-ttu-id="9d901-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d901-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d901-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d901-113">-Name</span></span>
<span data-ttu-id="9d901-114">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d901-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d901-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9d901-116">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="9d901-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d901-117">-Confirm</span></span>
<span data-ttu-id="9d901-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d901-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d901-119">-WhatIf</span></span>
<span data-ttu-id="9d901-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d901-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d901-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d901-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d901-122">CommonParameters</span></span>
<span data-ttu-id="9d901-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d901-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d901-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d901-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d901-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d901-125">INPUTS</span></span>

### <span data-ttu-id="9d901-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d901-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9d901-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9d901-127">System.String</span></span>

## <span data-ttu-id="9d901-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d901-128">OUTPUTS</span></span>

### <span data-ttu-id="9d901-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d901-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9d901-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d901-130">NOTES</span></span>

## <span data-ttu-id="9d901-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d901-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d901-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="9d901-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9d901-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


