---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073222"
---
# <span data-ttu-id="a171c-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a171c-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="a171c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a171c-102">SYNOPSIS</span></span>
<span data-ttu-id="a171c-103">Создание Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="a171c-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="a171c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a171c-104">SYNTAX</span></span>

### <span data-ttu-id="a171c-105">HostedGatewayParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a171c-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a171c-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a171c-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a171c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a171c-107">DESCRIPTION</span></span>
<span data-ttu-id="a171c-108">Командлет **New-AzVirtualRouter** создает Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a171c-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="a171c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a171c-109">EXAMPLES</span></span>

### <span data-ttu-id="a171c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a171c-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="a171c-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a171c-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="a171c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a171c-112">PARAMETERS</span></span>

### <span data-ttu-id="a171c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a171c-113">-AsJob</span></span>
<span data-ttu-id="a171c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a171c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a171c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a171c-115">-DefaultProfile</span></span>
<span data-ttu-id="a171c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a171c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a171c-117">-Force</span></span>
<span data-ttu-id="a171c-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="a171c-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a171c-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="a171c-119">-HostedGateway</span></span>
<span data-ttu-id="a171c-120">Шлюз, на котором должен быть размещен виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="a171c-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="a171c-121">-HostedGatewayId</span></span>
<span data-ttu-id="a171c-122">Идентификатор шлюза, на котором должен быть размещен виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="a171c-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a171c-123">-Location</span></span>
<span data-ttu-id="a171c-124">Расположение.</span><span class="sxs-lookup"><span data-stu-id="a171c-124">The location.</span></span>

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

### <span data-ttu-id="a171c-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a171c-125">-Name</span></span>
<span data-ttu-id="a171c-126">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="a171c-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a171c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a171c-128">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="a171c-128">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="a171c-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="a171c-129">-Tag</span></span>
<span data-ttu-id="a171c-130">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a171c-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a171c-131">-Confirm</span></span>
<span data-ttu-id="a171c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a171c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a171c-133">-WhatIf</span></span>
<span data-ttu-id="a171c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a171c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a171c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a171c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a171c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a171c-136">CommonParameters</span></span>
<span data-ttu-id="a171c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a171c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a171c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a171c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a171c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a171c-139">INPUTS</span></span>

### <span data-ttu-id="a171c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a171c-140">System.String</span></span>

### <span data-ttu-id="a171c-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a171c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a171c-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a171c-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a171c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a171c-143">OUTPUTS</span></span>

### <span data-ttu-id="a171c-144">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a171c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a171c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a171c-145">NOTES</span></span>

## <span data-ttu-id="a171c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a171c-146">RELATED LINKS</span></span>
