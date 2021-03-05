---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1f99fe982496fc6cef3ee9579d8e0be555880aaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006200"
---
# <span data-ttu-id="3ecda-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3ecda-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="3ecda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ecda-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecda-103">Создает SKU для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3ecda-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="3ecda-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ecda-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ecda-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ecda-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecda-106">Для шлюза приложения Azure с его использованием создается проектный проект **New-AzApplicationGatewaySku.**</span><span class="sxs-lookup"><span data-stu-id="3ecda-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="3ecda-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ecda-107">EXAMPLES</span></span>

### <span data-ttu-id="3ecda-108">Пример 1. Создание SKU для шлюза приложения Azure</span><span class="sxs-lookup"><span data-stu-id="3ecda-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3ecda-109">Эта команда создает SKU с именем Standard_Small для шлюза приложения Azure и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="3ecda-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="3ecda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ecda-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecda-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3ecda-111">-Capacity</span></span>
<span data-ttu-id="3ecda-112">Количество экземпляров шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3ecda-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="3ecda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecda-113">-DefaultProfile</span></span>
<span data-ttu-id="3ecda-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ecda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ecda-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3ecda-115">-Name</span></span>
<span data-ttu-id="3ecda-116">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="3ecda-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="3ecda-117">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="3ecda-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ecda-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3ecda-118">Standard_Small</span></span>
- <span data-ttu-id="3ecda-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3ecda-119">Standard_Medium</span></span>
- <span data-ttu-id="3ecda-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3ecda-120">Standard_Large</span></span>
- <span data-ttu-id="3ecda-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3ecda-121">WAF_Medium</span></span>
- <span data-ttu-id="3ecda-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3ecda-122">WAF_Large</span></span>
- <span data-ttu-id="3ecda-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="3ecda-123">Standard_v2</span></span>
- <span data-ttu-id="3ecda-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3ecda-124">WAF_v2</span></span>

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

### <span data-ttu-id="3ecda-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="3ecda-125">-Tier</span></span>
<span data-ttu-id="3ecda-126">Определяет уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="3ecda-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="3ecda-127">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="3ecda-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ecda-128">Стандартный</span><span class="sxs-lookup"><span data-stu-id="3ecda-128">Standard</span></span>
- <span data-ttu-id="3ecda-129">WAF</span><span class="sxs-lookup"><span data-stu-id="3ecda-129">WAF</span></span>
- <span data-ttu-id="3ecda-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="3ecda-130">Standard_v2</span></span>
- <span data-ttu-id="3ecda-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3ecda-131">WAF_v2</span></span>

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

### <span data-ttu-id="3ecda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecda-132">CommonParameters</span></span>
<span data-ttu-id="3ecda-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecda-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecda-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecda-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ecda-135">INPUTS</span></span>

### <span data-ttu-id="3ecda-136">Нет</span><span class="sxs-lookup"><span data-stu-id="3ecda-136">None</span></span>

## <span data-ttu-id="3ecda-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ecda-137">OUTPUTS</span></span>

### <span data-ttu-id="3ecda-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3ecda-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="3ecda-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ecda-139">NOTES</span></span>

## <span data-ttu-id="3ecda-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ecda-140">RELATED LINKS</span></span>

[<span data-ttu-id="3ecda-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3ecda-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="3ecda-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3ecda-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


