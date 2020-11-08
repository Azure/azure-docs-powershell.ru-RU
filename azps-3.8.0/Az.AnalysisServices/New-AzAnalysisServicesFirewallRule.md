---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065649"
---
# <span data-ttu-id="c8df6-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8df6-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="c8df6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8df6-102">SYNOPSIS</span></span>
<span data-ttu-id="c8df6-103">Создание правила брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="c8df6-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="c8df6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8df6-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8df6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8df6-105">DESCRIPTION</span></span>
<span data-ttu-id="c8df6-106">New-AzAnalysisServicesFirewallRule создает новый объект правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c8df6-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="c8df6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8df6-107">EXAMPLES</span></span>

### <span data-ttu-id="c8df6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8df6-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="c8df6-109">Создание правила брандмауэра с именем rule1 с начальным диапазоном 0.0.0.0 и конечным диапазоном 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="c8df6-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="c8df6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8df6-110">PARAMETERS</span></span>

### <span data-ttu-id="c8df6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8df6-111">-DefaultProfile</span></span>
<span data-ttu-id="c8df6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8df6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8df6-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="c8df6-113">-FirewallRuleName</span></span>
<span data-ttu-id="c8df6-114">Имя правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c8df6-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8df6-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="c8df6-115">-RangeEnd</span></span>
<span data-ttu-id="c8df6-116">Конец диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c8df6-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8df6-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="c8df6-117">-RangeStart</span></span>
<span data-ttu-id="c8df6-118">Начало диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c8df6-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8df6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8df6-119">CommonParameters</span></span>
<span data-ttu-id="c8df6-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8df6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8df6-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8df6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8df6-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8df6-122">INPUTS</span></span>

### <span data-ttu-id="c8df6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c8df6-123">System.String</span></span>

## <span data-ttu-id="c8df6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8df6-124">OUTPUTS</span></span>

### <span data-ttu-id="c8df6-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8df6-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="c8df6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8df6-126">NOTES</span></span>

## <span data-ttu-id="c8df6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8df6-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8df6-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="c8df6-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)