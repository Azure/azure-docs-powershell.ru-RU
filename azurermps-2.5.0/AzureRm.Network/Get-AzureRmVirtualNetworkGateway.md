---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913829"
---
# <span data-ttu-id="675c0-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="675c0-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="675c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="675c0-102">SYNOPSIS</span></span>
<span data-ttu-id="675c0-103">Получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="675c0-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="675c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="675c0-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="675c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="675c0-105">DESCRIPTION</span></span>
<span data-ttu-id="675c0-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="675c0-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="675c0-107">Командлет **Get-AzureRmVirtualNetworkGateway** возвращает объект шлюза в Azure на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="675c0-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="675c0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="675c0-108">EXAMPLES</span></span>

### <span data-ttu-id="675c0-109">1: получение шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="675c0-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="675c0-110">Возвращает объект шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="675c0-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="675c0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="675c0-111">PARAMETERS</span></span>

### <span data-ttu-id="675c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675c0-112">-DefaultProfile</span></span>
<span data-ttu-id="675c0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="675c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="675c0-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="675c0-114">-Name</span></span>
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

### <span data-ttu-id="675c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="675c0-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="675c0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675c0-116">CommonParameters</span></span>
<span data-ttu-id="675c0-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="675c0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675c0-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="675c0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675c0-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="675c0-119">INPUTS</span></span>

## <span data-ttu-id="675c0-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="675c0-120">OUTPUTS</span></span>

### <span data-ttu-id="675c0-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="675c0-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="675c0-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="675c0-122">NOTES</span></span>

## <span data-ttu-id="675c0-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="675c0-123">RELATED LINKS</span></span>

