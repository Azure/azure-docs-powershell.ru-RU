---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567028"
---
# <span data-ttu-id="65c54-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="65c54-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="65c54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65c54-102">SYNOPSIS</span></span>
<span data-ttu-id="65c54-103">Создание правила брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="65c54-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65c54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65c54-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="65c54-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c54-105">DESCRIPTION</span></span>
<span data-ttu-id="65c54-106">New-AzureRmAnalysisServicesFirewallRule создает новый объект правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="65c54-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="65c54-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65c54-107">EXAMPLES</span></span>

### <span data-ttu-id="65c54-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65c54-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="65c54-109">Создание правила брандмауэра с именем rule1 с начальным диапазоном 0.0.0.0 и конечным диапазоном 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="65c54-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="65c54-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65c54-110">PARAMETERS</span></span>

### <span data-ttu-id="65c54-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="65c54-111">-FirewallRuleName</span></span>
<span data-ttu-id="65c54-112">Имя правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="65c54-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c54-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="65c54-113">-RangeStart</span></span>
<span data-ttu-id="65c54-114">Начало диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="65c54-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c54-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="65c54-115">-RangeEnd</span></span>
<span data-ttu-id="65c54-116">Конец диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="65c54-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="65c54-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65c54-117">INPUTS</span></span>

## <span data-ttu-id="65c54-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c54-118">OUTPUTS</span></span>

### <span data-ttu-id="65c54-119">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="65c54-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="65c54-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65c54-120">RELATED LINKS</span></span>

[<span data-ttu-id="65c54-121">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="65c54-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
