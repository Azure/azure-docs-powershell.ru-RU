---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519513"
---
# <span data-ttu-id="94fca-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94fca-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="94fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94fca-102">SYNOPSIS</span></span>
<span data-ttu-id="94fca-103">Удаляет сетевой интерфейс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="94fca-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="94fca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94fca-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94fca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94fca-105">DESCRIPTION</span></span>
<span data-ttu-id="94fca-106">Командлет **Remove-AzVMNetworkInterface** удаляет сетевой интерфейс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="94fca-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="94fca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94fca-107">EXAMPLES</span></span>

## <span data-ttu-id="94fca-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94fca-108">PARAMETERS</span></span>

### <span data-ttu-id="94fca-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fca-109">-DefaultProfile</span></span>
<span data-ttu-id="94fca-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94fca-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94fca-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="94fca-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="94fca-112">Определяет массив кодов сетевого интерфейса, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94fca-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fca-113">-VM</span><span class="sxs-lookup"><span data-stu-id="94fca-113">-VM</span></span>
<span data-ttu-id="94fca-114">Указывает виртуальную машину, с которой этот cmdlet удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="94fca-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="94fca-115">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="94fca-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94fca-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94fca-116">-Confirm</span></span>
<span data-ttu-id="94fca-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94fca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94fca-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94fca-118">-WhatIf</span></span>
<span data-ttu-id="94fca-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94fca-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94fca-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94fca-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94fca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fca-121">CommonParameters</span></span>
<span data-ttu-id="94fca-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94fca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fca-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94fca-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fca-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94fca-124">INPUTS</span></span>

### <span data-ttu-id="94fca-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="94fca-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="94fca-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94fca-126">OUTPUTS</span></span>

### <span data-ttu-id="94fca-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="94fca-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="94fca-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94fca-128">NOTES</span></span>

## <span data-ttu-id="94fca-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94fca-129">RELATED LINKS</span></span>

[<span data-ttu-id="94fca-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="94fca-130">Get-AzVM</span></span>](./Get-AzVM.md)


