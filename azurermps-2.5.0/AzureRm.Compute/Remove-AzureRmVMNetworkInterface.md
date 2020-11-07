---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914202"
---
# <span data-ttu-id="13b39-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13b39-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="13b39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13b39-102">SYNOPSIS</span></span>
<span data-ttu-id="13b39-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="13b39-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13b39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13b39-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b39-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13b39-105">DESCRIPTION</span></span>
<span data-ttu-id="13b39-106">Командлет **Remove-AzureRmVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="13b39-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="13b39-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13b39-107">EXAMPLES</span></span>

### <span data-ttu-id="13b39-108">1:</span><span class="sxs-lookup"><span data-stu-id="13b39-108">1:</span></span>
```

```

## <span data-ttu-id="13b39-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13b39-109">PARAMETERS</span></span>

### <span data-ttu-id="13b39-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b39-110">-DefaultProfile</span></span>
<span data-ttu-id="13b39-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13b39-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b39-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="13b39-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="13b39-113">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="13b39-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13b39-114">-VM</span><span class="sxs-lookup"><span data-stu-id="13b39-114">-VM</span></span>
<span data-ttu-id="13b39-115">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="13b39-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="13b39-116">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="13b39-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="13b39-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b39-117">-Confirm</span></span>
<span data-ttu-id="13b39-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13b39-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="13b39-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b39-119">-WhatIf</span></span>
<span data-ttu-id="13b39-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13b39-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13b39-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13b39-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="13b39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b39-122">CommonParameters</span></span>
<span data-ttu-id="13b39-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13b39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b39-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b39-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b39-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13b39-125">INPUTS</span></span>

### <span data-ttu-id="13b39-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="13b39-126">PSVirtualMachine</span></span>
<span data-ttu-id="13b39-127">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="13b39-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="13b39-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13b39-128">OUTPUTS</span></span>

### <span data-ttu-id="13b39-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="13b39-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="13b39-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="13b39-130">NOTES</span></span>

## <span data-ttu-id="13b39-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13b39-131">RELATED LINKS</span></span>

[<span data-ttu-id="13b39-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13b39-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


