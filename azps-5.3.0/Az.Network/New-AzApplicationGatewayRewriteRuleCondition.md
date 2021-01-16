---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421836"
---
# <span data-ttu-id="b270c-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b270c-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="b270c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b270c-102">SYNOPSIS</span></span>
<span data-ttu-id="b270c-103">Добавляет условие для шлюза приложения в условие RewriteRule.</span><span class="sxs-lookup"><span data-stu-id="b270c-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="b270c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b270c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b270c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b270c-105">DESCRIPTION</span></span>
<span data-ttu-id="b270c-106">**Cmdlet AzApplicationGatewayRewriteRuleCondition** создает условие правила переописи для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b270c-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="b270c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b270c-107">EXAMPLES</span></span>

### <span data-ttu-id="b270c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b270c-108">Example 1</span></span>
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
<span data-ttu-id="b270c-109">Эта команда создает условие в правиле переписывание и сохраняет результат в переменной с $condition.</span><span class="sxs-lookup"><span data-stu-id="b270c-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="b270c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b270c-110">PARAMETERS</span></span>

### <span data-ttu-id="b270c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b270c-111">-DefaultProfile</span></span>
<span data-ttu-id="b270c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b270c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b270c-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="b270c-113">-IgnoreCase</span></span>
<span data-ttu-id="b270c-114">Как настроить этот флажок, чтобы игнорировать дело в шаблоне</span><span class="sxs-lookup"><span data-stu-id="b270c-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="b270c-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="b270c-115">-Negate</span></span>
<span data-ttu-id="b270c-116">Установите этот флажок, чтобы отменять проверку условий.</span><span class="sxs-lookup"><span data-stu-id="b270c-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="b270c-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="b270c-117">-Pattern</span></span>
<span data-ttu-id="b270c-118">Шаблон, который нужно найти в заглавной переменной</span><span class="sxs-lookup"><span data-stu-id="b270c-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="b270c-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="b270c-119">-Variable</span></span>
<span data-ttu-id="b270c-120">Имя заголовка, которое нужно настроить для него</span><span class="sxs-lookup"><span data-stu-id="b270c-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="b270c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b270c-121">CommonParameters</span></span>
<span data-ttu-id="b270c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b270c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b270c-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b270c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b270c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b270c-124">INPUTS</span></span>

### <span data-ttu-id="b270c-125">Нет</span><span class="sxs-lookup"><span data-stu-id="b270c-125">None</span></span>

## <span data-ttu-id="b270c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b270c-126">OUTPUTS</span></span>

### <span data-ttu-id="b270c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="b270c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="b270c-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b270c-128">NOTES</span></span>

## <span data-ttu-id="b270c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b270c-129">RELATED LINKS</span></span>
[<span data-ttu-id="b270c-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b270c-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b270c-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b270c-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b270c-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b270c-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b270c-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b270c-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b270c-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b270c-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b270c-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b270c-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b270c-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b270c-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
