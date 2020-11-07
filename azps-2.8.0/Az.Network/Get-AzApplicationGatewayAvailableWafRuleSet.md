---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902526"
---
# <span data-ttu-id="d9761-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="d9761-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="d9761-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9761-102">SYNOPSIS</span></span>
<span data-ttu-id="d9761-103">Получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d9761-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d9761-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9761-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9761-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9761-105">DESCRIPTION</span></span>
<span data-ttu-id="d9761-106">Командлет **Get-AzApplicationGatewayAvailableWafRuleSet** получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d9761-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d9761-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9761-107">EXAMPLES</span></span>

### <span data-ttu-id="d9761-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9761-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="d9761-109">Эти команды возвращают все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d9761-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="d9761-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9761-110">PARAMETERS</span></span>

### <span data-ttu-id="d9761-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9761-111">-DefaultProfile</span></span>
<span data-ttu-id="d9761-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9761-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9761-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9761-113">CommonParameters</span></span>
<span data-ttu-id="d9761-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9761-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9761-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9761-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9761-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9761-116">INPUTS</span></span>

### <span data-ttu-id="d9761-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="d9761-117">None</span></span>

## <span data-ttu-id="d9761-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9761-118">OUTPUTS</span></span>

### <span data-ttu-id="d9761-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="d9761-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="d9761-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9761-120">NOTES</span></span>
<span data-ttu-id="d9761-121">**List-AzApplicationGatewayAvailableWafRuleSets** — псевдоним для командлета **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="d9761-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="d9761-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9761-122">RELATED LINKS</span></span>
