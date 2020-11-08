---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: b628f0050ab0aa4b16864b510f4426b940226ec5
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077273"
---
# <span data-ttu-id="d52e2-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d52e2-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="d52e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d52e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d52e2-103">Получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="d52e2-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d52e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d52e2-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d52e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d52e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d52e2-106">Командлет **Get-AzOperationalInsightsIntelligencePack** получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="d52e2-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d52e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d52e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d52e2-108">Пример 1: получение пакетов для аналитики</span><span class="sxs-lookup"><span data-stu-id="d52e2-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d52e2-109">Эта команда получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="d52e2-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="d52e2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d52e2-110">PARAMETERS</span></span>

### <span data-ttu-id="d52e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52e2-111">-DefaultProfile</span></span>
<span data-ttu-id="d52e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d52e2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d52e2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52e2-113">-ResourceGroupName</span></span>
<span data-ttu-id="d52e2-114">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d52e2-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d52e2-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d52e2-115">-WorkspaceName</span></span>
<span data-ttu-id="d52e2-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d52e2-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d52e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52e2-117">CommonParameters</span></span>
<span data-ttu-id="d52e2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d52e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52e2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d52e2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52e2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d52e2-120">INPUTS</span></span>

### <span data-ttu-id="d52e2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d52e2-121">System.String</span></span>

## <span data-ttu-id="d52e2-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d52e2-122">OUTPUTS</span></span>

### <span data-ttu-id="d52e2-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d52e2-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="d52e2-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d52e2-124">NOTES</span></span>

## <span data-ttu-id="d52e2-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d52e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="d52e2-126">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="d52e2-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


