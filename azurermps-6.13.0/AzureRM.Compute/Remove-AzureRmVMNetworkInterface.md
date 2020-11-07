---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733896"
---
# <span data-ttu-id="420e2-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="420e2-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="420e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="420e2-102">SYNOPSIS</span></span>
<span data-ttu-id="420e2-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="420e2-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="420e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="420e2-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="420e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="420e2-105">DESCRIPTION</span></span>
<span data-ttu-id="420e2-106">Командлет **Remove-AzureRmVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="420e2-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="420e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="420e2-107">EXAMPLES</span></span>

## <span data-ttu-id="420e2-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="420e2-108">PARAMETERS</span></span>

### <span data-ttu-id="420e2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420e2-109">-DefaultProfile</span></span>
<span data-ttu-id="420e2-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="420e2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="420e2-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="420e2-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="420e2-112">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="420e2-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="420e2-113">-VM</span><span class="sxs-lookup"><span data-stu-id="420e2-113">-VM</span></span>
<span data-ttu-id="420e2-114">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="420e2-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="420e2-115">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="420e2-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="420e2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="420e2-116">-Confirm</span></span>
<span data-ttu-id="420e2-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="420e2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420e2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420e2-118">-WhatIf</span></span>
<span data-ttu-id="420e2-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="420e2-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="420e2-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="420e2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420e2-121">CommonParameters</span></span>
<span data-ttu-id="420e2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="420e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420e2-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420e2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420e2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="420e2-124">INPUTS</span></span>

### <span data-ttu-id="420e2-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="420e2-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="420e2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="420e2-126">OUTPUTS</span></span>

### <span data-ttu-id="420e2-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="420e2-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="420e2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="420e2-128">NOTES</span></span>

## <span data-ttu-id="420e2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="420e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="420e2-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="420e2-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


