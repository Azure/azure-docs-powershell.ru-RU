---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d97c6825a6681127e2275a7d3d171e6500daba5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902561"
---
# <span data-ttu-id="8239d-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8239d-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="8239d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8239d-102">SYNOPSIS</span></span>
<span data-ttu-id="8239d-103">Добавление авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8239d-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="8239d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8239d-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8239d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8239d-105">DESCRIPTION</span></span>
<span data-ttu-id="8239d-106">Командлет **Add-AzExpressRouteCircuitAuthorization** добавляет авторизацию в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8239d-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="8239d-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="8239d-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="8239d-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="8239d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="8239d-109">**Add-AzExpressRouteCircuitAuthorization** добавляет новую авторизацию в цепь и, в то же время, создает соответствующий ключ проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8239d-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="8239d-110">Эти ключи можно просмотреть в любое время, запустив командлет Get-AzExpressRouteCircuitAuthorization и, при необходимости, можно скопировать его и перенаправить на соответствующий владелец сети.</span><span class="sxs-lookup"><span data-stu-id="8239d-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="8239d-111">Обратите внимание, что после выполнения **Add-AzExpressRouteCircuitAuthorization** необходимо вызвать командлет Set-AzExpressRouteCircuit, чтобы активировать ключ.</span><span class="sxs-lookup"><span data-stu-id="8239d-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="8239d-112">Если вы не вызываете **Set-AzExpressRouteCircuit** , авторизация будет добавлена в цепь, но не будет включена для использования.</span><span class="sxs-lookup"><span data-stu-id="8239d-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="8239d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8239d-113">EXAMPLES</span></span>

### <span data-ttu-id="8239d-114">Пример 1: Добавление авторизации для указанной цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8239d-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="8239d-115">Команды в этом примере добавляют новую авторизацию в существующую цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8239d-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="8239d-116">Первая команда использует **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="8239d-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="8239d-117">Ссылка на объект хранится в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="8239d-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="8239d-118">Во второй команде командлет **Add-AzExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8239d-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="8239d-119">Эта команда добавляет авторизацию, но не активирует эту авторизацию.</span><span class="sxs-lookup"><span data-stu-id="8239d-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="8239d-120">Для активации авторизации требуется **Set-AzExpressRouteCircuit** , показанный в финальной команде примера.</span><span class="sxs-lookup"><span data-stu-id="8239d-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="8239d-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8239d-121">PARAMETERS</span></span>

### <span data-ttu-id="8239d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8239d-122">-DefaultProfile</span></span>
<span data-ttu-id="8239d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8239d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8239d-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8239d-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8239d-125">Указывает канал ExpressRoute, на который добавляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8239d-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="8239d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8239d-126">-Name</span></span>
<span data-ttu-id="8239d-127">Указывает имя добавляемой авторизации цепи.</span><span class="sxs-lookup"><span data-stu-id="8239d-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8239d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8239d-128">CommonParameters</span></span>
<span data-ttu-id="8239d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8239d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8239d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8239d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8239d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8239d-131">INPUTS</span></span>

### <span data-ttu-id="8239d-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8239d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8239d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8239d-133">OUTPUTS</span></span>

### <span data-ttu-id="8239d-134">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8239d-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8239d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8239d-135">NOTES</span></span>

## <span data-ttu-id="8239d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8239d-136">RELATED LINKS</span></span>

[<span data-ttu-id="8239d-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8239d-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8239d-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8239d-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8239d-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8239d-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8239d-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8239d-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8239d-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8239d-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
