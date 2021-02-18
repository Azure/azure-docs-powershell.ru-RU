---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223761"
---
# <span data-ttu-id="3b176-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3b176-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3b176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b176-102">SYNOPSIS</span></span>
<span data-ttu-id="3b176-103">Создает авторизацию каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b176-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="3b176-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b176-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b176-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b176-105">DESCRIPTION</span></span>
<span data-ttu-id="3b176-106">**Новый-AzExpressRouteCircuitAuthorization создает** авторизацию каналов, которую можно добавить в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b176-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="3b176-107">Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="3b176-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3b176-108">Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения сети к каналу.</span><span class="sxs-lookup"><span data-stu-id="3b176-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="3b176-109">В виртуальной сети может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="3b176-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="3b176-110">После создания схемы ExpressRoute вы можете добавить авторизацию в канал с помощью **Add-AzExpressRouteCircuitAuthorization.**</span><span class="sxs-lookup"><span data-stu-id="3b176-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="3b176-111">Кроме того, вы можете создать авторизацию, которую можно добавить в новый канал при создании схемы, с помощью **New-AzExpressRouteCircuitAuthorization.**</span><span class="sxs-lookup"><span data-stu-id="3b176-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="3b176-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b176-112">EXAMPLES</span></span>

### <span data-ttu-id="3b176-113">Пример 1. Создание авторизации каналов</span><span class="sxs-lookup"><span data-stu-id="3b176-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="3b176-114">Эта команда создает новый канал авторизации с именем ContosoCircuitAuthorization, а затем сохраняет этот объект в переменной $Authorization.</span><span class="sxs-lookup"><span data-stu-id="3b176-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="3b176-115">Важно сохранить объект в переменной: хотя **New-AzExpressRouteCircuitAuthorization** может создать авторизацию каналов, она не может добавить эту авторизацию в маршрут схемы.</span><span class="sxs-lookup"><span data-stu-id="3b176-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="3b176-116">Вместо этого переменная $Authorization используется New-AzExpressRouteCircuit при создании нового схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b176-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="3b176-117">Дополнительные сведения см. в документации New-AzExpressRouteCircuit управления проектами.</span><span class="sxs-lookup"><span data-stu-id="3b176-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="3b176-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b176-118">PARAMETERS</span></span>

### <span data-ttu-id="3b176-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b176-119">-DefaultProfile</span></span>
<span data-ttu-id="3b176-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b176-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b176-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3b176-121">-Name</span></span>
<span data-ttu-id="3b176-122">Указывает уникальное имя для новой авторизации каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3b176-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="3b176-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b176-123">CommonParameters</span></span>
<span data-ttu-id="3b176-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b176-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b176-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b176-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b176-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b176-126">INPUTS</span></span>

### <span data-ttu-id="3b176-127">Нет</span><span class="sxs-lookup"><span data-stu-id="3b176-127">None</span></span>

## <span data-ttu-id="3b176-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b176-128">OUTPUTS</span></span>

### <span data-ttu-id="3b176-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3b176-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3b176-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b176-130">NOTES</span></span>

## <span data-ttu-id="3b176-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b176-131">RELATED LINKS</span></span>

[<span data-ttu-id="3b176-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3b176-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3b176-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3b176-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3b176-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3b176-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

