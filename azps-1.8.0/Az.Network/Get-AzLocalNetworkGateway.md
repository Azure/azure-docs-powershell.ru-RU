---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 04cec0db46eef985819ea44355b9bbedf792dbf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730544"
---
# <span data-ttu-id="f80b6-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f80b6-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f80b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f80b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f80b6-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="f80b6-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="f80b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f80b6-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f80b6-105">DESCRIPTION</span></span>
<span data-ttu-id="f80b6-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="f80b6-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f80b6-107">Командлет **Get-AzLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f80b6-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f80b6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f80b6-108">EXAMPLES</span></span>

### <span data-ttu-id="f80b6-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="f80b6-109">1: Get a Local Network Gateway</span></span>
```
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

<span data-ttu-id="f80b6-110">Возвращает объект шлюза локальной сети с именем "myLocalGW1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="f80b6-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="f80b6-111">2. получение локальных сетевых шлюзов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="f80b6-111">2: Get Local Network Gateways using filtering</span></span>
```
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

<span data-ttu-id="f80b6-112">Возвращает объект шлюза локальной сети с именем, начинающимся с "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="f80b6-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="f80b6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f80b6-113">PARAMETERS</span></span>

### <span data-ttu-id="f80b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80b6-114">-DefaultProfile</span></span>
<span data-ttu-id="f80b6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f80b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f80b6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f80b6-116">-Name</span></span>
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

### <span data-ttu-id="f80b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80b6-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f80b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80b6-118">CommonParameters</span></span>
<span data-ttu-id="f80b6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f80b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80b6-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f80b6-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80b6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f80b6-121">INPUTS</span></span>

### <span data-ttu-id="f80b6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f80b6-122">System.String</span></span>

## <span data-ttu-id="f80b6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f80b6-123">OUTPUTS</span></span>

### <span data-ttu-id="f80b6-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f80b6-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f80b6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f80b6-125">NOTES</span></span>

## <span data-ttu-id="f80b6-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f80b6-126">RELATED LINKS</span></span>

[<span data-ttu-id="f80b6-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f80b6-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="f80b6-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f80b6-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="f80b6-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f80b6-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
