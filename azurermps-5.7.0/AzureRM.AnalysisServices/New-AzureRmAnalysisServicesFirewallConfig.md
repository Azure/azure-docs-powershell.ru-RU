---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733292"
---
# <span data-ttu-id="eaff0-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="eaff0-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="eaff0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaff0-102">SYNOPSIS</span></span>
<span data-ttu-id="eaff0-103">Создает новую конфигурацию брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="eaff0-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaff0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaff0-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="eaff0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaff0-105">DESCRIPTION</span></span>
<span data-ttu-id="eaff0-106">New-AzureRmAnalysisServicesFirewallConfig создает новый объект конфигурации брандмауэра</span><span class="sxs-lookup"><span data-stu-id="eaff0-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="eaff0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaff0-107">EXAMPLES</span></span>

### <span data-ttu-id="eaff0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eaff0-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="eaff0-109">Создание конфигурации правила брандмауэра без включения службы Power BI.</span><span class="sxs-lookup"><span data-stu-id="eaff0-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="eaff0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaff0-110">PARAMETERS</span></span>

### <span data-ttu-id="eaff0-111">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="eaff0-111">-EnablePowerBIService</span></span>
<span data-ttu-id="eaff0-112">Флаг, указывающий, включена ли служба PowerBI</span><span class="sxs-lookup"><span data-stu-id="eaff0-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaff0-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="eaff0-113">-FirewallRules</span></span>
<span data-ttu-id="eaff0-114">Список правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="eaff0-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="eaff0-115">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaff0-115">INPUTS</span></span>

## <span data-ttu-id="eaff0-116">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaff0-116">OUTPUTS</span></span>

### <span data-ttu-id="eaff0-117">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="eaff0-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="eaff0-118">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaff0-118">RELATED LINKS</span></span>

[<span data-ttu-id="eaff0-119">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="eaff0-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
