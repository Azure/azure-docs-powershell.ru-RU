---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: b77d741c0313e202304be3fd51fb3e1cd5b25b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557875"
---
# <span data-ttu-id="bb087-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bb087-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="bb087-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb087-102">SYNOPSIS</span></span>
<span data-ttu-id="bb087-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb087-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb087-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb087-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb087-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb087-105">DESCRIPTION</span></span>
<span data-ttu-id="bb087-106">Командлет **Remove-AzureRmVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb087-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="bb087-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb087-107">EXAMPLES</span></span>

## <span data-ttu-id="bb087-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb087-108">PARAMETERS</span></span>

### <span data-ttu-id="bb087-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb087-109">-DefaultProfile</span></span>
<span data-ttu-id="bb087-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb087-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb087-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="bb087-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="bb087-112">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bb087-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb087-113">-VM</span><span class="sxs-lookup"><span data-stu-id="bb087-113">-VM</span></span>
<span data-ttu-id="bb087-114">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bb087-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="bb087-115">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="bb087-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="bb087-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb087-116">-Confirm</span></span>
<span data-ttu-id="bb087-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb087-117">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="bb087-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb087-118">-WhatIf</span></span>
<span data-ttu-id="bb087-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb087-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb087-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb087-120">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="bb087-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb087-121">CommonParameters</span></span>
<span data-ttu-id="bb087-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb087-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb087-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb087-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb087-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb087-124">INPUTS</span></span>

## <span data-ttu-id="bb087-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb087-125">OUTPUTS</span></span>

## <span data-ttu-id="bb087-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb087-126">NOTES</span></span>

## <span data-ttu-id="bb087-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb087-127">RELATED LINKS</span></span>

[<span data-ttu-id="bb087-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bb087-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


