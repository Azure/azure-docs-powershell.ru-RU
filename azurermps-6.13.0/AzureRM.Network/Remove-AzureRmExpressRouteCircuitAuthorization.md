---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 6a8c81f8c130f322e868c91e18c7fff7b1175d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568472"
---
# <span data-ttu-id="bb1fa-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fa-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="bb1fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1fa-103">Удаление существующей авторизации конфигурации ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb1fa-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb1fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb1fa-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1fa-106">Командлет **Remove-AzureRmExpressRouteCircuitAuthorization** удаляет авторизацию, связанную с цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="bb1fa-107">Каналы ExpressRoute соединяют локальную сеть с Azure с помощью провайдера соединений вместо общедоступного Интернета.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="bb1fa-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к каналу.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="bb1fa-109">В каждой виртуальной сети может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="bb1fa-110">Тем не менее, в любое время владелец цепи может использовать **Remove-AzureRmExpressRouteCircuitAuthorization** для удаления авторизации, назначенной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="bb1fa-111">Когда это случится, соответствующая виртуальная сеть больше не сможет использовать цепь ExpressRoute для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="bb1fa-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb1fa-112">EXAMPLES</span></span>

### <span data-ttu-id="bb1fa-113">Пример 1: удаление авторизации канала из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bb1fa-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="bb1fa-114">В этом примере удаляется проверка подлинности канала из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="bb1fa-115">Первая команда использует командлет **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале ExpressRoute с именем ContosoCircuit и сохраняет результат в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="bb1fa-116">Вторая команда отмечает ContosoCircuitAuthorization авторизации канала для удаления.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="bb1fa-117">Третья команда использует командлет Set-AzureRmExpressRouteCircuit для подтверждения удаления канала ExpressRoute, хранящегося в переменной $Circuit.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="bb1fa-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb1fa-118">PARAMETERS</span></span>

### <span data-ttu-id="bb1fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1fa-119">-DefaultProfile</span></span>
<span data-ttu-id="bb1fa-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb1fa-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb1fa-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bb1fa-122">Указывает объект ExpressRouteCircuit, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb1fa-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb1fa-123">-Name</span></span>
<span data-ttu-id="bb1fa-124">Указывает имя авторизации канала, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb1fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1fa-125">CommonParameters</span></span>
<span data-ttu-id="bb1fa-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb1fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1fa-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1fa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb1fa-128">INPUTS</span></span>

### <span data-ttu-id="bb1fa-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb1fa-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="bb1fa-130">Параметры: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb1fa-130">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="bb1fa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb1fa-131">OUTPUTS</span></span>

### <span data-ttu-id="bb1fa-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb1fa-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bb1fa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb1fa-133">NOTES</span></span>

## <span data-ttu-id="bb1fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb1fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb1fa-135">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fa-135">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bb1fa-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb1fa-136">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="bb1fa-137">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fa-137">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bb1fa-138">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fa-138">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bb1fa-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb1fa-139">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
