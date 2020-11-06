---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a2c6c51a1f9f22130436e7d0a0d5fd888bccfb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562820"
---
# <span data-ttu-id="0d287-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0d287-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="0d287-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d287-102">SYNOPSIS</span></span>
<span data-ttu-id="0d287-103">Удаляет сайт по умолчанию из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d287-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d287-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d287-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d287-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d287-105">DESCRIPTION</span></span>
<span data-ttu-id="0d287-106">Командлет **Remove-AzureRmVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию для принудительного туннелирования из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0d287-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="0d287-107">Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.</span><span class="sxs-lookup"><span data-stu-id="0d287-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="0d287-108">Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.</span><span class="sxs-lookup"><span data-stu-id="0d287-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="0d287-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию, назначенный шлюзу.</span><span class="sxs-lookup"><span data-stu-id="0d287-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="0d287-110">Если вы это сделаете, вы должны использовать Set-AzureRmVirtualNetworkGatewayDefaultSite для назначения нового сайта по умолчанию, прежде чем шлюз можно будет использовать для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="0d287-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="0d287-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d287-111">EXAMPLES</span></span>

### <span data-ttu-id="0d287-112">Пример 1: удаление сайта по умолчанию, назначенного шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0d287-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="0d287-113">В этом примере удаляется сайт по умолчанию, который в данный момент назначен шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="0d287-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="0d287-114">Первая команда использует **Get-AzureRmVirtualNetworkGateway** для создания ссылки на объект Gateway. Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="0d287-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="0d287-115">Вторая команда использует команду **Remove-AzureRmVirtualNetworkGatewayDefaultSite** , чтобы удалить сайт по умолчанию, назначенный этому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="0d287-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="0d287-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d287-116">PARAMETERS</span></span>

### <span data-ttu-id="0d287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d287-117">-DefaultProfile</span></span>
<span data-ttu-id="0d287-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d287-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d287-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d287-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="0d287-120">Указывает ссылку на объект шлюза виртуальной сети, содержащего сайт по умолчанию, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0d287-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="0d287-121">Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="0d287-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="0d287-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d287-122">CommonParameters</span></span>
<span data-ttu-id="0d287-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d287-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d287-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d287-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d287-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d287-125">INPUTS</span></span>

### <span data-ttu-id="0d287-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d287-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="0d287-127">Параметры: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d287-127">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="0d287-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d287-128">OUTPUTS</span></span>

### <span data-ttu-id="0d287-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d287-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0d287-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d287-130">NOTES</span></span>

## <span data-ttu-id="0d287-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d287-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d287-132">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d287-132">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="0d287-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0d287-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


