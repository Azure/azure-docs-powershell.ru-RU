---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518038"
---
# <span data-ttu-id="3925e-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3925e-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="3925e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3925e-102">SYNOPSIS</span></span>
<span data-ttu-id="3925e-103">Изменяет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="3925e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3925e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3925e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3925e-105">DESCRIPTION</span></span>
<span data-ttu-id="3925e-106">**Cmdlet Set-AzApplicationGatewaySku** изменяет единицу сохраняемого акций (SKU) шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="3925e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3925e-107">EXAMPLES</span></span>

### <span data-ttu-id="3925e-108">Пример 1. Обновление SKU шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="3925e-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3925e-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="3925e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3925e-110">Вторая команда обновляет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="3925e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3925e-111">PARAMETERS</span></span>

### <span data-ttu-id="3925e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3925e-112">-ApplicationGateway</span></span>
<span data-ttu-id="3925e-113">Определяет объект шлюза приложения, с которым этот cmdlet связывает SKU.</span><span class="sxs-lookup"><span data-stu-id="3925e-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3925e-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3925e-114">-Capacity</span></span>
<span data-ttu-id="3925e-115">Количество экземпляров шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3925e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3925e-116">-DefaultProfile</span></span>
<span data-ttu-id="3925e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3925e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3925e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3925e-118">-Name</span></span>
<span data-ttu-id="3925e-119">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="3925e-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3925e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3925e-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3925e-121">Standard_Small</span></span>
- <span data-ttu-id="3925e-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3925e-122">Standard_Medium</span></span>
- <span data-ttu-id="3925e-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3925e-123">Standard_Large</span></span>
- <span data-ttu-id="3925e-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3925e-124">WAF_Medium</span></span>
- <span data-ttu-id="3925e-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3925e-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3925e-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="3925e-126">-Tier</span></span>
<span data-ttu-id="3925e-127">Определяет уровень шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3925e-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="3925e-128">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3925e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3925e-129">Стандартный</span><span class="sxs-lookup"><span data-stu-id="3925e-129">Standard</span></span>
- <span data-ttu-id="3925e-130">WAF</span><span class="sxs-lookup"><span data-stu-id="3925e-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3925e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3925e-131">CommonParameters</span></span>
<span data-ttu-id="3925e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3925e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3925e-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3925e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3925e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3925e-134">INPUTS</span></span>

### <span data-ttu-id="3925e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3925e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3925e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3925e-136">OUTPUTS</span></span>

### <span data-ttu-id="3925e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3925e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3925e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3925e-138">NOTES</span></span>

## <span data-ttu-id="3925e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3925e-139">RELATED LINKS</span></span>

[<span data-ttu-id="3925e-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3925e-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="3925e-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3925e-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


