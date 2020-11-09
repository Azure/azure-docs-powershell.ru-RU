---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318014"
---
# <span data-ttu-id="feb80-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="feb80-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="feb80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="feb80-102">SYNOPSIS</span></span>
<span data-ttu-id="feb80-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="feb80-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="feb80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="feb80-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feb80-105">DESCRIPTION</span></span>
<span data-ttu-id="feb80-106">Командлет **New-AzApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="feb80-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="feb80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="feb80-107">EXAMPLES</span></span>

### <span data-ttu-id="feb80-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="feb80-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="feb80-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="feb80-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="feb80-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="feb80-110">PARAMETERS</span></span>

### <span data-ttu-id="feb80-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="feb80-111">-Capacity</span></span>
<span data-ttu-id="feb80-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="feb80-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="feb80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb80-113">-DefaultProfile</span></span>
<span data-ttu-id="feb80-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feb80-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb80-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="feb80-115">-Name</span></span>
<span data-ttu-id="feb80-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="feb80-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="feb80-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="feb80-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="feb80-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="feb80-118">Standard_Small</span></span>
- <span data-ttu-id="feb80-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="feb80-119">Standard_Medium</span></span>
- <span data-ttu-id="feb80-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="feb80-120">Standard_Large</span></span>
- <span data-ttu-id="feb80-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="feb80-121">WAF_Medium</span></span>
- <span data-ttu-id="feb80-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="feb80-122">WAF_Large</span></span>
- <span data-ttu-id="feb80-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="feb80-123">Standard_v2</span></span>
- <span data-ttu-id="feb80-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="feb80-124">WAF_v2</span></span>

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

### <span data-ttu-id="feb80-125">Уровень</span><span class="sxs-lookup"><span data-stu-id="feb80-125">-Tier</span></span>
<span data-ttu-id="feb80-126">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="feb80-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="feb80-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="feb80-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="feb80-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="feb80-128">Standard</span></span>
- <span data-ttu-id="feb80-129">WAF</span><span class="sxs-lookup"><span data-stu-id="feb80-129">WAF</span></span>
- <span data-ttu-id="feb80-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="feb80-130">Standard_v2</span></span>
- <span data-ttu-id="feb80-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="feb80-131">WAF_v2</span></span>

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

### <span data-ttu-id="feb80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb80-132">CommonParameters</span></span>
<span data-ttu-id="feb80-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="feb80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb80-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb80-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb80-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="feb80-135">INPUTS</span></span>

### <span data-ttu-id="feb80-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="feb80-136">None</span></span>

## <span data-ttu-id="feb80-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="feb80-137">OUTPUTS</span></span>

### <span data-ttu-id="feb80-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="feb80-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="feb80-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="feb80-139">NOTES</span></span>

## <span data-ttu-id="feb80-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feb80-140">RELATED LINKS</span></span>

[<span data-ttu-id="feb80-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="feb80-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="feb80-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="feb80-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


