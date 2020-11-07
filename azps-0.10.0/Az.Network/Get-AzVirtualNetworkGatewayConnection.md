---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909841"
---
# <span data-ttu-id="95972-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95972-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="95972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95972-102">SYNOPSIS</span></span>
<span data-ttu-id="95972-103">Возвращает подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95972-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="95972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95972-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95972-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95972-105">DESCRIPTION</span></span>
<span data-ttu-id="95972-106">Подключение к шлюзу виртуальной сети является объектом, представляющим туннель IPsec ("сайт-сайт" или "Виртуальная сеть-сеть"), подключенного к шлюзу виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="95972-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="95972-107">Командлет **Get-AzVirtualNetworkGatewayConnection** возвращает объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95972-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="95972-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95972-108">EXAMPLES</span></span>

### <span data-ttu-id="95972-109">1: получение подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="95972-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="95972-110">Возвращает объект подключения к шлюзу виртуальной сети с именем "myTunnel" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="95972-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="95972-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95972-111">PARAMETERS</span></span>

### <span data-ttu-id="95972-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95972-112">-DefaultProfile</span></span>
<span data-ttu-id="95972-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95972-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95972-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95972-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95972-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95972-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95972-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95972-116">CommonParameters</span></span>
<span data-ttu-id="95972-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95972-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95972-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95972-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95972-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95972-119">INPUTS</span></span>

## <span data-ttu-id="95972-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95972-120">OUTPUTS</span></span>

### <span data-ttu-id="95972-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95972-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="95972-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="95972-122">NOTES</span></span>

## <span data-ttu-id="95972-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95972-123">RELATED LINKS</span></span>

