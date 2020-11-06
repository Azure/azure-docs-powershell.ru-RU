---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564800"
---
# <span data-ttu-id="6471e-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6471e-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="6471e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6471e-102">SYNOPSIS</span></span>
<span data-ttu-id="6471e-103">Добавляет конфигурацию пула адресных баз данных в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6471e-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6471e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6471e-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6471e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6471e-105">DESCRIPTION</span></span>
<span data-ttu-id="6471e-106">Командлет **Add-AzureRmLoadBalancerBackend** добавляет пул серверных адресов в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="6471e-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="6471e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6471e-107">EXAMPLES</span></span>

### <span data-ttu-id="6471e-108">Пример 1. Добавление конфигурации пула адресов серверной части в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="6471e-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="6471e-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer, добавляет пул серверных адресов с именем BackendAddressPool02 в MyLoadBalancer, а затем использует командлет **Set-AzureRmLoadBalancer** для обновления MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="6471e-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="6471e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6471e-110">PARAMETERS</span></span>

### <span data-ttu-id="6471e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6471e-111">-DefaultProfile</span></span>
<span data-ttu-id="6471e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6471e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6471e-113">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="6471e-113">-LoadBalancer</span></span>
<span data-ttu-id="6471e-114">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="6471e-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="6471e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6471e-115">-Name</span></span>
<span data-ttu-id="6471e-116">Указывает имя конфигурации пула адресов серверной базы данных, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="6471e-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6471e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6471e-117">CommonParameters</span></span>
<span data-ttu-id="6471e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6471e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6471e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6471e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6471e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6471e-120">INPUTS</span></span>

### <span data-ttu-id="6471e-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6471e-121">PSLoadBalancer</span></span>
<span data-ttu-id="6471e-122">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6471e-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6471e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6471e-123">OUTPUTS</span></span>

### <span data-ttu-id="6471e-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6471e-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6471e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="6471e-125">NOTES</span></span>

## <span data-ttu-id="6471e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6471e-126">RELATED LINKS</span></span>

[<span data-ttu-id="6471e-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6471e-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="6471e-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6471e-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="6471e-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6471e-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6471e-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6471e-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6471e-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6471e-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


