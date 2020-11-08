---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236054"
---
# <span data-ttu-id="8ddce-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ddce-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="8ddce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ddce-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddce-103">Создание конфигурации URL-адреса правила перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8ddce-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="8ddce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ddce-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ddce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ddce-105">DESCRIPTION</span></span>
<span data-ttu-id="8ddce-106">Командлет **AzApplicationGatewayRewriteRuleUrlConfiguration** создает конфигурацию URL-адреса правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddce-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="8ddce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ddce-107">EXAMPLES</span></span>

### <span data-ttu-id="8ddce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ddce-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="8ddce-109">Эта команда создает конфигурацию URL-адреса правила перезаписи и сохраняет результат в переменной с именем $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ddce-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="8ddce-110">Если вы хотите обновить существующий UrlConfiguration, вы можете создать новый UrlConfiguration и назначить новый UrlConfiguration свойству UrlConfiguration набора действий правила перезаписи.</span><span class="sxs-lookup"><span data-stu-id="8ddce-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="8ddce-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ddce-111">PARAMETERS</span></span>

### <span data-ttu-id="8ddce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddce-112">-DefaultProfile</span></span>
<span data-ttu-id="8ddce-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddce-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ddce-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="8ddce-114">-ModifiedPath</span></span>
<span data-ttu-id="8ddce-115">URL-путь значения.</span><span class="sxs-lookup"><span data-stu-id="8ddce-115">Url path value.</span></span>

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

### <span data-ttu-id="8ddce-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="8ddce-116">-ModifiedQueryString</span></span>
<span data-ttu-id="8ddce-117">Строковое значение URL-запроса.</span><span class="sxs-lookup"><span data-stu-id="8ddce-117">Url query string value.</span></span>

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

### <span data-ttu-id="8ddce-118">-Изменение направления</span><span class="sxs-lookup"><span data-stu-id="8ddce-118">-Reroute</span></span>
<span data-ttu-id="8ddce-119">Пометка для повторной оценки карты URL-пути, указанной в правилах маршрутизации запросов на основе пути с помощью измененного пути.</span><span class="sxs-lookup"><span data-stu-id="8ddce-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="8ddce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddce-120">CommonParameters</span></span>
<span data-ttu-id="8ddce-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ddce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddce-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ddce-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddce-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ddce-123">INPUTS</span></span>

### <span data-ttu-id="8ddce-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="8ddce-124">None</span></span>

## <span data-ttu-id="8ddce-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ddce-125">OUTPUTS</span></span>

### <span data-ttu-id="8ddce-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ddce-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="8ddce-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ddce-127">NOTES</span></span>

## <span data-ttu-id="8ddce-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ddce-128">RELATED LINKS</span></span>

[<span data-ttu-id="8ddce-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8ddce-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8ddce-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8ddce-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8ddce-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8ddce-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8ddce-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8ddce-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8ddce-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)