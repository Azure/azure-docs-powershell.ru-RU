---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913592"
---
# <span data-ttu-id="60ca3-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="60ca3-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="60ca3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="60ca3-103">Удаление существующей авторизации конфигурации ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60ca3-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ca3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60ca3-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ca3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="60ca3-106">Командлет **Remove-AzureRmExpressRouteCircuitAuthorization** удаляет авторизацию, связанную с цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60ca3-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="60ca3-107">Каналы ExpressRoute соединяют локальную сеть с Azure с помощью провайдера соединений вместо общедоступного Интернета.</span><span class="sxs-lookup"><span data-stu-id="60ca3-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="60ca3-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к каналу.</span><span class="sxs-lookup"><span data-stu-id="60ca3-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="60ca3-109">В каждой виртуальной сети может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="60ca3-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="60ca3-110">Тем не менее, в любое время владелец цепи может использовать **Remove-AzureRmExpressRouteCircuitAuthorization** для удаления авторизации, назначенной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="60ca3-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="60ca3-111">Когда это случится, соответствующая виртуальная сеть больше не сможет использовать цепь ExpressRoute для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="60ca3-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="60ca3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60ca3-112">EXAMPLES</span></span>

### <span data-ttu-id="60ca3-113">Пример 1: удаление авторизации канала из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="60ca3-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="60ca3-114">В этом примере удаляется проверка подлинности канала из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60ca3-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="60ca3-115">Первая команда использует командлет **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале ExpressRoute с именем ContosoCircuit и сохраняет результат в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="60ca3-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="60ca3-116">Вторая команда отмечает ContosoCircuitAuthorization авторизации канала для удаления.</span><span class="sxs-lookup"><span data-stu-id="60ca3-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="60ca3-117">Третья команда использует командлет Set-AzureRmExpressRouteCircuit для подтверждения удаления канала ExpressRoute, хранящегося в переменной $Circuit.</span><span class="sxs-lookup"><span data-stu-id="60ca3-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="60ca3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60ca3-118">PARAMETERS</span></span>

### <span data-ttu-id="60ca3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ca3-119">-DefaultProfile</span></span>
<span data-ttu-id="60ca3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60ca3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60ca3-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60ca3-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="60ca3-122">Указывает объект ExpressRouteCircuit, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="60ca3-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ca3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60ca3-123">-Name</span></span>
<span data-ttu-id="60ca3-124">Указывает имя авторизации канала, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="60ca3-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60ca3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ca3-125">CommonParameters</span></span>
<span data-ttu-id="60ca3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60ca3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ca3-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ca3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ca3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60ca3-128">INPUTS</span></span>

### <span data-ttu-id="60ca3-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60ca3-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="60ca3-130">Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="60ca3-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="60ca3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60ca3-131">OUTPUTS</span></span>

### <span data-ttu-id="60ca3-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60ca3-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="60ca3-133">Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="60ca3-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="60ca3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="60ca3-134">NOTES</span></span>

## <span data-ttu-id="60ca3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60ca3-135">RELATED LINKS</span></span>

[<span data-ttu-id="60ca3-136">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="60ca3-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="60ca3-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60ca3-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="60ca3-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="60ca3-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="60ca3-139">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="60ca3-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="60ca3-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60ca3-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
