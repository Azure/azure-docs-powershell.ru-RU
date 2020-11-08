---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074829"
---
# <span data-ttu-id="67fd4-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="67fd4-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="67fd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="67fd4-103">Создание списка исключаемых правил для WAF шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="67fd4-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="67fd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67fd4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67fd4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="67fd4-106">Командлет **New-AzApplicationGatewayFirewallExclusionConfig** — новый список правил исключения для WAF шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="67fd4-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="67fd4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="67fd4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67fd4-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="67fd4-109">Эта команда создает новое правило исключения, которое содержит конфигурацию для переменной с именем RequestHeaderNames и с именем XYZ и Selector.</span><span class="sxs-lookup"><span data-stu-id="67fd4-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="67fd4-110">Конфигурация списка исключений сохраняется в $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="67fd4-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="67fd4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67fd4-111">PARAMETERS</span></span>

### <span data-ttu-id="67fd4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67fd4-112">-DefaultProfile</span></span>
<span data-ttu-id="67fd4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67fd4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67fd4-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="67fd4-114">-Operator</span></span>
<span data-ttu-id="67fd4-115">Если переменная является коллекцией, то для указания элементов в коллекции, к которой применяется это исключение, проработайте с элементом selector.</span><span class="sxs-lookup"><span data-stu-id="67fd4-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="67fd4-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="67fd4-116">-Selector</span></span>
<span data-ttu-id="67fd4-117">Если переменная является коллекцией, оператор используется для указания элементов в коллекции, к которой применяется это исключение.</span><span class="sxs-lookup"><span data-stu-id="67fd4-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="67fd4-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="67fd4-118">-Variable</span></span>
<span data-ttu-id="67fd4-119">Переменная, которую нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="67fd4-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="67fd4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67fd4-120">CommonParameters</span></span>
<span data-ttu-id="67fd4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67fd4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67fd4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67fd4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67fd4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67fd4-123">INPUTS</span></span>

### <span data-ttu-id="67fd4-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="67fd4-124">None</span></span>

## <span data-ttu-id="67fd4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67fd4-125">OUTPUTS</span></span>

### <span data-ttu-id="67fd4-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="67fd4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="67fd4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="67fd4-127">NOTES</span></span>

## <span data-ttu-id="67fd4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67fd4-128">RELATED LINKS</span></span>
