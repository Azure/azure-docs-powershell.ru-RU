---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519504"
---
# <span data-ttu-id="5c302-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c302-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="5c302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c302-102">SYNOPSIS</span></span>
<span data-ttu-id="5c302-103">Удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c302-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="5c302-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c302-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c302-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c302-105">DESCRIPTION</span></span>
<span data-ttu-id="5c302-106">С **помощью cmdlet Remove-AzVmssDiagnosticsExtension** можно удалить расширение диагностики из набора масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5c302-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5c302-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c302-107">EXAMPLES</span></span>

### <span data-ttu-id="5c302-108">Пример 1. Удаление расширения диагностики из VMSS</span><span class="sxs-lookup"><span data-stu-id="5c302-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="5c302-109">Эта команда удаляет расширение диагностики из VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c302-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="5c302-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c302-110">PARAMETERS</span></span>

### <span data-ttu-id="5c302-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c302-111">-DefaultProfile</span></span>
<span data-ttu-id="5c302-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c302-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c302-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5c302-113">-Name</span></span>
<span data-ttu-id="5c302-114">Указывает имя расширения, которое этот cmdlet удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c302-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="5c302-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c302-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c302-116">Определяет VMSS, из которых нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="5c302-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="5c302-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c302-117">-Confirm</span></span>
<span data-ttu-id="5c302-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c302-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c302-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c302-119">-WhatIf</span></span>
<span data-ttu-id="5c302-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c302-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c302-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c302-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c302-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c302-122">CommonParameters</span></span>
<span data-ttu-id="5c302-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c302-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c302-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c302-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c302-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c302-125">INPUTS</span></span>

### <span data-ttu-id="5c302-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c302-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5c302-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c302-127">System.String</span></span>

## <span data-ttu-id="5c302-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c302-128">OUTPUTS</span></span>

### <span data-ttu-id="5c302-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c302-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5c302-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c302-130">NOTES</span></span>

## <span data-ttu-id="5c302-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c302-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c302-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c302-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="5c302-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5c302-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5c302-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5c302-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


