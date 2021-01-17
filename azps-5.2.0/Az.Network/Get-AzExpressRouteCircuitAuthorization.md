---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323781"
---
# <span data-ttu-id="4879a-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4879a-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4879a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4879a-102">SYNOPSIS</span></span>
<span data-ttu-id="4879a-103">Сведения о авторизации каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4879a-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="4879a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4879a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4879a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4879a-105">DESCRIPTION</span></span>
<span data-ttu-id="4879a-106">Cmdlet **Get-AzExpressRouteCircuitAuthorization получает** сведения о разрешениях, которые назначены каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4879a-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="4879a-107">Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="4879a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4879a-108">Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения своей сети к каналу (по одной авторизации на виртуальную сеть).</span><span class="sxs-lookup"><span data-stu-id="4879a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="4879a-109">Ключи авторизации, а также другие сведения о авторизации можно просмотреть в любое время с помощью **get-AzExpressRouteCircuitAuthorization.**</span><span class="sxs-lookup"><span data-stu-id="4879a-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="4879a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4879a-110">EXAMPLES</span></span>

### <span data-ttu-id="4879a-111">Пример 1. Получить все авторизации ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4879a-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="4879a-112">Эти команды возвращают сведения обо всех авторизациях ExpressRoute, связанных с каналом ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4879a-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="4879a-113">Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале ContosoCircuit; эта ссылка на объект хранится в переменной $Circuit.</span><span class="sxs-lookup"><span data-stu-id="4879a-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="4879a-114">Затем вторая команда использует эту ссылку на объект и командлет **Get-AzExpressRouteCircuitAuthorization** для возврата сведений о разрешениях, связанных с ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="4879a-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="4879a-115">Пример 2. Получить все авторизацию ExpressRoute с Where-Object-управления</span><span class="sxs-lookup"><span data-stu-id="4879a-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="4879a-116">Эти команды представляют собой вариант команд, используемых в примере 1.</span><span class="sxs-lookup"><span data-stu-id="4879a-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="4879a-117">Однако в этом случае сведения возвращаются только для тех авторов, которые доступны для использования (то есть для авторизации, не назначенной виртуальной сети).</span><span class="sxs-lookup"><span data-stu-id="4879a-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="4879a-118">Для этого сведения о авторизации канала возвращаются в команде 2 и сдаются **командлету Where-Object** по каналу.</span><span class="sxs-lookup"><span data-stu-id="4879a-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="4879a-119">**Затем Where-Object** выбирает только те авторизации, для которых свойство *AuthorizationUseStatus* имеет разрешение Available.</span><span class="sxs-lookup"><span data-stu-id="4879a-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="4879a-120">Чтобы перечислить только те авторизации, которые недоступны, используйте такой синтаксис для предложения Where: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="4879a-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="4879a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4879a-121">PARAMETERS</span></span>

### <span data-ttu-id="4879a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4879a-122">-DefaultProfile</span></span>
<span data-ttu-id="4879a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4879a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4879a-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4879a-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4879a-125">Определяет авторизацию каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4879a-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="4879a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4879a-126">-Name</span></span>
<span data-ttu-id="4879a-127">Указывает имя авторизации каналов ExpressRoute, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4879a-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="4879a-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="4879a-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="4879a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4879a-129">CommonParameters</span></span>
<span data-ttu-id="4879a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4879a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4879a-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4879a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4879a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4879a-132">INPUTS</span></span>

### <span data-ttu-id="4879a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4879a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4879a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4879a-134">OUTPUTS</span></span>

### <span data-ttu-id="4879a-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4879a-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4879a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4879a-136">NOTES</span></span>

## <span data-ttu-id="4879a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4879a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4879a-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4879a-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4879a-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4879a-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4879a-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4879a-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4879a-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4879a-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
