---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416652"
---
# <span data-ttu-id="59786-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="59786-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="59786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59786-102">SYNOPSIS</span></span>
<span data-ttu-id="59786-103">Получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="59786-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="59786-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59786-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59786-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59786-105">DESCRIPTION</span></span>
<span data-ttu-id="59786-106">Доступен набор пакетов аналитики для **get-AzOperationalInsightsIntelligencePack.**</span><span class="sxs-lookup"><span data-stu-id="59786-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="59786-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59786-107">EXAMPLES</span></span>

### <span data-ttu-id="59786-108">Пример 1. Получить пакеты аналитики</span><span class="sxs-lookup"><span data-stu-id="59786-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="59786-109">Эта команда получает доступные пакеты аналитики.</span><span class="sxs-lookup"><span data-stu-id="59786-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="59786-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59786-110">PARAMETERS</span></span>

### <span data-ttu-id="59786-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59786-111">-DefaultProfile</span></span>
<span data-ttu-id="59786-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59786-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59786-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59786-113">-ResourceGroupName</span></span>
<span data-ttu-id="59786-114">Указывает имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="59786-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="59786-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59786-115">-WorkspaceName</span></span>
<span data-ttu-id="59786-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="59786-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="59786-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59786-117">CommonParameters</span></span>
<span data-ttu-id="59786-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59786-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59786-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59786-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59786-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59786-120">INPUTS</span></span>

### <span data-ttu-id="59786-121">System.String</span><span class="sxs-lookup"><span data-stu-id="59786-121">System.String</span></span>

## <span data-ttu-id="59786-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59786-122">OUTPUTS</span></span>

### <span data-ttu-id="59786-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="59786-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="59786-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59786-124">NOTES</span></span>

## <span data-ttu-id="59786-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59786-125">RELATED LINKS</span></span>

[<span data-ttu-id="59786-126">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="59786-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


