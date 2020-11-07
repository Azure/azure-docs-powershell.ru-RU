---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732500"
---
# <span data-ttu-id="775d2-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="775d2-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="775d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="775d2-102">SYNOPSIS</span></span>
<span data-ttu-id="775d2-103">Создает новую конфигурацию брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="775d2-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="775d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="775d2-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="775d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="775d2-105">DESCRIPTION</span></span>
<span data-ttu-id="775d2-106">New-AzureRmAnalysisServicesFirewallConfig создает новый объект конфигурации брандмауэра</span><span class="sxs-lookup"><span data-stu-id="775d2-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="775d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="775d2-107">EXAMPLES</span></span>

### <span data-ttu-id="775d2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="775d2-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="775d2-109">Создает объект конфигурации брандмауэра с двумя правилами, а также включает доступ из службы Power BI.</span><span class="sxs-lookup"><span data-stu-id="775d2-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="775d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="775d2-110">PARAMETERS</span></span>

### <span data-ttu-id="775d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775d2-111">-DefaultProfile</span></span>
<span data-ttu-id="775d2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="775d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775d2-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="775d2-113">-EnablePowerBIService</span></span>
<span data-ttu-id="775d2-114">Флаг, указывающий, разрешено ли брандмауэру доступ из Power BI</span><span class="sxs-lookup"><span data-stu-id="775d2-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="775d2-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="775d2-115">-FirewallRule</span></span>
<span data-ttu-id="775d2-116">Список правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="775d2-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775d2-117">CommonParameters</span></span>
<span data-ttu-id="775d2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="775d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775d2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775d2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="775d2-120">INPUTS</span></span>

### <span data-ttu-id="775d2-121">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. AnalysisServices, Version = 0.6.11.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="775d2-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="775d2-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="775d2-122">OUTPUTS</span></span>

### <span data-ttu-id="775d2-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="775d2-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="775d2-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="775d2-124">NOTES</span></span>

## <span data-ttu-id="775d2-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="775d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="775d2-126">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="775d2-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
