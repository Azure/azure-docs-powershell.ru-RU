---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074775"
---
# <span data-ttu-id="b0c79-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b0c79-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="b0c79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0c79-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c79-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b0c79-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="b0c79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0c79-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0c79-105">DESCRIPTION</span></span>
<span data-ttu-id="b0c79-106">Командлет **New-AzApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c79-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="b0c79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0c79-107">EXAMPLES</span></span>

### <span data-ttu-id="b0c79-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="b0c79-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="b0c79-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="b0c79-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="b0c79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0c79-110">PARAMETERS</span></span>

### <span data-ttu-id="b0c79-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="b0c79-111">-Capacity</span></span>
<span data-ttu-id="b0c79-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b0c79-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="b0c79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c79-113">-DefaultProfile</span></span>
<span data-ttu-id="b0c79-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c79-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0c79-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0c79-115">-Name</span></span>
<span data-ttu-id="b0c79-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="b0c79-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="b0c79-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b0c79-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0c79-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="b0c79-118">Standard_Small</span></span>
- <span data-ttu-id="b0c79-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="b0c79-119">Standard_Medium</span></span>
- <span data-ttu-id="b0c79-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="b0c79-120">Standard_Large</span></span>
- <span data-ttu-id="b0c79-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="b0c79-121">WAF_Medium</span></span>
- <span data-ttu-id="b0c79-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="b0c79-122">WAF_Large</span></span>
- <span data-ttu-id="b0c79-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="b0c79-123">Standard_v2</span></span>
- <span data-ttu-id="b0c79-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b0c79-124">WAF_v2</span></span>

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

### <span data-ttu-id="b0c79-125">Уровень</span><span class="sxs-lookup"><span data-stu-id="b0c79-125">-Tier</span></span>
<span data-ttu-id="b0c79-126">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="b0c79-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="b0c79-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b0c79-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0c79-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="b0c79-128">Standard</span></span>
- <span data-ttu-id="b0c79-129">WAF</span><span class="sxs-lookup"><span data-stu-id="b0c79-129">WAF</span></span>
- <span data-ttu-id="b0c79-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="b0c79-130">Standard_v2</span></span>
- <span data-ttu-id="b0c79-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b0c79-131">WAF_v2</span></span>

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

### <span data-ttu-id="b0c79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c79-132">CommonParameters</span></span>
<span data-ttu-id="b0c79-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0c79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c79-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c79-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c79-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0c79-135">INPUTS</span></span>

### <span data-ttu-id="b0c79-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="b0c79-136">None</span></span>

## <span data-ttu-id="b0c79-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0c79-137">OUTPUTS</span></span>

### <span data-ttu-id="b0c79-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b0c79-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="b0c79-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0c79-139">NOTES</span></span>

## <span data-ttu-id="b0c79-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0c79-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0c79-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b0c79-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="b0c79-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b0c79-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


