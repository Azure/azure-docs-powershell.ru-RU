---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730379"
---
# <span data-ttu-id="bc2ad-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="bc2ad-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="bc2ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2ad-103">Создает SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="bc2ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc2ad-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc2ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2ad-106">Командлет **New-AzApplicationGatewaySku** создает единицу хранения (SKU) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="bc2ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc2ad-107">EXAMPLES</span></span>

### <span data-ttu-id="bc2ad-108">Пример 1: создание SKU для шлюза приложений Azure</span><span class="sxs-lookup"><span data-stu-id="bc2ad-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="bc2ad-109">Эта команда создает SKU с именем Standard_Small для шлюза приложений Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="bc2ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc2ad-110">PARAMETERS</span></span>

### <span data-ttu-id="bc2ad-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="bc2ad-111">-Capacity</span></span>
<span data-ttu-id="bc2ad-112">Задает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="bc2ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2ad-113">-DefaultProfile</span></span>
<span data-ttu-id="bc2ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc2ad-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc2ad-115">-Name</span></span>
<span data-ttu-id="bc2ad-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="bc2ad-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc2ad-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc2ad-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="bc2ad-118">Standard_Small</span></span>
- <span data-ttu-id="bc2ad-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="bc2ad-119">Standard_Medium</span></span>
- <span data-ttu-id="bc2ad-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="bc2ad-120">Standard_Large</span></span>
- <span data-ttu-id="bc2ad-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="bc2ad-121">WAF_Medium</span></span>
- <span data-ttu-id="bc2ad-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="bc2ad-122">WAF_Large</span></span>

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

### <span data-ttu-id="bc2ad-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="bc2ad-123">-Tier</span></span>
<span data-ttu-id="bc2ad-124">Указывает уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="bc2ad-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc2ad-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc2ad-126">Стандартная</span><span class="sxs-lookup"><span data-stu-id="bc2ad-126">Standard</span></span>
- <span data-ttu-id="bc2ad-127">WAF</span><span class="sxs-lookup"><span data-stu-id="bc2ad-127">WAF</span></span>

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

### <span data-ttu-id="bc2ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2ad-128">CommonParameters</span></span>
<span data-ttu-id="bc2ad-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc2ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2ad-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc2ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2ad-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc2ad-131">INPUTS</span></span>

### <span data-ttu-id="bc2ad-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc2ad-132">None</span></span>

## <span data-ttu-id="bc2ad-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc2ad-133">OUTPUTS</span></span>

### <span data-ttu-id="bc2ad-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="bc2ad-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="bc2ad-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc2ad-135">NOTES</span></span>

## <span data-ttu-id="bc2ad-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc2ad-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc2ad-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="bc2ad-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="bc2ad-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="bc2ad-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


