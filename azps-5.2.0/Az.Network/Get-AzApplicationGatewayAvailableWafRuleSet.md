---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407188"
---
# <span data-ttu-id="ba511-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba511-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="ba511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba511-102">SYNOPSIS</span></span>
<span data-ttu-id="ba511-103">Получает все доступные наборы правил брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ba511-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ba511-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba511-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba511-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba511-105">DESCRIPTION</span></span>
<span data-ttu-id="ba511-106">С **помощью cmdlet Get-AzApplicationGatewayAvailableWafRuleSet** можно получить все доступные наборы правил брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ba511-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ba511-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba511-107">EXAMPLES</span></span>

### <span data-ttu-id="ba511-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba511-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="ba511-109">Эти команды возвращают все доступные наборы правил брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ba511-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="ba511-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba511-110">PARAMETERS</span></span>

### <span data-ttu-id="ba511-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba511-111">-DefaultProfile</span></span>
<span data-ttu-id="ba511-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba511-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba511-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba511-113">CommonParameters</span></span>
<span data-ttu-id="ba511-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba511-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba511-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba511-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba511-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba511-116">INPUTS</span></span>

### <span data-ttu-id="ba511-117">Нет</span><span class="sxs-lookup"><span data-stu-id="ba511-117">None</span></span>

## <span data-ttu-id="ba511-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba511-118">OUTPUTS</span></span>

### <span data-ttu-id="ba511-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="ba511-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="ba511-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba511-120">NOTES</span></span>
<span data-ttu-id="ba511-121">**List-AzApplicationGatewayAvailableWafRuleSets** — псевдоним для cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="ba511-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="ba511-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba511-122">RELATED LINKS</span></span>
