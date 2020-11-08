---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248746"
---
# <span data-ttu-id="30cf2-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="30cf2-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="30cf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="30cf2-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="30cf2-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="30cf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30cf2-104">SYNTAX</span></span>

### <span data-ttu-id="30cf2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30cf2-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30cf2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30cf2-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30cf2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="30cf2-108">Командлет **Remove-AzVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="30cf2-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="30cf2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="30cf2-110">Пример 1: удаление расширения VMSS</span><span class="sxs-lookup"><span data-stu-id="30cf2-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="30cf2-111">Эта команда удаляет расширение VMSS и обновляет VMSS после изменения.</span><span class="sxs-lookup"><span data-stu-id="30cf2-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="30cf2-112">Пример 2: удаление экземпляра в VMSS</span><span class="sxs-lookup"><span data-stu-id="30cf2-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="30cf2-113">Эта команда удаляет ИД расширения из VMSS, который принадлежит группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="30cf2-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="30cf2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="30cf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cf2-115">-DefaultProfile</span></span>
<span data-ttu-id="30cf2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30cf2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30cf2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="30cf2-117">-Id</span></span>
<span data-ttu-id="30cf2-118">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="30cf2-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="30cf2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30cf2-119">-Name</span></span>
<span data-ttu-id="30cf2-120">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="30cf2-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="30cf2-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30cf2-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="30cf2-122">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="30cf2-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="30cf2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30cf2-123">-Confirm</span></span>
<span data-ttu-id="30cf2-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30cf2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30cf2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30cf2-125">-WhatIf</span></span>
<span data-ttu-id="30cf2-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30cf2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30cf2-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30cf2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30cf2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cf2-128">CommonParameters</span></span>
<span data-ttu-id="30cf2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30cf2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cf2-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30cf2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cf2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30cf2-131">INPUTS</span></span>

### <span data-ttu-id="30cf2-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30cf2-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="30cf2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="30cf2-133">System.String</span></span>

## <span data-ttu-id="30cf2-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30cf2-134">OUTPUTS</span></span>

### <span data-ttu-id="30cf2-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30cf2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="30cf2-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="30cf2-136">NOTES</span></span>

## <span data-ttu-id="30cf2-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30cf2-137">RELATED LINKS</span></span>

[<span data-ttu-id="30cf2-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="30cf2-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
