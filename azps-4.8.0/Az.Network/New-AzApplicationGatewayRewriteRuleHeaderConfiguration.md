---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243021"
---
# <span data-ttu-id="eb724-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb724-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="eb724-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb724-102">SYNOPSIS</span></span>
<span data-ttu-id="eb724-103">Создает конфигурацию заголовка правила перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="eb724-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="eb724-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb724-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb724-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb724-105">DESCRIPTION</span></span>
<span data-ttu-id="eb724-106">Командлет **AzApplicationGatewayRewriteRuleHeaderConfiguration** создает набор действий правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="eb724-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="eb724-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb724-107">EXAMPLES</span></span>

### <span data-ttu-id="eb724-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb724-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="eb724-109">Эта команда создает конфигурацию заголовка правила перезаписи и сохраняет результат в переменной с именем $hc.</span><span class="sxs-lookup"><span data-stu-id="eb724-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="eb724-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb724-110">PARAMETERS</span></span>

### <span data-ttu-id="eb724-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb724-111">-DefaultProfile</span></span>
<span data-ttu-id="eb724-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb724-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb724-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="eb724-113">-HeaderName</span></span>
<span data-ttu-id="eb724-114">Имя заголовка для перезаписи</span><span class="sxs-lookup"><span data-stu-id="eb724-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="eb724-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="eb724-115">-HeaderValue</span></span>
<span data-ttu-id="eb724-116">Значение заголовка в множество для заданных имен заголовков.</span><span class="sxs-lookup"><span data-stu-id="eb724-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="eb724-117">Верхний колонтитул будет удален, если он не указан</span><span class="sxs-lookup"><span data-stu-id="eb724-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="eb724-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb724-118">CommonParameters</span></span>
<span data-ttu-id="eb724-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb724-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb724-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb724-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb724-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb724-121">INPUTS</span></span>

### <span data-ttu-id="eb724-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb724-122">None</span></span>

## <span data-ttu-id="eb724-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb724-123">OUTPUTS</span></span>

### <span data-ttu-id="eb724-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb724-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="eb724-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb724-125">NOTES</span></span>

## <span data-ttu-id="eb724-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb724-126">RELATED LINKS</span></span>

[<span data-ttu-id="eb724-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb724-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb724-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb724-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb724-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb724-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb724-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb724-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb724-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb724-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb724-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eb724-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="eb724-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eb724-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)