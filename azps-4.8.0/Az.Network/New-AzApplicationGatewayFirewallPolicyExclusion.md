---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244395"
---
# <span data-ttu-id="63692-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="63692-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="63692-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63692-102">SYNOPSIS</span></span>
<span data-ttu-id="63692-103">Создание исключения для политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="63692-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="63692-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63692-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63692-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63692-105">DESCRIPTION</span></span>
<span data-ttu-id="63692-106">Командлет **New-AzApplicationGatewayFirewallPolicyExclusion** , новый список правил исключения для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="63692-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="63692-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63692-107">EXAMPLES</span></span>

### <span data-ttu-id="63692-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63692-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="63692-109">Эта команда создает новую запись исключения для переменной с именем RequestHeaderNames и operator с именем XYZ и Selector.</span><span class="sxs-lookup"><span data-stu-id="63692-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="63692-110">Запись исключения сохраняется в $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="63692-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="63692-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63692-111">PARAMETERS</span></span>

### <span data-ttu-id="63692-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63692-112">-DefaultProfile</span></span>
<span data-ttu-id="63692-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63692-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63692-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="63692-114">-MatchVariable</span></span>
<span data-ttu-id="63692-115">Переменная, которую нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="63692-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="63692-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="63692-116">-Selector</span></span>
<span data-ttu-id="63692-117">Если переменная является коллекцией, оператор используется для указания элементов в коллекции, к которой применяется это исключение.</span><span class="sxs-lookup"><span data-stu-id="63692-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="63692-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="63692-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="63692-119">Если переменная является коллекцией, то для указания элементов в коллекции, к которой применяется это исключение, проработайте с элементом selector.</span><span class="sxs-lookup"><span data-stu-id="63692-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="63692-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63692-120">CommonParameters</span></span>
<span data-ttu-id="63692-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63692-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63692-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63692-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63692-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63692-123">INPUTS</span></span>

### <span data-ttu-id="63692-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="63692-124">None</span></span>

## <span data-ttu-id="63692-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63692-125">OUTPUTS</span></span>

### <span data-ttu-id="63692-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="63692-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="63692-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="63692-127">NOTES</span></span>

## <span data-ttu-id="63692-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63692-128">RELATED LINKS</span></span>
