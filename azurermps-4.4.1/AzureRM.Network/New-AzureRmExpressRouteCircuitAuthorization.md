---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734043"
---
# <span data-ttu-id="6157b-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6157b-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="6157b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6157b-102">SYNOPSIS</span></span>
<span data-ttu-id="6157b-103">Создание авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6157b-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6157b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6157b-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6157b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6157b-105">DESCRIPTION</span></span>
<span data-ttu-id="6157b-106">Командлет **New-AzureRmExpressRouteCircuitAuthorization** создает разрешение на канал, которое можно добавить в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6157b-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="6157b-107">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="6157b-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="6157b-108">Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ проверки подлинности, который может использоваться владельцем виртуальной сети для подключения к каналу сети.</span><span class="sxs-lookup"><span data-stu-id="6157b-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="6157b-109">На виртуальную сеть может быть только одна авторизация.</span><span class="sxs-lookup"><span data-stu-id="6157b-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="6157b-110">После того как вы создадите цепь ExpressRoute, вы можете использовать **Add-AzureRmExpressRouteCircuitAuthorization** , чтобы добавить авторизацию для этого канала.</span><span class="sxs-lookup"><span data-stu-id="6157b-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="6157b-111">Кроме того, вы можете использовать **New-AzureRmExpressRouteCircuitAuthorization** для создания авторизации, которая может быть добавлена в новую цепь одновременно с созданием канала.</span><span class="sxs-lookup"><span data-stu-id="6157b-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="6157b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6157b-112">EXAMPLES</span></span>

### <span data-ttu-id="6157b-113">Пример 1: создание авторизации новой цепи</span><span class="sxs-lookup"><span data-stu-id="6157b-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="6157b-114">Эта команда создает новое разрешение на канал с именем ContosoCircuitAuthorization и сохраняет этот объект в переменной с именем $Authorization.</span><span class="sxs-lookup"><span data-stu-id="6157b-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="6157b-115">Сохранение объекта в переменной играет важную роль: Несмотря на то, что **New-AzureRmExpressRouteCircuitAuthorization** может создавать полномочия на канал, он не может добавить эту авторизацию в маршрут цепи.</span><span class="sxs-lookup"><span data-stu-id="6157b-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="6157b-116">Вместо этого переменная $Authorization используется New-AzureRmExpressRouteCircuit при создании новой цепи ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6157b-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="6157b-117">Дополнительные сведения можно найти в документации по командлету New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="6157b-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="6157b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6157b-118">PARAMETERS</span></span>

### <span data-ttu-id="6157b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6157b-119">-Name</span></span>
<span data-ttu-id="6157b-120">Указывает уникальное имя для новой авторизации канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6157b-120">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="6157b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6157b-121">-DefaultProfile</span></span>
<span data-ttu-id="6157b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6157b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6157b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6157b-123">CommonParameters</span></span>
<span data-ttu-id="6157b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6157b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6157b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6157b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6157b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6157b-126">INPUTS</span></span>

### <span data-ttu-id="6157b-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6157b-127">None</span></span>
<span data-ttu-id="6157b-128">Этот командлет не поддерживает конвейерный вход.</span><span class="sxs-lookup"><span data-stu-id="6157b-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="6157b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6157b-129">OUTPUTS</span></span>

### <span data-ttu-id="6157b-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6157b-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="6157b-131">Этот командлет создает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="6157b-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="6157b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6157b-132">NOTES</span></span>

## <span data-ttu-id="6157b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6157b-133">RELATED LINKS</span></span>

[<span data-ttu-id="6157b-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6157b-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6157b-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6157b-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6157b-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6157b-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

