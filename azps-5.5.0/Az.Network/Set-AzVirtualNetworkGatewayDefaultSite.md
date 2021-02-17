---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225665"
---
# <span data-ttu-id="d3adf-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d3adf-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="d3adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d3adf-103">Задает сайт по умолчанию для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="d3adf-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="d3adf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3adf-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3adf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3adf-105">DESCRIPTION</span></span>
<span data-ttu-id="d3adf-106">Командлет **Set-AzVirtualNetworkGatewayDefaultSite** назначает сайт по умолчанию для принудительных туннелов виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="d3adf-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="d3adf-107">Принудительный туннелинг позволяет перенаправлять интернет-трафик с виртуальных машин Azure в вашу локальное сеть; это позволяет проверять и проверять трафик до его выпуска.</span><span class="sxs-lookup"><span data-stu-id="d3adf-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="d3adf-108">Принудительный туннелинг осуществляется с помощью VPN-туннель. для этого туннель требуется сайт по умолчанию — локальный шлюз, в котором перенаправляется весь интернет-трафик Azure.</span><span class="sxs-lookup"><span data-stu-id="d3adf-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="d3adf-109">**Сайт Set-AzVirtualNetworkGatewayDefaultSite** позволяет изменить сайт по умолчанию, присвоенный шлюзу.</span><span class="sxs-lookup"><span data-stu-id="d3adf-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="d3adf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3adf-110">EXAMPLES</span></span>

### <span data-ttu-id="d3adf-111">Пример 1. Назначение сайта по умолчанию виртуальному сетевому шлюзу</span><span class="sxs-lookup"><span data-stu-id="d3adf-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="d3adf-112">В этом примере сайт по умолчанию назначается виртуальному сетевому шлюзу с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="d3adf-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="d3adf-113">Первая команда создает ссылку на локальный шлюз ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="d3adf-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="d3adf-114">Эта ссылка на объект, которая хранится в переменной с именем $LocalGateway представляет шлюз, который нужно настроить как сайт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3adf-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="d3adf-115">Вторая команда затем создает ссылку на объект на виртуальный сетевой шлюз и сохраняет результат в переменной с $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="d3adf-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="d3adf-116">Третья команда использует командлет **Set-AzVirtualNetworkGatewayDefaultSite,** чтобы назначить сайту ContosoVirtualGateway по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3adf-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="d3adf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3adf-117">PARAMETERS</span></span>

### <span data-ttu-id="d3adf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3adf-118">-DefaultProfile</span></span>
<span data-ttu-id="d3adf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3adf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3adf-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d3adf-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="d3adf-121">Указывает ссылку на объект на локальный сетевой шлюз, который должен быть назначен в качестве сайта по умолчанию для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d3adf-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="d3adf-122">С помощью Get-AzLocalNetworkGateway можно создать ссылку на локальный шлюз.</span><span class="sxs-lookup"><span data-stu-id="d3adf-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3adf-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d3adf-124">Указывает ссылку на виртуальный сетевой шлюз, для которой будет назначен сайт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3adf-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="d3adf-125">Вы можете создать ссылку на виртуальный сетевой шлюз с помощью **Get-AzVirtualNetworkGateway** и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="d3adf-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="d3adf-126">Переменную $VirtualGateway затем можно использовать в качестве значения параметра *параметра VirtualNetworkGateway:*</span><span class="sxs-lookup"><span data-stu-id="d3adf-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3adf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3adf-127">CommonParameters</span></span>
<span data-ttu-id="d3adf-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3adf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3adf-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3adf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3adf-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3adf-130">INPUTS</span></span>

### <span data-ttu-id="d3adf-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d3adf-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="d3adf-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3adf-133">OUTPUTS</span></span>

### <span data-ttu-id="d3adf-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d3adf-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3adf-135">NOTES</span></span>

## <span data-ttu-id="d3adf-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3adf-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3adf-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="d3adf-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d3adf-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d3adf-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d3adf-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


