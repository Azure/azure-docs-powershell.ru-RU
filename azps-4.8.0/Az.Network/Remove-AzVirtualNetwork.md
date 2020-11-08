---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244344"
---
# <span data-ttu-id="f4bf9-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4bf9-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="f4bf9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bf9-103">Удаляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-103">Removes a virtual network.</span></span>

## <span data-ttu-id="f4bf9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4bf9-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4bf9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="f4bf9-106">Командлет **Remove-AzVirtualNetwork** удаляет виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="f4bf9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="f4bf9-108">1: создание и удаление виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f4bf9-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="f4bf9-109">Этот пример создает виртуальную сеть в группе ресурсов, а затем немедленно удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f4bf9-110">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="f4bf9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4bf9-111">PARAMETERS</span></span>

### <span data-ttu-id="f4bf9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4bf9-112">-AsJob</span></span>
<span data-ttu-id="f4bf9-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4bf9-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bf9-114">-DefaultProfile</span></span>
<span data-ttu-id="f4bf9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4bf9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f4bf9-116">-Force</span></span>
<span data-ttu-id="f4bf9-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4bf9-118">-Name</span></span>
<span data-ttu-id="f4bf9-119">Указывает имя виртуальной сети, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4bf9-120">-PassThru</span></span>
<span data-ttu-id="f4bf9-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4bf9-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4bf9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4bf9-124">Указывает имя группы ресурсов, которая содержит виртуальную сеть, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4bf9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4bf9-125">-Confirm</span></span>
<span data-ttu-id="f4bf9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4bf9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4bf9-127">-WhatIf</span></span>
<span data-ttu-id="f4bf9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4bf9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4bf9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bf9-130">CommonParameters</span></span>
<span data-ttu-id="f4bf9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4bf9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bf9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4bf9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bf9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4bf9-133">INPUTS</span></span>

### <span data-ttu-id="f4bf9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f4bf9-134">System.String</span></span>

## <span data-ttu-id="f4bf9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4bf9-135">OUTPUTS</span></span>

### <span data-ttu-id="f4bf9-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4bf9-136">System.Boolean</span></span>

## <span data-ttu-id="f4bf9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4bf9-137">NOTES</span></span>

## <span data-ttu-id="f4bf9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4bf9-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4bf9-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4bf9-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f4bf9-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4bf9-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f4bf9-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4bf9-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


