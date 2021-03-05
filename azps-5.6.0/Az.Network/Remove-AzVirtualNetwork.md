---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 18d73d317b1bf2056fdefdfbc112c56bc4ebdfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006051"
---
# <span data-ttu-id="8d1ab-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d1ab-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="8d1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1ab-103">Удаляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-103">Removes a virtual network.</span></span>

## <span data-ttu-id="8d1ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d1ab-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d1ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="8d1ab-106">Командлет **Remove-AzVirtualNetwork** удаляет виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="8d1ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d1ab-107">EXAMPLES</span></span>

### <span data-ttu-id="8d1ab-108">1. Создание и удаление виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8d1ab-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="8d1ab-109">В этом примере создается виртуальная сеть в группе ресурсов, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8d1ab-110">Чтобы скрыть запрос при удалении виртуальной сети, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="8d1ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d1ab-111">PARAMETERS</span></span>

### <span data-ttu-id="8d1ab-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d1ab-112">-AsJob</span></span>
<span data-ttu-id="8d1ab-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8d1ab-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d1ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1ab-114">-DefaultProfile</span></span>
<span data-ttu-id="8d1ab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d1ab-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8d1ab-116">-Force</span></span>
<span data-ttu-id="8d1ab-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d1ab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8d1ab-118">-Name</span></span>
<span data-ttu-id="8d1ab-119">Указывает имя виртуальной сети, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d1ab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d1ab-120">-PassThru</span></span>
<span data-ttu-id="8d1ab-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8d1ab-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d1ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d1ab-124">Имя группы ресурсов, которая содержит виртуальную сеть, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d1ab-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d1ab-125">-Confirm</span></span>
<span data-ttu-id="8d1ab-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d1ab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d1ab-127">-WhatIf</span></span>
<span data-ttu-id="8d1ab-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d1ab-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d1ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1ab-130">CommonParameters</span></span>
<span data-ttu-id="8d1ab-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d1ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1ab-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1ab-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1ab-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d1ab-133">INPUTS</span></span>

### <span data-ttu-id="8d1ab-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8d1ab-134">System.String</span></span>

## <span data-ttu-id="8d1ab-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d1ab-135">OUTPUTS</span></span>

### <span data-ttu-id="8d1ab-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d1ab-136">System.Boolean</span></span>

## <span data-ttu-id="8d1ab-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d1ab-137">NOTES</span></span>

## <span data-ttu-id="8d1ab-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d1ab-138">RELATED LINKS</span></span>

[<span data-ttu-id="8d1ab-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d1ab-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="8d1ab-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d1ab-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="8d1ab-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d1ab-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


