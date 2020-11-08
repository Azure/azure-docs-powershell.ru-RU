---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244383"
---
# <span data-ttu-id="96354-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96354-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="96354-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96354-102">SYNOPSIS</span></span>
<span data-ttu-id="96354-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="96354-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="96354-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96354-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96354-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96354-105">DESCRIPTION</span></span>
<span data-ttu-id="96354-106">Командлет **New-AzApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="96354-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="96354-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96354-107">EXAMPLES</span></span>

### <span data-ttu-id="96354-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="96354-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="96354-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="96354-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="96354-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96354-110">PARAMETERS</span></span>

### <span data-ttu-id="96354-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="96354-111">-Capacity</span></span>
<span data-ttu-id="96354-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="96354-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="96354-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96354-113">-DefaultProfile</span></span>
<span data-ttu-id="96354-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96354-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96354-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96354-115">-Name</span></span>
<span data-ttu-id="96354-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="96354-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="96354-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96354-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96354-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="96354-118">Standard_Small</span></span>
- <span data-ttu-id="96354-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="96354-119">Standard_Medium</span></span>
- <span data-ttu-id="96354-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="96354-120">Standard_Large</span></span>
- <span data-ttu-id="96354-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="96354-121">WAF_Medium</span></span>
- <span data-ttu-id="96354-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="96354-122">WAF_Large</span></span>
- <span data-ttu-id="96354-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="96354-123">Standard_v2</span></span>
- <span data-ttu-id="96354-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="96354-124">WAF_v2</span></span>

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

### <span data-ttu-id="96354-125">Уровень</span><span class="sxs-lookup"><span data-stu-id="96354-125">-Tier</span></span>
<span data-ttu-id="96354-126">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="96354-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="96354-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96354-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96354-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="96354-128">Standard</span></span>
- <span data-ttu-id="96354-129">WAF</span><span class="sxs-lookup"><span data-stu-id="96354-129">WAF</span></span>
- <span data-ttu-id="96354-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="96354-130">Standard_v2</span></span>
- <span data-ttu-id="96354-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="96354-131">WAF_v2</span></span>

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

### <span data-ttu-id="96354-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96354-132">CommonParameters</span></span>
<span data-ttu-id="96354-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96354-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96354-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96354-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96354-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96354-135">INPUTS</span></span>

### <span data-ttu-id="96354-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="96354-136">None</span></span>

## <span data-ttu-id="96354-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96354-137">OUTPUTS</span></span>

### <span data-ttu-id="96354-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96354-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="96354-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="96354-139">NOTES</span></span>

## <span data-ttu-id="96354-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96354-140">RELATED LINKS</span></span>

[<span data-ttu-id="96354-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96354-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="96354-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96354-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


