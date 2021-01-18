---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506098"
---
# <span data-ttu-id="54320-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="54320-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="54320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54320-102">SYNOPSIS</span></span>
<span data-ttu-id="54320-103">Создает исключение из политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="54320-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="54320-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54320-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54320-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54320-105">DESCRIPTION</span></span>
<span data-ttu-id="54320-106">Новый список правил исключения для политики брандмауэра **New-AzApplicationGatewayFirewallPolicyExclusion.**</span><span class="sxs-lookup"><span data-stu-id="54320-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="54320-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54320-107">EXAMPLES</span></span>

### <span data-ttu-id="54320-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54320-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="54320-109">Эта команда создает новое исключение для переменной RequestHeaderNames и оператора StartsWith и Selector с именем xyz.</span><span class="sxs-lookup"><span data-stu-id="54320-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="54320-110">Запись исключения будет сохранена в $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="54320-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="54320-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54320-111">PARAMETERS</span></span>

### <span data-ttu-id="54320-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54320-112">-DefaultProfile</span></span>
<span data-ttu-id="54320-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54320-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54320-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="54320-114">-MatchVariable</span></span>
<span data-ttu-id="54320-115">Переменная, исключаемая.</span><span class="sxs-lookup"><span data-stu-id="54320-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54320-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="54320-116">-Selector</span></span>
<span data-ttu-id="54320-117">Если переменная является коллекцией, оператор, используемый для указания элементов в коллекции, к которым применяется исключение.</span><span class="sxs-lookup"><span data-stu-id="54320-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="54320-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="54320-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="54320-119">Если переменная является коллекцией, оперировать с селектором, чтобы указать, к каку элементам коллекции применяется исключение.</span><span class="sxs-lookup"><span data-stu-id="54320-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54320-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54320-120">CommonParameters</span></span>
<span data-ttu-id="54320-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54320-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54320-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54320-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54320-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54320-123">INPUTS</span></span>

### <span data-ttu-id="54320-124">Нет</span><span class="sxs-lookup"><span data-stu-id="54320-124">None</span></span>

## <span data-ttu-id="54320-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54320-125">OUTPUTS</span></span>

### <span data-ttu-id="54320-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="54320-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="54320-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54320-127">NOTES</span></span>

## <span data-ttu-id="54320-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54320-128">RELATED LINKS</span></span>
