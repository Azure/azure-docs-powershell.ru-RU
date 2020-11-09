---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249643"
---
# <span data-ttu-id="07916-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="07916-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="07916-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07916-102">SYNOPSIS</span></span>
<span data-ttu-id="07916-103">Удаление существующей авторизации конфигурации ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="07916-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="07916-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07916-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07916-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07916-105">DESCRIPTION</span></span>
<span data-ttu-id="07916-106">Командлет **Remove-AzExpressRouteCircuitAuthorization** удаляет авторизацию, связанную с цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="07916-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="07916-107">Каналы ExpressRoute соединяют локальную сеть с Azure с помощью провайдера соединений вместо общедоступного Интернета.</span><span class="sxs-lookup"><span data-stu-id="07916-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="07916-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к каналу.</span><span class="sxs-lookup"><span data-stu-id="07916-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="07916-109">В каждой виртуальной сети может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="07916-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="07916-110">Тем не менее, в любое время владелец цепи может использовать **Remove-AzExpressRouteCircuitAuthorization** для удаления авторизации, назначенной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="07916-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="07916-111">Когда это случится, соответствующая виртуальная сеть больше не сможет использовать цепь ExpressRoute для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="07916-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="07916-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07916-112">EXAMPLES</span></span>

### <span data-ttu-id="07916-113">Пример 1: удаление авторизации канала из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="07916-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="07916-114">В этом примере удаляется проверка подлинности канала из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="07916-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="07916-115">Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале ExpressRoute с именем ContosoCircuit и сохраняет результат в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="07916-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="07916-116">Вторая команда отмечает ContosoCircuitAuthorization авторизации канала для удаления.</span><span class="sxs-lookup"><span data-stu-id="07916-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="07916-117">Третья команда использует командлет Set-AzExpressRouteCircuit для подтверждения удаления канала ExpressRoute, хранящегося в переменной $Circuit.</span><span class="sxs-lookup"><span data-stu-id="07916-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="07916-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07916-118">PARAMETERS</span></span>

### <span data-ttu-id="07916-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07916-119">-DefaultProfile</span></span>
<span data-ttu-id="07916-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07916-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07916-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07916-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="07916-122">Указывает объект ExpressRouteCircuit, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="07916-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07916-123">-Name</span></span>
<span data-ttu-id="07916-124">Указывает имя авторизации канала, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="07916-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07916-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07916-125">CommonParameters</span></span>
<span data-ttu-id="07916-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07916-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07916-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07916-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07916-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07916-128">INPUTS</span></span>

### <span data-ttu-id="07916-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07916-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="07916-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07916-130">OUTPUTS</span></span>

### <span data-ttu-id="07916-131">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07916-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="07916-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="07916-132">NOTES</span></span>

## <span data-ttu-id="07916-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07916-133">RELATED LINKS</span></span>

[<span data-ttu-id="07916-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="07916-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="07916-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07916-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="07916-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="07916-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="07916-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="07916-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="07916-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07916-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)