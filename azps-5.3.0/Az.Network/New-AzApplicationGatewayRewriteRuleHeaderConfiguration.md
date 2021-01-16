---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421828"
---
# <span data-ttu-id="4b56d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b56d-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="4b56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b56d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b56d-103">Создает конфигурацию заглавного правила переописи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4b56d-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="4b56d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b56d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b56d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b56d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b56d-106">**Cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** создает набор действий по перезаписи для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="4b56d-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="4b56d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b56d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b56d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b56d-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="4b56d-109">Эта команда создает конфигурацию заглавного правила переписыванием и сохраняет результат в переменной с именем $hc.</span><span class="sxs-lookup"><span data-stu-id="4b56d-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="4b56d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b56d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b56d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b56d-111">-DefaultProfile</span></span>
<span data-ttu-id="4b56d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b56d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b56d-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="4b56d-113">-HeaderName</span></span>
<span data-ttu-id="4b56d-114">Имя переописываемого загона</span><span class="sxs-lookup"><span data-stu-id="4b56d-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="4b56d-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="4b56d-115">-HeaderValue</span></span>
<span data-ttu-id="4b56d-116">Значение в заданный набор для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="4b56d-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="4b56d-117">Если этот замещен, заглавная заглавная будет удалена</span><span class="sxs-lookup"><span data-stu-id="4b56d-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b56d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b56d-118">CommonParameters</span></span>
<span data-ttu-id="4b56d-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b56d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b56d-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b56d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b56d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b56d-121">INPUTS</span></span>

### <span data-ttu-id="4b56d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="4b56d-122">None</span></span>

## <span data-ttu-id="4b56d-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b56d-123">OUTPUTS</span></span>

### <span data-ttu-id="4b56d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b56d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="4b56d-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b56d-125">NOTES</span></span>

## <span data-ttu-id="4b56d-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b56d-126">RELATED LINKS</span></span>

[<span data-ttu-id="4b56d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4b56d-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4b56d-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4b56d-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4b56d-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4b56d-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4b56d-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="4b56d-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4b56d-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
