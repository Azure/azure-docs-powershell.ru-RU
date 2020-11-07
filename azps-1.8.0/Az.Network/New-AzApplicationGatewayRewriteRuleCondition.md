---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730387"
---
# <span data-ttu-id="b1fa8-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b1fa8-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="b1fa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fa8-103">Добавляет условие в RewriteRule для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="b1fa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1fa8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1fa8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="b1fa8-106">Командлет **AzApplicationGatewayRewriteRuleCondition** создает условие правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="b1fa8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="b1fa8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1fa8-108">Example 1</span></span>
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
<span data-ttu-id="b1fa8-109">Эта команда создает условие в правиле перезаписи и сохраняет результат в переменной с именем $condition.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="b1fa8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="b1fa8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fa8-111">-DefaultProfile</span></span>
<span data-ttu-id="b1fa8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1fa8-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="b1fa8-113">-IgnoreCase</span></span>
<span data-ttu-id="b1fa8-114">Установка этого флага для игнорирования регистра в шаблоне</span><span class="sxs-lookup"><span data-stu-id="b1fa8-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="b1fa8-115">-Отрицание</span><span class="sxs-lookup"><span data-stu-id="b1fa8-115">-Negate</span></span>
<span data-ttu-id="b1fa8-116">Установка этого флага для отрицания проверки условия</span><span class="sxs-lookup"><span data-stu-id="b1fa8-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="b1fa8-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="b1fa8-117">-Pattern</span></span>
<span data-ttu-id="b1fa8-118">Шаблон для поиска в заголовке переменной</span><span class="sxs-lookup"><span data-stu-id="b1fa8-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="b1fa8-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="b1fa8-119">-Variable</span></span>
<span data-ttu-id="b1fa8-120">Имя заголовка, для которого задается условие</span><span class="sxs-lookup"><span data-stu-id="b1fa8-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="b1fa8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fa8-121">CommonParameters</span></span>
<span data-ttu-id="b1fa8-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1fa8-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fa8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fa8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1fa8-124">INPUTS</span></span>

### <span data-ttu-id="b1fa8-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="b1fa8-125">None</span></span>

## <span data-ttu-id="b1fa8-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1fa8-126">OUTPUTS</span></span>

### <span data-ttu-id="b1fa8-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b1fa8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="b1fa8-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1fa8-128">NOTES</span></span>

## <span data-ttu-id="b1fa8-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1fa8-129">RELATED LINKS</span></span>
[<span data-ttu-id="b1fa8-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1fa8-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1fa8-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1fa8-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1fa8-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1fa8-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b1fa8-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b1fa8-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b1fa8-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
