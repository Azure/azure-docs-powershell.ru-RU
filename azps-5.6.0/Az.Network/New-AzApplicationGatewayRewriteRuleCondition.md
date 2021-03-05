---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001144"
---
# <span data-ttu-id="f0391-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="f0391-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="f0391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0391-102">SYNOPSIS</span></span>
<span data-ttu-id="f0391-103">Добавляет условие для шлюза приложения в условие RewriteRule.</span><span class="sxs-lookup"><span data-stu-id="f0391-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="f0391-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0391-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0391-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0391-105">DESCRIPTION</span></span>
<span data-ttu-id="f0391-106">Для шлюза приложения Azure создается условие правила переописи для **azApplicationGatewayRewriteRuleCondition.**</span><span class="sxs-lookup"><span data-stu-id="f0391-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="f0391-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0391-107">EXAMPLES</span></span>

### <span data-ttu-id="f0391-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0391-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="f0391-109">Эта команда создает условие в правиле переописи и сохраняет результат в переменной с $condition.</span><span class="sxs-lookup"><span data-stu-id="f0391-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="f0391-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0391-110">PARAMETERS</span></span>

### <span data-ttu-id="f0391-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0391-111">-DefaultProfile</span></span>
<span data-ttu-id="f0391-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0391-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0391-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="f0391-113">-IgnoreCase</span></span>
<span data-ttu-id="f0391-114">Установите этот флажок, чтобы игнорировать дело в шаблоне</span><span class="sxs-lookup"><span data-stu-id="f0391-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0391-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="f0391-115">-Negate</span></span>
<span data-ttu-id="f0391-116">Установить этот флажок для отмены проверки условия</span><span class="sxs-lookup"><span data-stu-id="f0391-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0391-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="f0391-117">-Pattern</span></span>
<span data-ttu-id="f0391-118">Шаблон, который нужно найти в заглавной переменной</span><span class="sxs-lookup"><span data-stu-id="f0391-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0391-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="f0391-119">-Variable</span></span>
<span data-ttu-id="f0391-120">Имя заголовка, которое нужно настроить для него</span><span class="sxs-lookup"><span data-stu-id="f0391-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0391-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0391-121">CommonParameters</span></span>
<span data-ttu-id="f0391-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0391-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0391-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0391-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0391-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0391-124">INPUTS</span></span>

### <span data-ttu-id="f0391-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f0391-125">None</span></span>

## <span data-ttu-id="f0391-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0391-126">OUTPUTS</span></span>

### <span data-ttu-id="f0391-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="f0391-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="f0391-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0391-128">NOTES</span></span>

## <span data-ttu-id="f0391-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0391-129">RELATED LINKS</span></span>
[<span data-ttu-id="f0391-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0391-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0391-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0391-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0391-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0391-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0391-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0391-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0391-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0391-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f0391-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f0391-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f0391-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f0391-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
