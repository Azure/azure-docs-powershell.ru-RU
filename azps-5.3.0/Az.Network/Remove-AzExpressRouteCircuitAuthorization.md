---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421516"
---
# <span data-ttu-id="ee96a-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee96a-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ee96a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee96a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee96a-103">Удаляет существующую авторизацию конфигурации ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee96a-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="ee96a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee96a-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee96a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee96a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee96a-106">Cmdlet **Remove-AzExpressRouteCircuitAuthorization** удаляет авторизацию, назначенную каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee96a-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="ee96a-107">Схемы ExpressRoute подключают вашу локальное сеть к Azure с помощью поставщика услуг подключения, а не общесетного Интернета.</span><span class="sxs-lookup"><span data-stu-id="ee96a-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ee96a-108">Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения своей сети к каналу.</span><span class="sxs-lookup"><span data-stu-id="ee96a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="ee96a-109">В виртуальной сети может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="ee96a-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="ee96a-110">Однако владелец схемы в любое время может использовать **Remove-AzExpressRouteCircuitAuthorization** для удаления авторизации, назначенной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ee96a-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="ee96a-111">В этом случае соответствующая виртуальная сеть больше не может использовать канал ExpressRoute для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="ee96a-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="ee96a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee96a-112">EXAMPLES</span></span>

### <span data-ttu-id="ee96a-113">Пример 1. Удаление авторизации каналов из схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ee96a-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="ee96a-114">В этом примере авторизация каналов удаляется из каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee96a-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="ee96a-115">Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на канал ExpressRoute с именем ContosoCircuit и сохраняет результат в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="ee96a-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="ee96a-116">Вторая команда отмечает авторизацию схемы ContosoCircuitAuthorization для удаления.</span><span class="sxs-lookup"><span data-stu-id="ee96a-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="ee96a-117">Третья команда использует Set-AzExpressRouteCircuit для подтверждения удаления схемы ExpressRoute, $Circuit переменной.</span><span class="sxs-lookup"><span data-stu-id="ee96a-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="ee96a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee96a-118">PARAMETERS</span></span>

### <span data-ttu-id="ee96a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee96a-119">-DefaultProfile</span></span>
<span data-ttu-id="ee96a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee96a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee96a-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee96a-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ee96a-122">Определяет объект ExpressRouteCircuit, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee96a-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee96a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ee96a-123">-Name</span></span>
<span data-ttu-id="ee96a-124">Указывает имя авторизации каналов, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee96a-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ee96a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee96a-125">CommonParameters</span></span>
<span data-ttu-id="ee96a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee96a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee96a-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee96a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee96a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee96a-128">INPUTS</span></span>

### <span data-ttu-id="ee96a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee96a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ee96a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee96a-130">OUTPUTS</span></span>

### <span data-ttu-id="ee96a-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee96a-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ee96a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee96a-132">NOTES</span></span>

## <span data-ttu-id="ee96a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee96a-133">RELATED LINKS</span></span>

[<span data-ttu-id="ee96a-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee96a-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee96a-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee96a-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ee96a-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee96a-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee96a-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee96a-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee96a-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee96a-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
