---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910144"
---
# <span data-ttu-id="59aec-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="59aec-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="59aec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59aec-102">SYNOPSIS</span></span>
<span data-ttu-id="59aec-103">Добавляет конфигурацию пула адресных баз данных в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="59aec-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="59aec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59aec-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59aec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59aec-105">DESCRIPTION</span></span>
<span data-ttu-id="59aec-106">Командлет **Add-AzLoadBalancerBackend** добавляет пул серверных адресов в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="59aec-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="59aec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59aec-107">EXAMPLES</span></span>

### <span data-ttu-id="59aec-108">Пример 1. Добавление конфигурации пула адресов серверной части в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="59aec-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="59aec-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer, добавляет пул серверных адресов с именем BackendAddressPool02 в MyLoadBalancer, а затем использует командлет **Set-AzLoadBalancer** для обновления MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="59aec-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="59aec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59aec-110">PARAMETERS</span></span>

### <span data-ttu-id="59aec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59aec-111">-DefaultProfile</span></span>
<span data-ttu-id="59aec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59aec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59aec-113">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="59aec-113">-LoadBalancer</span></span>
<span data-ttu-id="59aec-114">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="59aec-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="59aec-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59aec-115">-Name</span></span>
<span data-ttu-id="59aec-116">Указывает имя конфигурации пула адресов серверной базы данных, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="59aec-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="59aec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59aec-117">CommonParameters</span></span>
<span data-ttu-id="59aec-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59aec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59aec-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59aec-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59aec-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59aec-120">INPUTS</span></span>

### <span data-ttu-id="59aec-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59aec-121">PSLoadBalancer</span></span>
<span data-ttu-id="59aec-122">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="59aec-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="59aec-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59aec-123">OUTPUTS</span></span>

### <span data-ttu-id="59aec-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59aec-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="59aec-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="59aec-125">NOTES</span></span>

## <span data-ttu-id="59aec-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59aec-126">RELATED LINKS</span></span>

[<span data-ttu-id="59aec-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59aec-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="59aec-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="59aec-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="59aec-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="59aec-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="59aec-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="59aec-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="59aec-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="59aec-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


