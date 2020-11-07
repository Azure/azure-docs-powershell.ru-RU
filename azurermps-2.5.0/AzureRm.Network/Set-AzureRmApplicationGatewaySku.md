---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: ccefc75d28ee49f12dd1f72d03512e3850298986
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913771"
---
# <span data-ttu-id="3953e-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3953e-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="3953e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3953e-102">SYNOPSIS</span></span>
<span data-ttu-id="3953e-103">Изменение номера SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3953e-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3953e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3953e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3953e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3953e-105">DESCRIPTION</span></span>
<span data-ttu-id="3953e-106">Командлет **Set-AzureRmApplicationGatewaySku** изменяет единицу складского учета (SKU) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3953e-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="3953e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3953e-107">EXAMPLES</span></span>

### <span data-ttu-id="3953e-108">Пример 1: обновление SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="3953e-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3953e-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3953e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3953e-110">Вторая команда обновляет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3953e-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="3953e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3953e-111">PARAMETERS</span></span>

### <span data-ttu-id="3953e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3953e-112">-ApplicationGateway</span></span>
<span data-ttu-id="3953e-113">Указывает объект шлюза приложения, с которым этот командлет связывает SKU.</span><span class="sxs-lookup"><span data-stu-id="3953e-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3953e-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3953e-114">-Capacity</span></span>
<span data-ttu-id="3953e-115">Указывает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3953e-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3953e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3953e-116">-DefaultProfile</span></span>
<span data-ttu-id="3953e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3953e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3953e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3953e-118">-Name</span></span>
<span data-ttu-id="3953e-119">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3953e-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="3953e-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3953e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3953e-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3953e-121">Standard_Small</span></span>
- <span data-ttu-id="3953e-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3953e-122">Standard_Medium</span></span>
- <span data-ttu-id="3953e-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3953e-123">Standard_Large</span></span>
- <span data-ttu-id="3953e-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3953e-124">WAF_Medium</span></span>
- <span data-ttu-id="3953e-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3953e-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3953e-126">Уровень</span><span class="sxs-lookup"><span data-stu-id="3953e-126">-Tier</span></span>
<span data-ttu-id="3953e-127">Указывает уровень шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3953e-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="3953e-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3953e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3953e-129">Стандартная</span><span class="sxs-lookup"><span data-stu-id="3953e-129">Standard</span></span>
- <span data-ttu-id="3953e-130">WAF</span><span class="sxs-lookup"><span data-stu-id="3953e-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3953e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3953e-131">CommonParameters</span></span>
<span data-ttu-id="3953e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3953e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3953e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3953e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3953e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3953e-134">INPUTS</span></span>

### <span data-ttu-id="3953e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3953e-135">System.String</span></span>

## <span data-ttu-id="3953e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3953e-136">OUTPUTS</span></span>

### <span data-ttu-id="3953e-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3953e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3953e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3953e-138">NOTES</span></span>

## <span data-ttu-id="3953e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3953e-139">RELATED LINKS</span></span>

[<span data-ttu-id="3953e-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3953e-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="3953e-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3953e-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


