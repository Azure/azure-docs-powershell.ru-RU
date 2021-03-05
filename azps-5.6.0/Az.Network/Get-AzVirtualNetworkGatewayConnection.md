---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964259"
---
# <span data-ttu-id="2ed97-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ed97-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2ed97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed97-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed97-103">Получает виртуальное подключение к сетевому шлюзу</span><span class="sxs-lookup"><span data-stu-id="2ed97-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="2ed97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ed97-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed97-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ed97-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed97-106">Виртуальное подключение к сетевому шлюзу — это объект, представляющий туннель IPsec (Site-to-Site или Vnet-to-Vnet), подключенный к виртуальному сетевому шлюзу в Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed97-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2ed97-107">Командлет **Get-AzVirtualNetworkGatewayConnection** возвращает объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ed97-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="2ed97-108">Если **командлет Get-AzVirtualNetworkGatewayConnection** выдан без указания параметра -Name, выходные данные не будут выводиться в данных ConnectionStatus и SharedKey.</span><span class="sxs-lookup"><span data-stu-id="2ed97-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="2ed97-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ed97-109">EXAMPLES</span></span>

### <span data-ttu-id="2ed97-110">1. Подключение виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="2ed97-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="2ed97-111">Возвращает объект подключения виртуального сетевого шлюза с именем myTunnel в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="2ed97-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="2ed97-112">2. Получите все подключения виртуальных сетевых шлюзов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="2ed97-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="2ed97-113">Возвращает все подключения виртуальных сетевых шлюзов, которые начинаются с myTunnel в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="2ed97-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="2ed97-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ed97-114">PARAMETERS</span></span>

### <span data-ttu-id="2ed97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed97-115">-DefaultProfile</span></span>
<span data-ttu-id="2ed97-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed97-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed97-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2ed97-117">-Name</span></span>
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

### <span data-ttu-id="2ed97-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed97-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2ed97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed97-119">CommonParameters</span></span>
<span data-ttu-id="2ed97-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed97-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ed97-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed97-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ed97-122">INPUTS</span></span>

### <span data-ttu-id="2ed97-123">System.String</span><span class="sxs-lookup"><span data-stu-id="2ed97-123">System.String</span></span>

## <span data-ttu-id="2ed97-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ed97-124">OUTPUTS</span></span>

### <span data-ttu-id="2ed97-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ed97-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2ed97-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ed97-126">NOTES</span></span>

## <span data-ttu-id="2ed97-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ed97-127">RELATED LINKS</span></span>

[<span data-ttu-id="2ed97-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ed97-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ed97-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ed97-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ed97-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ed97-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
