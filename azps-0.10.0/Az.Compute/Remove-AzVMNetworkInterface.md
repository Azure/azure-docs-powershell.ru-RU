---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911408"
---
# <span data-ttu-id="ee818-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ee818-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="ee818-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee818-102">SYNOPSIS</span></span>
<span data-ttu-id="ee818-103">Удаление сетевого интерфейса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ee818-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ee818-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee818-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee818-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee818-105">DESCRIPTION</span></span>
<span data-ttu-id="ee818-106">Командлет **Remove-AzVMNetworkInterface** удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ee818-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="ee818-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee818-107">EXAMPLES</span></span>

### <span data-ttu-id="ee818-108">1:</span><span class="sxs-lookup"><span data-stu-id="ee818-108">1:</span></span>
```

```

## <span data-ttu-id="ee818-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee818-109">PARAMETERS</span></span>

### <span data-ttu-id="ee818-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee818-110">-DefaultProfile</span></span>
<span data-ttu-id="ee818-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee818-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee818-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="ee818-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="ee818-113">Указывает массив идентификаторов сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ee818-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee818-114">-VM</span><span class="sxs-lookup"><span data-stu-id="ee818-114">-VM</span></span>
<span data-ttu-id="ee818-115">Указывает виртуальную машину, с которой этот командлет удаляет сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ee818-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="ee818-116">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ee818-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="ee818-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee818-117">-Confirm</span></span>
<span data-ttu-id="ee818-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee818-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="ee818-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee818-119">-WhatIf</span></span>
<span data-ttu-id="ee818-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee818-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee818-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee818-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="ee818-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee818-122">CommonParameters</span></span>
<span data-ttu-id="ee818-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee818-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee818-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee818-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee818-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee818-125">INPUTS</span></span>

### <span data-ttu-id="ee818-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ee818-126">PSVirtualMachine</span></span>
<span data-ttu-id="ee818-127">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee818-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ee818-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee818-128">OUTPUTS</span></span>

### <span data-ttu-id="ee818-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ee818-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ee818-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee818-130">NOTES</span></span>

## <span data-ttu-id="ee818-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee818-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee818-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee818-132">Get-AzVM</span></span>](./Get-AzVM.md)


