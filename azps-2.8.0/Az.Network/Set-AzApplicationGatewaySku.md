---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: ccc78a65041cac5cb471ac1f1bfa8d3ea3248ba1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903329"
---
# <span data-ttu-id="efbc5-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="efbc5-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="efbc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="efbc5-103">Изменение номера SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="efbc5-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="efbc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efbc5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efbc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efbc5-105">DESCRIPTION</span></span>
<span data-ttu-id="efbc5-106">Командлет **Set-AzApplicationGatewaySku** изменяет единицу складского учета (SKU) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="efbc5-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="efbc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efbc5-107">EXAMPLES</span></span>

### <span data-ttu-id="efbc5-108">Пример 1: обновление SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="efbc5-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="efbc5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="efbc5-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="efbc5-110">Вторая команда обновляет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="efbc5-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="efbc5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efbc5-111">PARAMETERS</span></span>

### <span data-ttu-id="efbc5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="efbc5-112">-ApplicationGateway</span></span>
<span data-ttu-id="efbc5-113">Указывает объект шлюза приложения, с которым этот командлет связывает SKU.</span><span class="sxs-lookup"><span data-stu-id="efbc5-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="efbc5-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="efbc5-114">-Capacity</span></span>
<span data-ttu-id="efbc5-115">Указывает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="efbc5-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="efbc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbc5-116">-DefaultProfile</span></span>
<span data-ttu-id="efbc5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efbc5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efbc5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efbc5-118">-Name</span></span>
<span data-ttu-id="efbc5-119">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="efbc5-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="efbc5-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="efbc5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efbc5-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="efbc5-121">Standard_Small</span></span>
- <span data-ttu-id="efbc5-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="efbc5-122">Standard_Medium</span></span>
- <span data-ttu-id="efbc5-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="efbc5-123">Standard_Large</span></span>
- <span data-ttu-id="efbc5-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="efbc5-124">WAF_Medium</span></span>
- <span data-ttu-id="efbc5-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="efbc5-125">WAF_Large</span></span>

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

### <span data-ttu-id="efbc5-126">Уровень</span><span class="sxs-lookup"><span data-stu-id="efbc5-126">-Tier</span></span>
<span data-ttu-id="efbc5-127">Указывает уровень шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="efbc5-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="efbc5-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="efbc5-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efbc5-129">Стандартная</span><span class="sxs-lookup"><span data-stu-id="efbc5-129">Standard</span></span>
- <span data-ttu-id="efbc5-130">WAF</span><span class="sxs-lookup"><span data-stu-id="efbc5-130">WAF</span></span>

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

### <span data-ttu-id="efbc5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbc5-131">CommonParameters</span></span>
<span data-ttu-id="efbc5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efbc5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbc5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbc5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbc5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efbc5-134">INPUTS</span></span>

### <span data-ttu-id="efbc5-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="efbc5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="efbc5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efbc5-136">OUTPUTS</span></span>

### <span data-ttu-id="efbc5-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="efbc5-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="efbc5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="efbc5-138">NOTES</span></span>

## <span data-ttu-id="efbc5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efbc5-139">RELATED LINKS</span></span>

[<span data-ttu-id="efbc5-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="efbc5-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="efbc5-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="efbc5-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


