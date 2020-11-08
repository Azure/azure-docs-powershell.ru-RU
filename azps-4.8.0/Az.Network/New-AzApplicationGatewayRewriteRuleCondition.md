---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078915"
---
# <span data-ttu-id="e050d-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e050d-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="e050d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e050d-102">SYNOPSIS</span></span>
<span data-ttu-id="e050d-103">Добавляет условие в RewriteRule для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e050d-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="e050d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e050d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e050d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e050d-105">DESCRIPTION</span></span>
<span data-ttu-id="e050d-106">Командлет **AzApplicationGatewayRewriteRuleCondition** создает условие правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e050d-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="e050d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e050d-107">EXAMPLES</span></span>

### <span data-ttu-id="e050d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e050d-108">Example 1</span></span>
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
<span data-ttu-id="e050d-109">Эта команда создает условие в правиле перезаписи и сохраняет результат в переменной с именем $condition.</span><span class="sxs-lookup"><span data-stu-id="e050d-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="e050d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e050d-110">PARAMETERS</span></span>

### <span data-ttu-id="e050d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e050d-111">-DefaultProfile</span></span>
<span data-ttu-id="e050d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e050d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e050d-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="e050d-113">-IgnoreCase</span></span>
<span data-ttu-id="e050d-114">Установка этого флага для игнорирования регистра в шаблоне</span><span class="sxs-lookup"><span data-stu-id="e050d-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="e050d-115">-Отрицание</span><span class="sxs-lookup"><span data-stu-id="e050d-115">-Negate</span></span>
<span data-ttu-id="e050d-116">Установка этого флага для отрицания проверки условия</span><span class="sxs-lookup"><span data-stu-id="e050d-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="e050d-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="e050d-117">-Pattern</span></span>
<span data-ttu-id="e050d-118">Шаблон для поиска в заголовке переменной</span><span class="sxs-lookup"><span data-stu-id="e050d-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="e050d-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="e050d-119">-Variable</span></span>
<span data-ttu-id="e050d-120">Имя заголовка, для которого задается условие</span><span class="sxs-lookup"><span data-stu-id="e050d-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="e050d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e050d-121">CommonParameters</span></span>
<span data-ttu-id="e050d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e050d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e050d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e050d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e050d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e050d-124">INPUTS</span></span>

### <span data-ttu-id="e050d-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="e050d-125">None</span></span>

## <span data-ttu-id="e050d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e050d-126">OUTPUTS</span></span>

### <span data-ttu-id="e050d-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e050d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="e050d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e050d-128">NOTES</span></span>

## <span data-ttu-id="e050d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e050d-129">RELATED LINKS</span></span>
[<span data-ttu-id="e050d-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050d-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e050d-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050d-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e050d-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050d-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e050d-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050d-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e050d-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e050d-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e050d-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e050d-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e050d-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e050d-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)