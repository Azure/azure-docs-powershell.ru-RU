---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519837"
---
# <span data-ttu-id="960f6-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="960f6-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="960f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="960f6-102">SYNOPSIS</span></span>
<span data-ttu-id="960f6-103">Получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="960f6-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="960f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="960f6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="960f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="960f6-105">DESCRIPTION</span></span>
<span data-ttu-id="960f6-106">Доступен набор пакетов аналитики для **get-AzOperationalInsightsIntelligencePack.**</span><span class="sxs-lookup"><span data-stu-id="960f6-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="960f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="960f6-107">EXAMPLES</span></span>

### <span data-ttu-id="960f6-108">Пример 1. Получить пакеты аналитики</span><span class="sxs-lookup"><span data-stu-id="960f6-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="960f6-109">Эта команда получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="960f6-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="960f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="960f6-110">PARAMETERS</span></span>

### <span data-ttu-id="960f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960f6-111">-DefaultProfile</span></span>
<span data-ttu-id="960f6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="960f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="960f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="960f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="960f6-114">Указывает имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="960f6-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="960f6-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="960f6-115">-WorkspaceName</span></span>
<span data-ttu-id="960f6-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="960f6-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="960f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960f6-117">CommonParameters</span></span>
<span data-ttu-id="960f6-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="960f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960f6-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="960f6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960f6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="960f6-120">INPUTS</span></span>

### <span data-ttu-id="960f6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="960f6-121">System.String</span></span>

## <span data-ttu-id="960f6-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="960f6-122">OUTPUTS</span></span>

### <span data-ttu-id="960f6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="960f6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="960f6-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="960f6-124">NOTES</span></span>

## <span data-ttu-id="960f6-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="960f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="960f6-126">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="960f6-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


