---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227777"
---
# <span data-ttu-id="c1b6a-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="c1b6a-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="c1b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b6a-103">Списки маршрутов, усвоеных виртуальным сетевым шлюзом Azure</span><span class="sxs-lookup"><span data-stu-id="c1b6a-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="c1b6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1b6a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b6a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b6a-106">Продумывка маршрутов, усвоеных виртуальным сетевым шлюзом Azure, из различных источников.</span><span class="sxs-lookup"><span data-stu-id="c1b6a-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="c1b6a-107">К ним относятся маршруты, отучимся через BGP, а также статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="c1b6a-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="c1b6a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1b6a-108">EXAMPLES</span></span>

### <span data-ttu-id="c1b6a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1b6a-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="c1b6a-110">Для виртуального сетевого шлюза Azure с именем шлюза в группе ресурсов resourceGroup извлекает маршруты, известные шлюзу Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b6a-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="c1b6a-111">В данном случае виртуальный сетевой шлюз Azure имеет два статических маршрута (10.1.0.0/16 и 10.0.0.254/32), а также один маршрут, обученный через BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="c1b6a-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="c1b6a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1b6a-112">PARAMETERS</span></span>

### <span data-ttu-id="c1b6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b6a-113">-AsJob</span></span>
<span data-ttu-id="c1b6a-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c1b6a-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b6a-115">-DefaultProfile</span></span>
<span data-ttu-id="c1b6a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b6a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b6a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1b6a-118">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="c1b6a-118">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b6a-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c1b6a-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c1b6a-120">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="c1b6a-120">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b6a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b6a-121">CommonParameters</span></span>
<span data-ttu-id="c1b6a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b6a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b6a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1b6a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b6a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1b6a-124">INPUTS</span></span>

### <span data-ttu-id="c1b6a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c1b6a-125">System.String</span></span>

## <span data-ttu-id="c1b6a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1b6a-126">OUTPUTS</span></span>

### <span data-ttu-id="c1b6a-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="c1b6a-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="c1b6a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1b6a-128">NOTES</span></span>

## <span data-ttu-id="c1b6a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1b6a-129">RELATED LINKS</span></span>
