---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909998"
---
# <span data-ttu-id="2f240-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f240-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2f240-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f240-102">SYNOPSIS</span></span>
<span data-ttu-id="2f240-103">Получение сведений об авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f240-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="2f240-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f240-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f240-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f240-105">DESCRIPTION</span></span>
<span data-ttu-id="2f240-106">Командлет **Get-AzExpressRouteCircuitAuthorization** получает сведения о авторизациях, назначенных каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f240-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="2f240-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="2f240-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2f240-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="2f240-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="2f240-109">Ключи авторизации, а также другие сведения об авторизации можно просмотреть в любое время, выполнив **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="2f240-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="2f240-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f240-110">EXAMPLES</span></span>

### <span data-ttu-id="2f240-111">Пример 1: получение всех авторизаций ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2f240-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="2f240-112">Эти команды возвращают сведения обо всех параметрах авторизации ExpressRoute, связанных с цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f240-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="2f240-113">Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit; Ссылка на объект хранится в $Circuit переменной.</span><span class="sxs-lookup"><span data-stu-id="2f240-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="2f240-114">Вторая команда использует ссылку на объект и командлет **Get-AzExpressRouteCircuitAuthorization** для получения сведений об авторизации, связанных с ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="2f240-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="2f240-115">Пример 2: получение всех авторизаций ExpressRoute с помощью командлета Where-Object</span><span class="sxs-lookup"><span data-stu-id="2f240-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="2f240-116">Эти команды представляют собой вариант команд, используемых в примере 1.</span><span class="sxs-lookup"><span data-stu-id="2f240-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="2f240-117">Однако в этом случае информация возвращается только для тех авторизаций, которые доступны для использования (то есть для авторизаций, которые не назначены виртуальной сети).</span><span class="sxs-lookup"><span data-stu-id="2f240-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="2f240-118">Для этого данные авторизации канала возвращаются в команде 2 и передаются в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="2f240-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="2f240-119">**Where-Object** затем выберет только те авторизации, для которых в свойстве *AuthorizationUseStatus* задано значение доступно.</span><span class="sxs-lookup"><span data-stu-id="2f240-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="2f240-120">Чтобы вычислить только недоступные разрешения, используйте следующий синтаксис для предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="2f240-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="2f240-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f240-121">PARAMETERS</span></span>

### <span data-ttu-id="2f240-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f240-122">-DefaultProfile</span></span>
<span data-ttu-id="2f240-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f240-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f240-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f240-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2f240-125">Указывает для авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f240-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="2f240-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f240-126">-Name</span></span>
<span data-ttu-id="2f240-127">Указывает имя авторизации канала ExpressRoute, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f240-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="2f240-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="2f240-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="2f240-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f240-129">CommonParameters</span></span>
<span data-ttu-id="2f240-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f240-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f240-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f240-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f240-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f240-132">INPUTS</span></span>

### <span data-ttu-id="2f240-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f240-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2f240-134">**Get-AzExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2f240-134">**Get-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2f240-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f240-135">OUTPUTS</span></span>

### <span data-ttu-id="2f240-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f240-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="2f240-137">Функция **Get-AzExpressRouteCircuitAuthorization** возвращает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="2f240-137">**Get-AzExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="2f240-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f240-138">NOTES</span></span>

## <span data-ttu-id="2f240-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f240-139">RELATED LINKS</span></span>

[<span data-ttu-id="2f240-140">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f240-140">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2f240-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f240-141">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f240-142">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f240-142">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2f240-143">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f240-143">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
