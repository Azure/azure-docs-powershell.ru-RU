---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914077"
---
# <span data-ttu-id="c52bd-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c52bd-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="c52bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c52bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c52bd-103">Получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="c52bd-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c52bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c52bd-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c52bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52bd-105">DESCRIPTION</span></span>
<span data-ttu-id="c52bd-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="c52bd-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="c52bd-107">Командлет **Get-AzureRmLocalNetworkGateway** возвращает объект, представляющий локальный шлюз на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c52bd-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c52bd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c52bd-108">EXAMPLES</span></span>

### <span data-ttu-id="c52bd-109">1: получение шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="c52bd-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="c52bd-110">Возвращает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="c52bd-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="c52bd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c52bd-111">PARAMETERS</span></span>

### <span data-ttu-id="c52bd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52bd-112">-DefaultProfile</span></span>
<span data-ttu-id="c52bd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c52bd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c52bd-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c52bd-114">-Name</span></span>
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

### <span data-ttu-id="c52bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52bd-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c52bd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52bd-116">CommonParameters</span></span>
<span data-ttu-id="c52bd-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c52bd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52bd-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52bd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52bd-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c52bd-119">INPUTS</span></span>

## <span data-ttu-id="c52bd-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52bd-120">OUTPUTS</span></span>

### <span data-ttu-id="c52bd-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c52bd-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="c52bd-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="c52bd-122">NOTES</span></span>

## <span data-ttu-id="c52bd-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c52bd-123">RELATED LINKS</span></span>

