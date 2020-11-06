---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: eb7f7b85286d491d4168e08ef94c1a46ff9076ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557743"
---
# <span data-ttu-id="bbf42-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bbf42-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="bbf42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbf42-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf42-103">Удаляет конфигурацию пула адресных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="bbf42-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbf42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbf42-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf42-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbf42-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf42-106">Командлет **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** удаляет пул серверных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="bbf42-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="bbf42-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbf42-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf42-108">Пример 1: Удаление конфигурации пула адресов серверной части из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="bbf42-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="bbf42-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и передает ее в **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , удаляя конфигурацию BackendAddressPool02 из MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="bbf42-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="bbf42-110">Наконец, командлет Set-AzureRmLoadBalancer обновляет MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="bbf42-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="bbf42-111">Обратите внимание, что конфигурация пула адресных адресов сервера должна существовать, прежде чем ее можно будет удалить.</span><span class="sxs-lookup"><span data-stu-id="bbf42-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="bbf42-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbf42-112">PARAMETERS</span></span>

### <span data-ttu-id="bbf42-113">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="bbf42-113">-LoadBalancer</span></span>
<span data-ttu-id="bbf42-114">Указывает подсистему балансировки нагрузки, которая содержит пул серверных адресов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bbf42-114">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf42-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbf42-115">-Name</span></span>
<span data-ttu-id="bbf42-116">Указывает имя пула адресных адресов серверной платформы, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bbf42-116">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bbf42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf42-117">-DefaultProfile</span></span>
<span data-ttu-id="bbf42-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf42-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbf42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf42-119">CommonParameters</span></span>
<span data-ttu-id="bbf42-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbf42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf42-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf42-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf42-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbf42-122">INPUTS</span></span>

### <span data-ttu-id="bbf42-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbf42-123">PSLoadBalancer</span></span>
<span data-ttu-id="bbf42-124">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bbf42-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bbf42-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbf42-125">OUTPUTS</span></span>

### <span data-ttu-id="bbf42-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbf42-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbf42-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbf42-127">NOTES</span></span>

## <span data-ttu-id="bbf42-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbf42-128">RELATED LINKS</span></span>

[<span data-ttu-id="bbf42-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bbf42-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="bbf42-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbf42-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bbf42-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bbf42-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="bbf42-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="bbf42-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


