---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565863"
---
# <span data-ttu-id="0bbe3-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="0bbe3-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="0bbe3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbe3-103">Создание списка исключаемых правил для WAF шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0bbe3-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bbe3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bbe3-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bbe3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-105">DESCRIPTION</span></span>
<span data-ttu-id="0bbe3-106">Командлет **New-AzureRmApplicationGatewayFirewallExclusionConfig** — новый список правил исключения для WAF шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="0bbe3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-107">EXAMPLES</span></span>

### <span data-ttu-id="0bbe3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0bbe3-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="0bbe3-109">Эта команда создает новое правило исключения, которое содержит конфигурацию для переменной с именем RequestHeaderNames и с именем XYZ и Selector.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="0bbe3-110">Конфигурация списка исключений сохраняется в $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="0bbe3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-111">PARAMETERS</span></span>

### <span data-ttu-id="0bbe3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbe3-112">-DefaultProfile</span></span>
<span data-ttu-id="0bbe3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bbe3-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="0bbe3-114">-Operator</span></span>
<span data-ttu-id="0bbe3-115">Если переменная является коллекцией, то для указания элементов в коллекции, к которой применяется это исключение, проработайте с элементом selector.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbe3-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="0bbe3-116">-Selector</span></span>
<span data-ttu-id="0bbe3-117">Если переменная является коллекцией, оператор используется для указания элементов в коллекции, к которой применяется это исключение.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbe3-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="0bbe3-118">-Variable</span></span>
<span data-ttu-id="0bbe3-119">Переменная, которую нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbe3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbe3-120">CommonParameters</span></span>
<span data-ttu-id="0bbe3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbe3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bbe3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbe3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bbe3-123">INPUTS</span></span>

### <span data-ttu-id="0bbe3-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="0bbe3-124">None</span></span>

## <span data-ttu-id="0bbe3-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-125">OUTPUTS</span></span>

### <span data-ttu-id="0bbe3-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="0bbe3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="0bbe3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bbe3-127">NOTES</span></span>

## <span data-ttu-id="0bbe3-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-128">RELATED LINKS</span></span>
