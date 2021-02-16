---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233828"
---
# <span data-ttu-id="270b8-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="270b8-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="270b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270b8-102">SYNOPSIS</span></span>
<span data-ttu-id="270b8-103">Создание брандмауэра Analysis Services</span><span class="sxs-lookup"><span data-stu-id="270b8-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="270b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="270b8-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="270b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="270b8-105">DESCRIPTION</span></span>
<span data-ttu-id="270b8-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span><span class="sxs-lookup"><span data-stu-id="270b8-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="270b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="270b8-107">EXAMPLES</span></span>

### <span data-ttu-id="270b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="270b8-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="270b8-109">Создает объект брандмауэра с двумя правилами, одновременно предоставляя доступ из службы Power BI.</span><span class="sxs-lookup"><span data-stu-id="270b8-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="270b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="270b8-110">PARAMETERS</span></span>

### <span data-ttu-id="270b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270b8-111">-DefaultProfile</span></span>
<span data-ttu-id="270b8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="270b8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270b8-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="270b8-113">-EnablePowerBIService</span></span>
<span data-ttu-id="270b8-114">Флаг, позволяющий указать, разрешает ли брандмауэр доступ из Power BI</span><span class="sxs-lookup"><span data-stu-id="270b8-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="270b8-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="270b8-115">-FirewallRule</span></span>
<span data-ttu-id="270b8-116">Список правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="270b8-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="270b8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270b8-117">CommonParameters</span></span>
<span data-ttu-id="270b8-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270b8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270b8-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270b8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270b8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="270b8-120">INPUTS</span></span>

### <span data-ttu-id="270b8-121">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="270b8-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="270b8-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="270b8-122">OUTPUTS</span></span>

### <span data-ttu-id="270b8-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="270b8-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="270b8-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="270b8-124">NOTES</span></span>

## <span data-ttu-id="270b8-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="270b8-125">RELATED LINKS</span></span>

[<span data-ttu-id="270b8-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="270b8-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)