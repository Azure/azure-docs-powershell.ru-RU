---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720208"
---
# <span data-ttu-id="55ca5-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="55ca5-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="55ca5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="55ca5-103">Создает новую конфигурацию брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="55ca5-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="55ca5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55ca5-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ca5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="55ca5-106">New-AzAnalysisServicesFirewallConfig создает новый объект конфигурации брандмауэра</span><span class="sxs-lookup"><span data-stu-id="55ca5-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="55ca5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="55ca5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55ca5-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="55ca5-109">Создает объект конфигурации брандмауэра с двумя правилами, а также включает доступ из службы Power BI.</span><span class="sxs-lookup"><span data-stu-id="55ca5-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="55ca5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55ca5-110">PARAMETERS</span></span>

### <span data-ttu-id="55ca5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ca5-111">-DefaultProfile</span></span>
<span data-ttu-id="55ca5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55ca5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ca5-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="55ca5-113">-EnablePowerBIService</span></span>
<span data-ttu-id="55ca5-114">Флаг, указывающий, разрешено ли брандмауэру доступ из Power BI</span><span class="sxs-lookup"><span data-stu-id="55ca5-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="55ca5-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="55ca5-115">-FirewallRule</span></span>
<span data-ttu-id="55ca5-116">Список правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="55ca5-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="55ca5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ca5-117">CommonParameters</span></span>
<span data-ttu-id="55ca5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55ca5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ca5-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ca5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ca5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55ca5-120">INPUTS</span></span>

### <span data-ttu-id="55ca5-121">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. AnalysisServices. AnalysisServices, версия = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="55ca5-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="55ca5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ca5-122">OUTPUTS</span></span>

### <span data-ttu-id="55ca5-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="55ca5-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="55ca5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="55ca5-124">NOTES</span></span>

## <span data-ttu-id="55ca5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55ca5-125">RELATED LINKS</span></span>

[<span data-ttu-id="55ca5-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55ca5-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)