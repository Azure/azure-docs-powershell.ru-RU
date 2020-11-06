---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557535"
---
# <span data-ttu-id="cd2ca-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd2ca-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="cd2ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2ca-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd2ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd2ca-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2ca-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2ca-106">Командлет **Remove-AzureRmVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="cd2ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd2ca-107">EXAMPLES</span></span>

## <span data-ttu-id="cd2ca-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd2ca-108">PARAMETERS</span></span>

### <span data-ttu-id="cd2ca-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="cd2ca-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="cd2ca-110">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2ca-111">-VM</span><span class="sxs-lookup"><span data-stu-id="cd2ca-111">-VM</span></span>
<span data-ttu-id="cd2ca-112">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="cd2ca-113">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd2ca-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd2ca-114">-Confirm</span></span>
<span data-ttu-id="cd2ca-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="cd2ca-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2ca-116">-WhatIf</span></span>
<span data-ttu-id="cd2ca-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2ca-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="cd2ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2ca-119">CommonParameters</span></span>
<span data-ttu-id="cd2ca-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2ca-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2ca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2ca-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd2ca-122">INPUTS</span></span>

### <span data-ttu-id="cd2ca-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="cd2ca-123">None</span></span>
<span data-ttu-id="cd2ca-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cd2ca-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd2ca-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2ca-125">OUTPUTS</span></span>

## <span data-ttu-id="cd2ca-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd2ca-126">NOTES</span></span>

## <span data-ttu-id="cd2ca-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd2ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="cd2ca-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd2ca-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


