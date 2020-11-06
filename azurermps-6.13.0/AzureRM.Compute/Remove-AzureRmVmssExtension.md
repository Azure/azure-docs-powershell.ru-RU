---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 7ede92fa653fe04072b75ce03dd6928421e01c6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556772"
---
# <span data-ttu-id="a0564-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a0564-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="a0564-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0564-102">SYNOPSIS</span></span>
<span data-ttu-id="a0564-103">Удаляет расширение из VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0564-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0564-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0564-104">SYNTAX</span></span>

### <span data-ttu-id="a0564-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0564-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0564-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0564-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0564-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0564-107">DESCRIPTION</span></span>
<span data-ttu-id="a0564-108">Командлет **Remove-AzureRmVmssExtension** удаляет расширение из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a0564-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a0564-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0564-109">EXAMPLES</span></span>

### <span data-ttu-id="a0564-110">Пример 1: удаление расширения VMSS</span><span class="sxs-lookup"><span data-stu-id="a0564-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzureRmVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="a0564-111">Эта команда удаляет расширение VMSS и обновляет VMSS после изменения.</span><span class="sxs-lookup"><span data-stu-id="a0564-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="a0564-112">Пример 2: удаление экземпляра в VMSS</span><span class="sxs-lookup"><span data-stu-id="a0564-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="a0564-113">Эта команда удаляет ИД расширения из VMSS, который принадлежит группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="a0564-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a0564-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0564-114">PARAMETERS</span></span>

### <span data-ttu-id="a0564-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0564-115">-DefaultProfile</span></span>
<span data-ttu-id="a0564-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0564-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0564-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a0564-117">-Id</span></span>
<span data-ttu-id="a0564-118">Указывает идентификатор расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0564-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a0564-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0564-119">-Name</span></span>
<span data-ttu-id="a0564-120">Указывает имя расширения, которое этот командлет удаляет из VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0564-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a0564-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0564-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a0564-122">Указывает VMSS, из которого нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="a0564-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a0564-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0564-123">-Confirm</span></span>
<span data-ttu-id="a0564-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0564-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0564-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0564-125">-WhatIf</span></span>
<span data-ttu-id="a0564-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0564-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0564-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0564-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0564-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0564-128">CommonParameters</span></span>
<span data-ttu-id="a0564-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0564-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0564-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0564-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0564-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0564-131">INPUTS</span></span>

### <span data-ttu-id="a0564-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0564-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a0564-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a0564-133">System.String</span></span>

## <span data-ttu-id="a0564-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0564-134">OUTPUTS</span></span>

### <span data-ttu-id="a0564-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0564-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a0564-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0564-136">NOTES</span></span>

## <span data-ttu-id="a0564-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0564-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0564-138">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a0564-138">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
