---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422247"
---
# <span data-ttu-id="7beb1-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7beb1-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="7beb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7beb1-102">SYNOPSIS</span></span>
<span data-ttu-id="7beb1-103">Получает локальный сетевой шлюз</span><span class="sxs-lookup"><span data-stu-id="7beb1-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="7beb1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7beb1-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7beb1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7beb1-105">DESCRIPTION</span></span>
<span data-ttu-id="7beb1-106">Локальный сетевой шлюз — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="7beb1-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="7beb1-107">Командлет **Get-AzLocalNetworkGateway** возвращает объект, представляющий ваш собственный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7beb1-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7beb1-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7beb1-108">EXAMPLES</span></span>

### <span data-ttu-id="7beb1-109">Пример 1. Получить локальный сетевой шлюз</span><span class="sxs-lookup"><span data-stu-id="7beb1-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="7beb1-110">Возвращает объект локального сетевого шлюза с именем myLocalGW1 в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="7beb1-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="7beb1-111">Пример 2. Получить локальные сетевые шлюзы с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7beb1-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="7beb1-112">Возвращает объект локального сетевого шлюза, имя которого начинается с myLocalGW в группе ресурсов MyRG.</span><span class="sxs-lookup"><span data-stu-id="7beb1-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="7beb1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7beb1-113">PARAMETERS</span></span>

### <span data-ttu-id="7beb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7beb1-114">-DefaultProfile</span></span>
<span data-ttu-id="7beb1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7beb1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7beb1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7beb1-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7beb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7beb1-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7beb1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7beb1-118">CommonParameters</span></span>
<span data-ttu-id="7beb1-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7beb1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7beb1-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7beb1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7beb1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7beb1-121">INPUTS</span></span>

### <span data-ttu-id="7beb1-122">System.String</span><span class="sxs-lookup"><span data-stu-id="7beb1-122">System.String</span></span>

## <span data-ttu-id="7beb1-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7beb1-123">OUTPUTS</span></span>

### <span data-ttu-id="7beb1-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7beb1-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="7beb1-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7beb1-125">NOTES</span></span>

## <span data-ttu-id="7beb1-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7beb1-126">RELATED LINKS</span></span>

[<span data-ttu-id="7beb1-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7beb1-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="7beb1-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7beb1-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="7beb1-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7beb1-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
