---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0e8644e55a599ae1cc72d9d04caa4ea4fb7eb5ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566814"
---
# <span data-ttu-id="f5ae5-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5ae5-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f5ae5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ae5-103">Возвращает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f5ae5-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ae5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5ae5-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ae5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ae5-106">Подключение к шлюзу виртуальной сети является объектом, представляющим туннель IPsec ("сайт-сайт" или "Виртуальная сеть-сеть"), подключенного к шлюзу виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ae5-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f5ae5-107">Командлет **Get-AzureRmVirtualNetworkGatewayConnection** возвращает объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5ae5-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f5ae5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5ae5-108">EXAMPLES</span></span>

### <span data-ttu-id="f5ae5-109">1: получение подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f5ae5-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="f5ae5-110">Возвращает объект подключения к шлюзу виртуальной сети с именем "myTunnel" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="f5ae5-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="f5ae5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5ae5-111">PARAMETERS</span></span>

### <span data-ttu-id="f5ae5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ae5-112">-DefaultProfile</span></span>
<span data-ttu-id="f5ae5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ae5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5ae5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5ae5-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ae5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ae5-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f5ae5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ae5-116">CommonParameters</span></span>
<span data-ttu-id="f5ae5-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5ae5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ae5-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ae5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ae5-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5ae5-119">INPUTS</span></span>

### <span data-ttu-id="f5ae5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f5ae5-120">System.String</span></span>

## <span data-ttu-id="f5ae5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5ae5-121">OUTPUTS</span></span>

### <span data-ttu-id="f5ae5-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5ae5-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f5ae5-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5ae5-123">NOTES</span></span>

## <span data-ttu-id="f5ae5-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5ae5-124">RELATED LINKS</span></span>
