---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246580"
---
# <span data-ttu-id="87688-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87688-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="87688-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87688-102">SYNOPSIS</span></span>
<span data-ttu-id="87688-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="87688-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="87688-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87688-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87688-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87688-105">DESCRIPTION</span></span>
<span data-ttu-id="87688-106">Командлет **Remove-AzVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="87688-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="87688-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87688-107">EXAMPLES</span></span>

## <span data-ttu-id="87688-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87688-108">PARAMETERS</span></span>

### <span data-ttu-id="87688-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87688-109">-DefaultProfile</span></span>
<span data-ttu-id="87688-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87688-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87688-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="87688-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="87688-112">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="87688-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="87688-113">-VM</span><span class="sxs-lookup"><span data-stu-id="87688-113">-VM</span></span>
<span data-ttu-id="87688-114">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="87688-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="87688-115">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="87688-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="87688-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87688-116">-Confirm</span></span>
<span data-ttu-id="87688-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87688-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87688-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87688-118">-WhatIf</span></span>
<span data-ttu-id="87688-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87688-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87688-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87688-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87688-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87688-121">CommonParameters</span></span>
<span data-ttu-id="87688-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87688-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87688-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87688-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87688-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87688-124">INPUTS</span></span>

### <span data-ttu-id="87688-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="87688-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="87688-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87688-126">OUTPUTS</span></span>

### <span data-ttu-id="87688-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="87688-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="87688-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="87688-128">NOTES</span></span>

## <span data-ttu-id="87688-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87688-129">RELATED LINKS</span></span>

[<span data-ttu-id="87688-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="87688-130">Get-AzVM</span></span>](./Get-AzVM.md)


