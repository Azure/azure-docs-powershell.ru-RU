---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078861"
---
# <span data-ttu-id="2817a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2817a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="2817a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2817a-102">SYNOPSIS</span></span>
<span data-ttu-id="2817a-103">Удаляет сайт по умолчанию из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2817a-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="2817a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2817a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2817a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2817a-105">DESCRIPTION</span></span>
<span data-ttu-id="2817a-106">Командлет **Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию для принудительного туннелирования из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="2817a-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="2817a-107">Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.</span><span class="sxs-lookup"><span data-stu-id="2817a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="2817a-108">Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.</span><span class="sxs-lookup"><span data-stu-id="2817a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="2817a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию, назначенный шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2817a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="2817a-110">Если вы это сделаете, вы должны использовать Set-AzVirtualNetworkGatewayDefaultSite для назначения нового сайта по умолчанию, прежде чем шлюз можно будет использовать для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="2817a-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="2817a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2817a-111">EXAMPLES</span></span>

### <span data-ttu-id="2817a-112">Пример 1: удаление сайта по умолчанию, назначенного шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2817a-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="2817a-113">В этом примере удаляется сайт по умолчанию, который в данный момент назначен шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2817a-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="2817a-114">Первая команда использует **Get-AzVirtualNetworkGateway** для создания ссылки на объект Gateway. Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2817a-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="2817a-115">Вторая команда использует команду **Remove-AzVirtualNetworkGatewayDefaultSite** , чтобы удалить сайт по умолчанию, назначенный этому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2817a-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="2817a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2817a-116">PARAMETERS</span></span>

### <span data-ttu-id="2817a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2817a-117">-DefaultProfile</span></span>
<span data-ttu-id="2817a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2817a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2817a-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2817a-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2817a-120">Указывает ссылку на объект шлюза виртуальной сети, содержащего сайт по умолчанию, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2817a-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="2817a-121">Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="2817a-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="2817a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2817a-122">CommonParameters</span></span>
<span data-ttu-id="2817a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2817a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2817a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2817a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2817a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2817a-125">INPUTS</span></span>

### <span data-ttu-id="2817a-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2817a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2817a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2817a-127">OUTPUTS</span></span>

### <span data-ttu-id="2817a-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2817a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2817a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="2817a-129">NOTES</span></span>

## <span data-ttu-id="2817a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2817a-130">RELATED LINKS</span></span>

[<span data-ttu-id="2817a-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2817a-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2817a-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2817a-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


