---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909506"
---
# <span data-ttu-id="a1b87-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b87-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a1b87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1b87-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b87-103">Удаляет конфигурацию пула адресных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1b87-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="a1b87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1b87-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b87-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b87-106">Командлет **Remove-AzLoadBalancerBackendAddressPoolConfig** удаляет пул серверных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1b87-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a1b87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1b87-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b87-108">Пример 1: Удаление конфигурации пула адресов серверной части из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a1b87-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="a1b87-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и передает ее в **Remove-AzLoadBalancerBackendAddressPoolConfig** , удаляя конфигурацию BackendAddressPool02 из MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a1b87-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a1b87-110">Наконец, командлет Set-AzLoadBalancer обновляет MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a1b87-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a1b87-111">Обратите внимание, что конфигурация пула адресных адресов сервера должна существовать, прежде чем ее можно будет удалить.</span><span class="sxs-lookup"><span data-stu-id="a1b87-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a1b87-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1b87-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b87-113">-DefaultProfile</span></span>
<span data-ttu-id="a1b87-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b87-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a1b87-115">-LoadBalancer</span></span>
<span data-ttu-id="a1b87-116">Указывает подсистему балансировки нагрузки, которая содержит пул серверных адресов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1b87-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b87-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1b87-117">-Name</span></span>
<span data-ttu-id="a1b87-118">Указывает имя пула адресных адресов серверной платформы, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a1b87-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b87-119">CommonParameters</span></span>
<span data-ttu-id="a1b87-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1b87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b87-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b87-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b87-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1b87-122">INPUTS</span></span>

### <span data-ttu-id="a1b87-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b87-123">PSLoadBalancer</span></span>
<span data-ttu-id="a1b87-124">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a1b87-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a1b87-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b87-125">OUTPUTS</span></span>

### <span data-ttu-id="a1b87-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b87-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1b87-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1b87-127">NOTES</span></span>

## <span data-ttu-id="a1b87-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1b87-128">RELATED LINKS</span></span>

[<span data-ttu-id="a1b87-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b87-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a1b87-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b87-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1b87-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b87-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a1b87-132">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b87-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


