---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421916"
---
# <span data-ttu-id="a116d-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="a116d-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="a116d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a116d-102">SYNOPSIS</span></span>
<span data-ttu-id="a116d-103">Создание списка правил исключения для шлюза приложения waf</span><span class="sxs-lookup"><span data-stu-id="a116d-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="a116d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a116d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a116d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a116d-105">DESCRIPTION</span></span>
<span data-ttu-id="a116d-106">Новый список правил исключения для шлюза приложения waf — **New-AzApplicationGatewayFirewallExclusionConfig.**</span><span class="sxs-lookup"><span data-stu-id="a116d-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="a116d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a116d-107">EXAMPLES</span></span>

### <span data-ttu-id="a116d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a116d-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="a116d-109">Эта команда создает новое правило исключения для переменной RequestHeaderNames и оператора StartsWith и Selector с именем xyz.</span><span class="sxs-lookup"><span data-stu-id="a116d-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="a116d-110">Конфигурация списка исключений будет сохранена в $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="a116d-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="a116d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a116d-111">PARAMETERS</span></span>

### <span data-ttu-id="a116d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a116d-112">-DefaultProfile</span></span>
<span data-ttu-id="a116d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a116d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a116d-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="a116d-114">-Operator</span></span>
<span data-ttu-id="a116d-115">Если переменная является коллекцией, оперировать с селектором, чтобы указать, к каку элементам коллекции применяется исключение.</span><span class="sxs-lookup"><span data-stu-id="a116d-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="a116d-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="a116d-116">-Selector</span></span>
<span data-ttu-id="a116d-117">Если переменная является коллекцией, оператор, используемый для указания элементов в коллекции, к которым применяется исключение.</span><span class="sxs-lookup"><span data-stu-id="a116d-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="a116d-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="a116d-118">-Variable</span></span>
<span data-ttu-id="a116d-119">Переменная, исключаемая.</span><span class="sxs-lookup"><span data-stu-id="a116d-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="a116d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a116d-120">CommonParameters</span></span>
<span data-ttu-id="a116d-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a116d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a116d-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a116d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a116d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a116d-123">INPUTS</span></span>

### <span data-ttu-id="a116d-124">Нет</span><span class="sxs-lookup"><span data-stu-id="a116d-124">None</span></span>

## <span data-ttu-id="a116d-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a116d-125">OUTPUTS</span></span>

### <span data-ttu-id="a116d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="a116d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="a116d-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a116d-127">NOTES</span></span>

## <span data-ttu-id="a116d-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a116d-128">RELATED LINKS</span></span>
