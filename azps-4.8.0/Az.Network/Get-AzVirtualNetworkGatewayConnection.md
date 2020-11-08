---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235501"
---
# <span data-ttu-id="327e1-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="327e1-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="327e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="327e1-102">SYNOPSIS</span></span>
<span data-ttu-id="327e1-103">Возвращает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="327e1-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="327e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="327e1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="327e1-105">DESCRIPTION</span></span>
<span data-ttu-id="327e1-106">Подключение к шлюзу виртуальной сети является объектом, представляющим туннель IPsec ("сайт-сайт" или "Виртуальная сеть-сеть"), подключенного к шлюзу виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="327e1-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="327e1-107">Командлет **Get-AzVirtualNetworkGatewayConnection** возвращает объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="327e1-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="327e1-108">Если командлет **Get-AzVirtualNetworkGatewayConnection** выдан без указания параметра-name, выходные данные не будут показывать сведения о ConnectionStatus и SharedKey.</span><span class="sxs-lookup"><span data-stu-id="327e1-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="327e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="327e1-109">EXAMPLES</span></span>

### <span data-ttu-id="327e1-110">1: получение подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="327e1-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="327e1-111">Возвращает объект подключения к шлюзу виртуальной сети с именем "myTunnel" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="327e1-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="327e1-112">2. получение подключений к шлюзу виртуальной сети с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="327e1-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="327e1-113">Возвращает все подключения к шлюзу виртуальной сети, которые начинаются с "myTunnel" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="327e1-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="327e1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="327e1-114">PARAMETERS</span></span>

### <span data-ttu-id="327e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327e1-115">-DefaultProfile</span></span>
<span data-ttu-id="327e1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="327e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="327e1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="327e1-117">-Name</span></span>
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

### <span data-ttu-id="327e1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327e1-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="327e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327e1-119">CommonParameters</span></span>
<span data-ttu-id="327e1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="327e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327e1-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="327e1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327e1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="327e1-122">INPUTS</span></span>

### <span data-ttu-id="327e1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="327e1-123">System.String</span></span>

## <span data-ttu-id="327e1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="327e1-124">OUTPUTS</span></span>

### <span data-ttu-id="327e1-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="327e1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="327e1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="327e1-126">NOTES</span></span>

## <span data-ttu-id="327e1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="327e1-127">RELATED LINKS</span></span>

[<span data-ttu-id="327e1-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="327e1-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="327e1-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="327e1-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="327e1-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="327e1-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
