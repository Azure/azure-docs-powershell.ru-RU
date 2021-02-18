---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223668"
---
# <span data-ttu-id="98308-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="98308-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="98308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98308-102">SYNOPSIS</span></span>
<span data-ttu-id="98308-103">Удаляет конфигурацию пула адресов для загрузки из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98308-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="98308-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98308-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98308-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98308-105">DESCRIPTION</span></span>
<span data-ttu-id="98308-106">С **помощью cmdlet Remove-AzLoadBalancerBackendAddressPoolConfig** можно удалить пул адресов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="98308-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="98308-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98308-107">EXAMPLES</span></span>

### <span data-ttu-id="98308-108">Пример 1. Удаление конфигурации пула адресов для резервов загрузки из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="98308-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="98308-109">Эта команда получает балансир загрузки MyLoadBalancer и передает ее **в remove-AzLoadBalancerBackendAddressPoolConfig,** который удаляет конфигурацию BackendAddressPool02 из MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="98308-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig**, which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="98308-110">Наконец, Set-AzLoadBalancer-код обновляет MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="98308-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="98308-111">Обратите внимание на то, что для удаления пула адресов должен существовать резервная почта.</span><span class="sxs-lookup"><span data-stu-id="98308-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="98308-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98308-112">PARAMETERS</span></span>

### <span data-ttu-id="98308-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98308-113">-DefaultProfile</span></span>
<span data-ttu-id="98308-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98308-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98308-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98308-115">-LoadBalancer</span></span>
<span data-ttu-id="98308-116">Указывает балансировую нагрузку, которая содержит пул адресов для удаления.</span><span class="sxs-lookup"><span data-stu-id="98308-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98308-117">-Name</span><span class="sxs-lookup"><span data-stu-id="98308-117">-Name</span></span>
<span data-ttu-id="98308-118">Имя пула адресов, удаляемого этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98308-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98308-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98308-119">-Confirm</span></span>
<span data-ttu-id="98308-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98308-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98308-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98308-121">-WhatIf</span></span>
<span data-ttu-id="98308-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98308-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98308-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="98308-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98308-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98308-124">CommonParameters</span></span>
<span data-ttu-id="98308-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98308-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98308-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98308-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98308-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98308-127">INPUTS</span></span>

### <span data-ttu-id="98308-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98308-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="98308-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98308-129">OUTPUTS</span></span>

### <span data-ttu-id="98308-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98308-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="98308-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98308-131">NOTES</span></span>

## <span data-ttu-id="98308-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98308-132">RELATED LINKS</span></span>

[<span data-ttu-id="98308-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="98308-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="98308-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98308-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="98308-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="98308-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="98308-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="98308-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


