---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519940"
---
# <span data-ttu-id="369f7-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="369f7-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="369f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369f7-102">SYNOPSIS</span></span>
<span data-ttu-id="369f7-103">Удаляет сайт по умолчанию из виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="369f7-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="369f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="369f7-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="369f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="369f7-105">DESCRIPTION</span></span>
<span data-ttu-id="369f7-106">Командлет **Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию для принудительного туннелизации из виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="369f7-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="369f7-107">Принудительный туннелинг позволяет перенаправлять интернет-трафик с виртуальных машин Azure в вашу локальное сеть; это позволяет проверять и проверять трафик до его выпуска.</span><span class="sxs-lookup"><span data-stu-id="369f7-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="369f7-108">Принудительный туннелинг осуществляется с помощью VPN-туннель. для этого туннель требуется сайт по умолчанию — локальный шлюз, в котором перенаправляется весь интернет-трафик Azure.</span><span class="sxs-lookup"><span data-stu-id="369f7-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="369f7-109">**Сайт Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию, присвоенный шлюзу.</span><span class="sxs-lookup"><span data-stu-id="369f7-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="369f7-110">Для этого потребуется использовать Set-AzVirtualNetworkGatewayDefaultSite для назначения нового сайта по умолчанию, прежде чем шлюз можно будет использовать для принудительных туннелов.</span><span class="sxs-lookup"><span data-stu-id="369f7-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="369f7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="369f7-111">EXAMPLES</span></span>

### <span data-ttu-id="369f7-112">Пример 1. Удаление сайта по умолчанию, назначенного виртуальному сетевому шлюзу</span><span class="sxs-lookup"><span data-stu-id="369f7-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="369f7-113">В этом примере удаляется сайт по умолчанию, который в настоящее время назначен виртуальному сетевому шлюзу с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="369f7-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="369f7-114">Первая команда использует **Get-AzVirtualNetworkGateway** для создания ссылки на шлюз; эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="369f7-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="369f7-115">Затем вторая команда использует **Remove-AzVirtualNetworkGatewayDefaultSite** для удаления сайта по умолчанию, назначенного этому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="369f7-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="369f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="369f7-116">PARAMETERS</span></span>

### <span data-ttu-id="369f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369f7-117">-DefaultProfile</span></span>
<span data-ttu-id="369f7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="369f7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="369f7-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="369f7-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="369f7-120">Указывает ссылку на виртуальный сетевой шлюз, содержащий удаляемый сайт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="369f7-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="369f7-121">Вы можете создать ссылку на виртуальный сетевой шлюз, используя Get-AzVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="369f7-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="369f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369f7-122">CommonParameters</span></span>
<span data-ttu-id="369f7-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="369f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369f7-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369f7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369f7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="369f7-125">INPUTS</span></span>

### <span data-ttu-id="369f7-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="369f7-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="369f7-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="369f7-127">OUTPUTS</span></span>

### <span data-ttu-id="369f7-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="369f7-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="369f7-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="369f7-129">NOTES</span></span>

## <span data-ttu-id="369f7-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="369f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="369f7-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="369f7-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="369f7-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="369f7-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


