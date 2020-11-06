---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 71a6ec46cea6cc9d2ba6e6537797657b2124fe01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561716"
---
# <span data-ttu-id="5c472-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="5c472-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c472-102">SYNOPSIS</span></span>
<span data-ttu-id="5c472-103">Изменение канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5c472-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c472-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c472-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c472-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c472-105">DESCRIPTION</span></span>
<span data-ttu-id="5c472-106">Командлет **Set-AzureRmExpressRouteCircuit** сохраняет модифицированную цепь ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="5c472-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="5c472-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c472-107">EXAMPLES</span></span>

### <span data-ttu-id="5c472-108">Пример 1: изменение ServiceKeyа в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5c472-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="5c472-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c472-109">PARAMETERS</span></span>

### <span data-ttu-id="5c472-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c472-110">-AsJob</span></span>
<span data-ttu-id="5c472-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c472-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c472-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c472-112">-DefaultProfile</span></span>
<span data-ttu-id="5c472-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c472-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c472-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5c472-115">Указывает объект **ExpressRouteCircuit** , который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c472-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c472-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c472-116">CommonParameters</span></span>
<span data-ttu-id="5c472-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c472-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c472-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c472-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c472-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c472-119">INPUTS</span></span>

### <span data-ttu-id="5c472-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5c472-121">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5c472-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="5c472-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c472-122">OUTPUTS</span></span>

### <span data-ttu-id="5c472-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5c472-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c472-124">NOTES</span></span>

## <span data-ttu-id="5c472-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c472-125">RELATED LINKS</span></span>

[<span data-ttu-id="5c472-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5c472-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5c472-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5c472-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c472-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
