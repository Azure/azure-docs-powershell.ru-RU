---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563192"
---
# <span data-ttu-id="1de01-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1de01-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="1de01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1de01-102">SYNOPSIS</span></span>
<span data-ttu-id="1de01-103">Создание правила брандмауэра служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1de01-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1de01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1de01-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1de01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1de01-105">DESCRIPTION</span></span>
<span data-ttu-id="1de01-106">New-AzureRmAnalysisServicesFirewallRule создает новый объект правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="1de01-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="1de01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1de01-107">EXAMPLES</span></span>

### <span data-ttu-id="1de01-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1de01-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="1de01-109">Создание правила брандмауэра с именем rule1 с начальным диапазоном 0.0.0.0 и конечным диапазоном 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="1de01-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="1de01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1de01-110">PARAMETERS</span></span>

### <span data-ttu-id="1de01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de01-111">-DefaultProfile</span></span>
<span data-ttu-id="1de01-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1de01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de01-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="1de01-113">-FirewallRuleName</span></span>
<span data-ttu-id="1de01-114">Имя правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="1de01-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="1de01-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="1de01-115">-RangeEnd</span></span>
<span data-ttu-id="1de01-116">Конец диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="1de01-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="1de01-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="1de01-117">-RangeStart</span></span>
<span data-ttu-id="1de01-118">Начало диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="1de01-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="1de01-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de01-119">CommonParameters</span></span>
<span data-ttu-id="1de01-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1de01-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de01-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1de01-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de01-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1de01-122">INPUTS</span></span>

### <span data-ttu-id="1de01-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1de01-123">System.String</span></span>

## <span data-ttu-id="1de01-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1de01-124">OUTPUTS</span></span>

### <span data-ttu-id="1de01-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1de01-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="1de01-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1de01-126">NOTES</span></span>

## <span data-ttu-id="1de01-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1de01-127">RELATED LINKS</span></span>

[<span data-ttu-id="1de01-128">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1de01-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
