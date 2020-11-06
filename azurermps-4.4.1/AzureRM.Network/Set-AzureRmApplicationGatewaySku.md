---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565224"
---
# <span data-ttu-id="c3e06-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3e06-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="c3e06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3e06-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e06-103">Изменение номера SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c3e06-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3e06-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3e06-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e06-106">Командлет **Set-AzureRmApplicationGatewaySku** изменяет единицу складского учета (SKU) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c3e06-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="c3e06-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3e06-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e06-108">Пример 1: обновление SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="c3e06-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="c3e06-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c3e06-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c3e06-110">Вторая команда обновляет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c3e06-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="c3e06-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3e06-111">PARAMETERS</span></span>

### <span data-ttu-id="c3e06-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e06-112">-ApplicationGateway</span></span>
<span data-ttu-id="c3e06-113">Указывает объект шлюза приложения, с которым этот командлет связывает SKU.</span><span class="sxs-lookup"><span data-stu-id="c3e06-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="c3e06-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c3e06-114">-Capacity</span></span>
<span data-ttu-id="c3e06-115">Указывает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c3e06-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e06-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3e06-116">-Name</span></span>
<span data-ttu-id="c3e06-117">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c3e06-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="c3e06-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3e06-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3e06-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="c3e06-119">Standard_Small</span></span>
- <span data-ttu-id="c3e06-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="c3e06-120">Standard_Medium</span></span>
- <span data-ttu-id="c3e06-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="c3e06-121">Standard_Large</span></span>
- <span data-ttu-id="c3e06-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="c3e06-122">WAF_Medium</span></span>
- <span data-ttu-id="c3e06-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="c3e06-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e06-124">Уровень</span><span class="sxs-lookup"><span data-stu-id="c3e06-124">-Tier</span></span>
<span data-ttu-id="c3e06-125">Указывает уровень шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c3e06-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="c3e06-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3e06-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3e06-127">Стандартная</span><span class="sxs-lookup"><span data-stu-id="c3e06-127">Standard</span></span>
- <span data-ttu-id="c3e06-128">WAF</span><span class="sxs-lookup"><span data-stu-id="c3e06-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e06-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e06-129">-DefaultProfile</span></span>
<span data-ttu-id="c3e06-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e06-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e06-131">CommonParameters</span></span>
<span data-ttu-id="c3e06-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3e06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e06-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e06-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e06-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3e06-134">INPUTS</span></span>

### <span data-ttu-id="c3e06-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e06-135">System.String</span></span>

## <span data-ttu-id="c3e06-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3e06-136">OUTPUTS</span></span>

### <span data-ttu-id="c3e06-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e06-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3e06-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3e06-138">NOTES</span></span>

## <span data-ttu-id="c3e06-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3e06-139">RELATED LINKS</span></span>

[<span data-ttu-id="c3e06-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3e06-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="c3e06-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3e06-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


