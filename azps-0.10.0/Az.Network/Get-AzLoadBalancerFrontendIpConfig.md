---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a0b1acf49aa177d05be7361eedf644320b609797
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909985"
---
# <span data-ttu-id="c1d23-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1d23-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c1d23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1d23-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d23-103">Получает интерфейсную конфигурацию IP в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c1d23-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="c1d23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1d23-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1d23-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d23-106">Командлет **Get-AzLoadBalancerFrontendIpConfig** получает интерфейсную конфигурацию IP или список IP-конфигураций интерфейсов в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c1d23-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="c1d23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1d23-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d23-108">Пример 1: получение интерфейсной конфигурации IP в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c1d23-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="c1d23-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="c1d23-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="c1d23-110">Вторая команда возвращает IP-конфигурацию переднего плана, связанную с этим балансировщикм нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c1d23-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="c1d23-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1d23-111">PARAMETERS</span></span>

### <span data-ttu-id="c1d23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d23-112">-DefaultProfile</span></span>
<span data-ttu-id="c1d23-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d23-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d23-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="c1d23-114">-LoadBalancer</span></span>
<span data-ttu-id="c1d23-115">Указывает подсистему балансировки нагрузки, связанную с интерфейсной конфигурацией IP-интерфейса, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c1d23-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="c1d23-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1d23-116">-Name</span></span>
<span data-ttu-id="c1d23-117">Указывает имя подсистемы балансировки нагрузки, содержащей интерфейсную конфигурацию IP-адресов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c1d23-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="c1d23-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d23-118">CommonParameters</span></span>
<span data-ttu-id="c1d23-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1d23-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d23-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d23-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d23-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1d23-121">INPUTS</span></span>

### <span data-ttu-id="c1d23-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c1d23-122">PSLoadBalancer</span></span>
<span data-ttu-id="c1d23-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1d23-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c1d23-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1d23-124">OUTPUTS</span></span>

### <span data-ttu-id="c1d23-125">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1d23-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c1d23-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1d23-126">NOTES</span></span>

## <span data-ttu-id="c1d23-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1d23-127">RELATED LINKS</span></span>

[<span data-ttu-id="c1d23-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1d23-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c1d23-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c1d23-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c1d23-130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1d23-130">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c1d23-131">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1d23-131">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c1d23-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1d23-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


