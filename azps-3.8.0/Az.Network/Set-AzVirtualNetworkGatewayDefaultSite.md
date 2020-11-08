---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065129"
---
# <span data-ttu-id="384c2-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="384c2-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="384c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="384c2-102">SYNOPSIS</span></span>
<span data-ttu-id="384c2-103">Задает сайт по умолчанию для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="384c2-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="384c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="384c2-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="384c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="384c2-105">DESCRIPTION</span></span>
<span data-ttu-id="384c2-106">Командлет **Set-AzVirtualNetworkGatewayDefaultSite** назначает сайт по умолчанию для виртуального сетевого шлюза с принудительным туннелированием.</span><span class="sxs-lookup"><span data-stu-id="384c2-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="384c2-107">Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.</span><span class="sxs-lookup"><span data-stu-id="384c2-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="384c2-108">Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.</span><span class="sxs-lookup"><span data-stu-id="384c2-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="384c2-109">**Set-AzVirtualNetworkGatewayDefaultSite** предоставляет способ изменения сайта по умолчанию, назначенного шлюзом.</span><span class="sxs-lookup"><span data-stu-id="384c2-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="384c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="384c2-110">EXAMPLES</span></span>

### <span data-ttu-id="384c2-111">Пример 1: назначение сайта по умолчанию шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="384c2-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="384c2-112">В этом примере сайт по умолчанию назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="384c2-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="384c2-113">Первая команда создает ссылку на объект на локальный шлюз с именем ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="384c2-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="384c2-114">Эта ссылка на объект, хранящаяся в переменной с именем $LocalGateway, представляет шлюз для настройки в качестве сайта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="384c2-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="384c2-115">Вторая команда создает ссылку на объект для шлюза виртуальной сети и сохраняет результат в переменной с именем $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="384c2-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="384c2-116">Третья команда использует командлет **Set-AzVirtualNetworkGatewayDefaultSite** , чтобы назначить сайт по умолчанию ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="384c2-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="384c2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="384c2-117">PARAMETERS</span></span>

### <span data-ttu-id="384c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384c2-118">-DefaultProfile</span></span>
<span data-ttu-id="384c2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="384c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384c2-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="384c2-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="384c2-121">Указывает ссылку на объект для шлюза локальной сети, назначаемого в качестве сайта по умолчанию для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="384c2-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="384c2-122">Вы можете использовать командлет Get-AzLocalNetworkGateway для создания ссылки на объект на локальный шлюз.</span><span class="sxs-lookup"><span data-stu-id="384c2-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="384c2-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="384c2-124">Указывает ссылку на объект шлюза виртуальной сети, на котором будет назначен сайт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="384c2-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="384c2-125">Вы можете создать ссылку на объект для шлюза виртуальной сети с помощью **Get-AzVirtualNetworkGateway** и указать имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="384c2-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="384c2-126">Переменную $VirtualGateway можно использовать в качестве значения параметра для параметра *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="384c2-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="384c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384c2-127">CommonParameters</span></span>
<span data-ttu-id="384c2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="384c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384c2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384c2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384c2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="384c2-130">INPUTS</span></span>

### <span data-ttu-id="384c2-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="384c2-132">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="384c2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="384c2-133">OUTPUTS</span></span>

### <span data-ttu-id="384c2-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="384c2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="384c2-135">NOTES</span></span>

## <span data-ttu-id="384c2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="384c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="384c2-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="384c2-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="384c2-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="384c2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="384c2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


