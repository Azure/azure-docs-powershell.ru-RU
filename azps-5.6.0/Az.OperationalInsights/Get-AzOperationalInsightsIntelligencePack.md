---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965624"
---
# <span data-ttu-id="dd78a-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="dd78a-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="dd78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd78a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd78a-103">Получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="dd78a-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="dd78a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd78a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd78a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd78a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd78a-106">Доступен набор пакетов аналитики для **get-AzOperationalInsightsIntelligencePack.**</span><span class="sxs-lookup"><span data-stu-id="dd78a-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="dd78a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd78a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd78a-108">Пример 1. Получить пакеты аналитики</span><span class="sxs-lookup"><span data-stu-id="dd78a-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="dd78a-109">Эта команда получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="dd78a-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="dd78a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd78a-110">PARAMETERS</span></span>

### <span data-ttu-id="dd78a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd78a-111">-DefaultProfile</span></span>
<span data-ttu-id="dd78a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd78a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd78a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd78a-113">-ResourceGroupName</span></span>
<span data-ttu-id="dd78a-114">Указывает имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="dd78a-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="dd78a-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dd78a-115">-WorkspaceName</span></span>
<span data-ttu-id="dd78a-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="dd78a-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="dd78a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd78a-117">CommonParameters</span></span>
<span data-ttu-id="dd78a-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd78a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd78a-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd78a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd78a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd78a-120">INPUTS</span></span>

### <span data-ttu-id="dd78a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dd78a-121">System.String</span></span>

## <span data-ttu-id="dd78a-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd78a-122">OUTPUTS</span></span>

### <span data-ttu-id="dd78a-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="dd78a-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="dd78a-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd78a-124">NOTES</span></span>

## <span data-ttu-id="dd78a-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd78a-125">RELATED LINKS</span></span>

[<span data-ttu-id="dd78a-126">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="dd78a-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


