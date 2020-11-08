---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248543"
---
# <span data-ttu-id="26ea6-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="26ea6-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="26ea6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="26ea6-103">Создание авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="26ea6-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="26ea6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26ea6-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26ea6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="26ea6-106">Командлет **New-AzExpressRouteCircuitAuthorization** создает разрешение на канал, которое можно добавить в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="26ea6-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="26ea6-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="26ea6-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="26ea6-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ проверки подлинности, который может использоваться владельцем виртуальной сети для подключения к каналу сети.</span><span class="sxs-lookup"><span data-stu-id="26ea6-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="26ea6-109">На виртуальную сеть может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="26ea6-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="26ea6-110">После того как вы создадите цепь ExpressRoute, вы можете использовать **Add-AzExpressRouteCircuitAuthorization** , чтобы добавить авторизацию для этого канала.</span><span class="sxs-lookup"><span data-stu-id="26ea6-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="26ea6-111">Кроме того, вы можете использовать **New-AzExpressRouteCircuitAuthorization** для создания авторизации, которая может быть добавлена в новую цепь одновременно с созданием канала.</span><span class="sxs-lookup"><span data-stu-id="26ea6-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="26ea6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26ea6-112">EXAMPLES</span></span>

### <span data-ttu-id="26ea6-113">Пример 1: создание авторизации новой цепи</span><span class="sxs-lookup"><span data-stu-id="26ea6-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="26ea6-114">Эта команда создает новое разрешение на канал с именем ContosoCircuitAuthorization и сохраняет этот объект в переменной с именем $Authorization.</span><span class="sxs-lookup"><span data-stu-id="26ea6-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="26ea6-115">Сохранение объекта в переменной играет важную роль: Несмотря на то, что **New-AzExpressRouteCircuitAuthorization** может создавать полномочия на канал, он не может добавить эту авторизацию в маршрут цепи.</span><span class="sxs-lookup"><span data-stu-id="26ea6-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="26ea6-116">Вместо этого переменная $Authorization используется New-AzExpressRouteCircuit при создании новой цепи ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="26ea6-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="26ea6-117">Дополнительные сведения можно найти в документации по командлету New-AzExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="26ea6-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="26ea6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26ea6-118">PARAMETERS</span></span>

### <span data-ttu-id="26ea6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ea6-119">-DefaultProfile</span></span>
<span data-ttu-id="26ea6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26ea6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26ea6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26ea6-121">-Name</span></span>
<span data-ttu-id="26ea6-122">Указывает уникальное имя для новой авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="26ea6-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="26ea6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ea6-123">CommonParameters</span></span>
<span data-ttu-id="26ea6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26ea6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ea6-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ea6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ea6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26ea6-126">INPUTS</span></span>

### <span data-ttu-id="26ea6-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="26ea6-127">None</span></span>

## <span data-ttu-id="26ea6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ea6-128">OUTPUTS</span></span>

### <span data-ttu-id="26ea6-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="26ea6-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="26ea6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="26ea6-130">NOTES</span></span>

## <span data-ttu-id="26ea6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26ea6-131">RELATED LINKS</span></span>

[<span data-ttu-id="26ea6-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="26ea6-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="26ea6-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="26ea6-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="26ea6-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="26ea6-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

