---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913856"
---
# <span data-ttu-id="ee472-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee472-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ee472-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee472-102">SYNOPSIS</span></span>
<span data-ttu-id="ee472-103">Добавление авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee472-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee472-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee472-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee472-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee472-105">DESCRIPTION</span></span>
<span data-ttu-id="ee472-106">Командлет **Add-AzureRmExpressRouteCircuitAuthorization** добавляет авторизацию в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee472-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="ee472-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="ee472-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ee472-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="ee472-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="ee472-109">**Add-AzureRmExpressRouteCircuitAuthorization** добавляет новую авторизацию в цепь и, в то же время, создает соответствующий ключ проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ee472-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="ee472-110">Эти ключи можно просмотреть в любое время, запустив командлет Get-AzureRmExpressRouteCircuitAuthorization и, при необходимости, можно скопировать его и перенаправить на соответствующий владелец сети.</span><span class="sxs-lookup"><span data-stu-id="ee472-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="ee472-111">Обратите внимание, что после выполнения **Add-AzureRmExpressRouteCircuitAuthorization** необходимо вызвать командлет Set-AzureRmExpressRouteCircuit, чтобы активировать ключ.</span><span class="sxs-lookup"><span data-stu-id="ee472-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="ee472-112">Если вы не вызываете **Set-AzureRmExpressRouteCircuit** , авторизация будет добавлена в цепь, но не будет включена для использования.</span><span class="sxs-lookup"><span data-stu-id="ee472-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="ee472-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee472-113">EXAMPLES</span></span>

### <span data-ttu-id="ee472-114">Пример 1: Добавление авторизации для указанной цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ee472-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="ee472-115">Команды в этом примере добавляют новую авторизацию в существующую цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee472-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="ee472-116">Первая команда использует **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="ee472-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="ee472-117">Ссылка на объект хранится в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="ee472-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="ee472-118">Во второй команде командлет **Add-AzureRmExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ee472-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="ee472-119">Эта команда добавляет авторизацию, но не активирует эту авторизацию.</span><span class="sxs-lookup"><span data-stu-id="ee472-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="ee472-120">Для активации авторизации требуется **Set-AzureRmExpressRouteCircuit** , показанный в финальной команде примера.</span><span class="sxs-lookup"><span data-stu-id="ee472-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="ee472-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee472-121">PARAMETERS</span></span>

### <span data-ttu-id="ee472-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee472-122">-DefaultProfile</span></span>
<span data-ttu-id="ee472-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee472-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee472-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee472-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ee472-125">Указывает канал ExpressRoute, на который добавляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ee472-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="ee472-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee472-126">-Name</span></span>
<span data-ttu-id="ee472-127">Указывает имя добавляемой авторизации цепи.</span><span class="sxs-lookup"><span data-stu-id="ee472-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="ee472-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee472-128">CommonParameters</span></span>
<span data-ttu-id="ee472-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee472-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee472-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee472-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee472-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee472-131">INPUTS</span></span>

### <span data-ttu-id="ee472-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee472-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ee472-133">**Add-AzureRmExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="ee472-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="ee472-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee472-134">OUTPUTS</span></span>

### <span data-ttu-id="ee472-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee472-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ee472-136">**Add-AzureRmExpressRouteCircuitAuthorization** изменяет экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="ee472-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="ee472-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee472-137">NOTES</span></span>

## <span data-ttu-id="ee472-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee472-138">RELATED LINKS</span></span>

[<span data-ttu-id="ee472-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee472-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ee472-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee472-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee472-141">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee472-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee472-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee472-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ee472-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee472-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
