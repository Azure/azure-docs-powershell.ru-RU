---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952184"
---
# <span data-ttu-id="07af2-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="07af2-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="07af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07af2-102">SYNOPSIS</span></span>
<span data-ttu-id="07af2-103">Создает конфигурацию URL-адреса правила переописи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="07af2-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="07af2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07af2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07af2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07af2-105">DESCRIPTION</span></span>
<span data-ttu-id="07af2-106">Для шлюза приложения Azure создается конфигурация URL-адреса правила перезаписи **для azApplicationGatewayRewriteRuleUrlConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="07af2-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="07af2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07af2-107">EXAMPLES</span></span>

### <span data-ttu-id="07af2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07af2-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="07af2-109">Эта команда создает конфигурацию URL-адреса правила переписыванием и сохраняет результат в переменной с именем $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="07af2-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="07af2-110">Если вы хотите обновить существующие объекты URLConfiguration, создав новую структуру URLConfiguration и назначив новую ссылку свойству URLConfiguration набора действий rewrite Rule Action Set.</span><span class="sxs-lookup"><span data-stu-id="07af2-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="07af2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07af2-111">PARAMETERS</span></span>

### <span data-ttu-id="07af2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07af2-112">-DefaultProfile</span></span>
<span data-ttu-id="07af2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07af2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07af2-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="07af2-114">-ModifiedPath</span></span>
<span data-ttu-id="07af2-115">Значение URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="07af2-115">Url path value.</span></span>

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

### <span data-ttu-id="07af2-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="07af2-116">-ModifiedQueryString</span></span>
<span data-ttu-id="07af2-117">Строка URL-запроса.</span><span class="sxs-lookup"><span data-stu-id="07af2-117">Url query string value.</span></span>

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

### <span data-ttu-id="07af2-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="07af2-118">-Reroute</span></span>
<span data-ttu-id="07af2-119">Пометить, чтобы повторно оценить карту URL-адреса, указанную в правилах маршрутной маршрутки запросов, использующих измененный путь.</span><span class="sxs-lookup"><span data-stu-id="07af2-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07af2-120">CommonParameters</span></span>
<span data-ttu-id="07af2-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07af2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07af2-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07af2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07af2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07af2-123">INPUTS</span></span>

### <span data-ttu-id="07af2-124">Нет</span><span class="sxs-lookup"><span data-stu-id="07af2-124">None</span></span>

## <span data-ttu-id="07af2-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07af2-125">OUTPUTS</span></span>

### <span data-ttu-id="07af2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="07af2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="07af2-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07af2-127">NOTES</span></span>

## <span data-ttu-id="07af2-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07af2-128">RELATED LINKS</span></span>

[<span data-ttu-id="07af2-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07af2-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="07af2-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07af2-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="07af2-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07af2-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="07af2-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07af2-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="07af2-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="07af2-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="07af2-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="07af2-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="07af2-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="07af2-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)