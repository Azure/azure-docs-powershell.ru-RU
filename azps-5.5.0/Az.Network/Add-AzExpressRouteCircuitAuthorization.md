---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228044"
---
# <span data-ttu-id="99726-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="99726-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="99726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99726-102">SYNOPSIS</span></span>
<span data-ttu-id="99726-103">Добавляет авторизацию каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="99726-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="99726-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99726-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99726-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99726-105">DESCRIPTION</span></span>
<span data-ttu-id="99726-106">Cmdlet **Add-AzExpressRouteCircuitAuthorization добавляет** авторизацию в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="99726-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="99726-107">Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="99726-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="99726-108">Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения своей сети к каналу (по одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="99726-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="99726-109">**Add-AzExpressRouteCircuitAuthorization** добавляет новую авторизацию в канал и одновременно создает соответствующий ключ авторизации.</span><span class="sxs-lookup"><span data-stu-id="99726-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="99726-110">Эти ключи можно просмотреть в любое время с помощью Get-AzExpressRouteCircuitAuthorization- и при необходимости скопировать и перена вперед для соответствующего владельца сети.</span><span class="sxs-lookup"><span data-stu-id="99726-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="99726-111">Обратите внимание, что после запуска **Add-AzExpressRouteCircuitAuthorization** необходимо вызвать Set-AzExpressRouteCircuit для активации ключа.</span><span class="sxs-lookup"><span data-stu-id="99726-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="99726-112">Если вы не позвоните **в Set-AzExpressRouteCircuit,** авторизация будет добавлена в канал, но не будет включена для использования.</span><span class="sxs-lookup"><span data-stu-id="99726-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="99726-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99726-113">EXAMPLES</span></span>

### <span data-ttu-id="99726-114">Пример 1. Добавление авторизации в указанный канал ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="99726-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="99726-115">Команды в этом примере добавляют новую авторизацию в существующий канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="99726-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="99726-116">Первая команда использует **Get-AzExpressRouteCircuit** для создания ссылки на объект в канал ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="99726-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="99726-117">Эта ссылка на объект хранится в переменной с именем $Circuit.</span><span class="sxs-lookup"><span data-stu-id="99726-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="99726-118">Во второй команде командлет **Add-AzExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="99726-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="99726-119">Эта команда добавляет авторизацию, но не активирует ее.</span><span class="sxs-lookup"><span data-stu-id="99726-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="99726-120">Для активации авторизации требуется **Set-AzExpressRouteCircuit,** показанный в последней команде в примере.</span><span class="sxs-lookup"><span data-stu-id="99726-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="99726-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99726-121">PARAMETERS</span></span>

### <span data-ttu-id="99726-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99726-122">-DefaultProfile</span></span>
<span data-ttu-id="99726-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99726-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99726-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99726-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="99726-125">Определяет канал ExpressRoute, в который этот cmdlet добавляет авторизацию.</span><span class="sxs-lookup"><span data-stu-id="99726-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="99726-126">-Name</span><span class="sxs-lookup"><span data-stu-id="99726-126">-Name</span></span>
<span data-ttu-id="99726-127">Указывает имя добавляемой авторизации каналов.</span><span class="sxs-lookup"><span data-stu-id="99726-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="99726-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99726-128">CommonParameters</span></span>
<span data-ttu-id="99726-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99726-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99726-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99726-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99726-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99726-131">INPUTS</span></span>

### <span data-ttu-id="99726-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99726-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="99726-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99726-133">OUTPUTS</span></span>

### <span data-ttu-id="99726-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99726-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="99726-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99726-135">NOTES</span></span>

## <span data-ttu-id="99726-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99726-136">RELATED LINKS</span></span>

[<span data-ttu-id="99726-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99726-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="99726-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="99726-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="99726-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="99726-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="99726-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="99726-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="99726-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="99726-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
