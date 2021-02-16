---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216473"
---
# <span data-ttu-id="1bf34-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1bf34-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="1bf34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf34-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf34-103">Создание правила брандмауэра Служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1bf34-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="1bf34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1bf34-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf34-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bf34-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf34-106">Система New-AzAnalysisServicesFirewallRule создает объект правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="1bf34-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="1bf34-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1bf34-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf34-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1bf34-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="1bf34-109">Создает правило брандмауэра с именем "Правило1" с диапазоном начала 0.0.0.0 и конечным диапазоном 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="1bf34-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="1bf34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf34-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf34-111">-DefaultProfile</span></span>
<span data-ttu-id="1bf34-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf34-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf34-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="1bf34-113">-FirewallRuleName</span></span>
<span data-ttu-id="1bf34-114">Имя правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="1bf34-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="1bf34-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="1bf34-115">-RangeEnd</span></span>
<span data-ttu-id="1bf34-116">Конец действия правила брандмауэра в диапазоне</span><span class="sxs-lookup"><span data-stu-id="1bf34-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="1bf34-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="1bf34-117">-RangeStart</span></span>
<span data-ttu-id="1bf34-118">Начало действия правила брандмауэра в диапазоне</span><span class="sxs-lookup"><span data-stu-id="1bf34-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="1bf34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf34-119">CommonParameters</span></span>
<span data-ttu-id="1bf34-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf34-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf34-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf34-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf34-122">INPUTS</span></span>

### <span data-ttu-id="1bf34-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf34-123">System.String</span></span>

## <span data-ttu-id="1bf34-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf34-124">OUTPUTS</span></span>

### <span data-ttu-id="1bf34-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1bf34-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="1bf34-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1bf34-126">NOTES</span></span>

## <span data-ttu-id="1bf34-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bf34-127">RELATED LINKS</span></span>

[<span data-ttu-id="1bf34-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1bf34-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)