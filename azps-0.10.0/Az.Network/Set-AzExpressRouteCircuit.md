---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911052"
---
# <span data-ttu-id="d8b20-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="d8b20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8b20-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b20-103">Изменение канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d8b20-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d8b20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8b20-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b20-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b20-106">Командлет **Set-AzExpressRouteCircuit** сохраняет модифицированную цепь ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b20-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="d8b20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8b20-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b20-108">Пример 1: изменение ServiceKeyа в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d8b20-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="d8b20-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8b20-109">PARAMETERS</span></span>

### <span data-ttu-id="d8b20-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8b20-110">-AsJob</span></span>
<span data-ttu-id="d8b20-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8b20-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8b20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b20-112">-DefaultProfile</span></span>
<span data-ttu-id="d8b20-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b20-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b20-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d8b20-115">Указывает объект **ExpressRouteCircuit** , который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d8b20-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8b20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b20-116">CommonParameters</span></span>
<span data-ttu-id="d8b20-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8b20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b20-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b20-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b20-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8b20-119">INPUTS</span></span>

### <span data-ttu-id="d8b20-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d8b20-121">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8b20-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="d8b20-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b20-122">OUTPUTS</span></span>

### <span data-ttu-id="d8b20-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d8b20-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8b20-124">NOTES</span></span>

## <span data-ttu-id="d8b20-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8b20-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8b20-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b20-127">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b20-128">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="d8b20-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d8b20-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
