---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519502"
---
# <span data-ttu-id="51f45-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="51f45-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="51f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f45-102">SYNOPSIS</span></span>
<span data-ttu-id="51f45-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="51f45-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="51f45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="51f45-104">SYNTAX</span></span>

### <span data-ttu-id="51f45-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51f45-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f45-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51f45-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f45-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51f45-107">DESCRIPTION</span></span>
<span data-ttu-id="51f45-108">Для **удаления расширения из** набора виртуальных машин (VMSS) удаляется расширение.</span><span class="sxs-lookup"><span data-stu-id="51f45-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="51f45-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="51f45-109">EXAMPLES</span></span>

### <span data-ttu-id="51f45-110">Пример 1. Удаление расширения VMSS</span><span class="sxs-lookup"><span data-stu-id="51f45-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="51f45-111">Эта команда удаляет расширение VMSS и обновляет их после изменения.</span><span class="sxs-lookup"><span data-stu-id="51f45-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="51f45-112">Пример 2. Удаление экземпляра из VMSS</span><span class="sxs-lookup"><span data-stu-id="51f45-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="51f45-113">Эта команда удаляет из VMSS ID расширения, который принадлежит группе ресурсов "Группа002".</span><span class="sxs-lookup"><span data-stu-id="51f45-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="51f45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51f45-114">PARAMETERS</span></span>

### <span data-ttu-id="51f45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f45-115">-DefaultProfile</span></span>
<span data-ttu-id="51f45-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51f45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f45-117">-Id</span><span class="sxs-lookup"><span data-stu-id="51f45-117">-Id</span></span>
<span data-ttu-id="51f45-118">Определяет код расширения, которое этот cmdlet удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="51f45-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f45-119">-Name</span><span class="sxs-lookup"><span data-stu-id="51f45-119">-Name</span></span>
<span data-ttu-id="51f45-120">Указывает имя расширения, которое этот cmdlet удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="51f45-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f45-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="51f45-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="51f45-122">Определяет VMSS, из которых нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="51f45-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="51f45-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51f45-123">-Confirm</span></span>
<span data-ttu-id="51f45-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f45-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f45-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f45-125">-WhatIf</span></span>
<span data-ttu-id="51f45-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f45-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51f45-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="51f45-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f45-128">CommonParameters</span></span>
<span data-ttu-id="51f45-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f45-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51f45-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f45-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51f45-131">INPUTS</span></span>

### <span data-ttu-id="51f45-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="51f45-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="51f45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51f45-133">System.String</span></span>

## <span data-ttu-id="51f45-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51f45-134">OUTPUTS</span></span>

### <span data-ttu-id="51f45-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="51f45-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="51f45-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="51f45-136">NOTES</span></span>

## <span data-ttu-id="51f45-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51f45-137">RELATED LINKS</span></span>

[<span data-ttu-id="51f45-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="51f45-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
