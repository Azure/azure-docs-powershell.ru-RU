---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910147"
---
# <span data-ttu-id="2ea73-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2ea73-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2ea73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ea73-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea73-103">Добавление авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ea73-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="2ea73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ea73-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea73-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea73-106">Командлет **Add-AzExpressRouteCircuitAuthorization** добавляет авторизацию в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ea73-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="2ea73-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="2ea73-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2ea73-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="2ea73-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="2ea73-109">**Add-AzExpressRouteCircuitAuthorization** добавляет новую авторизацию в цепь и, в то же время, создает соответствующий ключ проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2ea73-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="2ea73-110">Эти ключи можно просмотреть в любое время, запустив командлет Get-AzExpressRouteCircuitAuthorization и, при необходимости, можно скопировать его и перенаправить на соответствующий владелец сети.</span><span class="sxs-lookup"><span data-stu-id="2ea73-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="2ea73-111">Обратите внимание, что после выполнения **Add-AzExpressRouteCircuitAuthorization** необходимо вызвать командлет Set-AzExpressRouteCircuit, чтобы активировать ключ.</span><span class="sxs-lookup"><span data-stu-id="2ea73-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="2ea73-112">Если вы не вызываете **Set-AzExpressRouteCircuit** , авторизация будет добавлена в цепь, но не будет включена для использования.</span><span class="sxs-lookup"><span data-stu-id="2ea73-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="2ea73-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ea73-113">EXAMPLES</span></span>

### <span data-ttu-id="2ea73-114">Пример 1: Добавление авторизации для указанной цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2ea73-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="2ea73-115">Команды в этом примере добавляют новую авторизацию в существующую цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ea73-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="2ea73-116">Первая команда использует **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="2ea73-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="2ea73-117">Ссылка на объект хранится в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="2ea73-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="2ea73-118">Во второй команде командлет **Add-AzExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ea73-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="2ea73-119">Эта команда добавляет авторизацию, но не активирует эту авторизацию.</span><span class="sxs-lookup"><span data-stu-id="2ea73-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="2ea73-120">Для активации авторизации требуется **Set-AzExpressRouteCircuit** , показанный в финальной команде примера.</span><span class="sxs-lookup"><span data-stu-id="2ea73-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="2ea73-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ea73-121">PARAMETERS</span></span>

### <span data-ttu-id="2ea73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea73-122">-DefaultProfile</span></span>
<span data-ttu-id="2ea73-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea73-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea73-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea73-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2ea73-125">Указывает канал ExpressRoute, на который добавляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2ea73-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="2ea73-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ea73-126">-Name</span></span>
<span data-ttu-id="2ea73-127">Указывает имя добавляемой авторизации цепи.</span><span class="sxs-lookup"><span data-stu-id="2ea73-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="2ea73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea73-128">CommonParameters</span></span>
<span data-ttu-id="2ea73-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ea73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea73-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea73-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea73-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ea73-131">INPUTS</span></span>

### <span data-ttu-id="2ea73-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea73-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2ea73-133">**Add-AzExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2ea73-133">**Add-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2ea73-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ea73-134">OUTPUTS</span></span>

### <span data-ttu-id="2ea73-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea73-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2ea73-136">**Add-AzExpressRouteCircuitAuthorization** изменяет экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2ea73-136">**Add-AzExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2ea73-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ea73-137">NOTES</span></span>

## <span data-ttu-id="2ea73-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ea73-138">RELATED LINKS</span></span>

[<span data-ttu-id="2ea73-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea73-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2ea73-140">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2ea73-140">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2ea73-141">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2ea73-141">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2ea73-142">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2ea73-142">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2ea73-143">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea73-143">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
