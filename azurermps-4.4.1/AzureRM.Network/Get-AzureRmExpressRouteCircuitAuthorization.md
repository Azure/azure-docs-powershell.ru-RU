---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: a99b2ce5364e256f19069e1142b49abaf7f5e938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570076"
---
# <span data-ttu-id="2f6ab-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f6ab-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2f6ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6ab-103">Получение сведений об авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f6ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f6ab-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f6ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="2f6ab-106">Командлет **Get-AzureRmExpressRouteCircuitAuthorization** получает сведения о авторизациях, назначенных каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="2f6ab-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2f6ab-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="2f6ab-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="2f6ab-109">Ключи авторизации, а также другие сведения об авторизации можно просмотреть в любое время, выполнив **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="2f6ab-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f6ab-110">EXAMPLES</span></span>

### <span data-ttu-id="2f6ab-111">Пример 1: получение всех авторизаций ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2f6ab-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="2f6ab-112">Эти команды возвращают сведения обо всех параметрах авторизации ExpressRoute, связанных с цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="2f6ab-113">Первая команда использует командлет **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit; Ссылка на объект хранится в $Circuit переменной.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="2f6ab-114">Вторая команда использует ссылку на объект и командлет **Get-AzureRmExpressRouteCircuitAuthorization** для получения сведений об авторизации, связанных с ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="2f6ab-115">Пример 2: получение всех авторизаций ExpressRoute с помощью командлета Where-Object</span><span class="sxs-lookup"><span data-stu-id="2f6ab-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="2f6ab-116">Эти команды представляют собой вариант команд, используемых в примере 1.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="2f6ab-117">Однако в этом случае информация возвращается только для тех авторизаций, которые доступны для использования (то есть для авторизаций, которые не назначены виртуальной сети).</span><span class="sxs-lookup"><span data-stu-id="2f6ab-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="2f6ab-118">Для этого данные авторизации канала возвращаются в команде 2 и передаются в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="2f6ab-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="2f6ab-119">**Where-Object** затем выберет только те авторизации, для которых в свойстве *AuthorizationUseStatus* задано значение доступно.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="2f6ab-120">Чтобы вычислить только недоступные разрешения, используйте следующий синтаксис для предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="2f6ab-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f6ab-121">PARAMETERS</span></span>

### <span data-ttu-id="2f6ab-122">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f6ab-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2f6ab-123">Указывает для авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-123">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="2f6ab-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f6ab-124">-Name</span></span>
<span data-ttu-id="2f6ab-125">Указывает имя авторизации канала ExpressRoute, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-125">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="2f6ab-126">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="2f6ab-126">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="2f6ab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6ab-127">-DefaultProfile</span></span>
<span data-ttu-id="2f6ab-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f6ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6ab-129">CommonParameters</span></span>
<span data-ttu-id="2f6ab-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f6ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6ab-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f6ab-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6ab-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f6ab-132">INPUTS</span></span>

### <span data-ttu-id="2f6ab-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f6ab-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="2f6ab-134">**Get-AzureRmExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="2f6ab-134">**Get-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="2f6ab-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6ab-135">OUTPUTS</span></span>

### <span data-ttu-id="2f6ab-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f6ab-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="2f6ab-137">Функция **Get-AzureRmExpressRouteCircuitAuthorization** возвращает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="2f6ab-137">**Get-AzureRmExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="2f6ab-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f6ab-138">NOTES</span></span>

## <span data-ttu-id="2f6ab-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f6ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="2f6ab-140">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f6ab-140">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2f6ab-141">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f6ab-141">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2f6ab-142">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f6ab-142">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2f6ab-143">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2f6ab-143">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
