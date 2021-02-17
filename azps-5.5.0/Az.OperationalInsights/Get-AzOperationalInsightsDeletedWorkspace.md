---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227276"
---
# <span data-ttu-id="124eb-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="124eb-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="124eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="124eb-102">SYNOPSIS</span></span>
<span data-ttu-id="124eb-103">Список удаленных рабочей области.</span><span class="sxs-lookup"><span data-stu-id="124eb-103">List deleted workspaces.</span></span>

## <span data-ttu-id="124eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="124eb-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="124eb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="124eb-105">DESCRIPTION</span></span>
<span data-ttu-id="124eb-106">Список удаленных рабочей области.</span><span class="sxs-lookup"><span data-stu-id="124eb-106">List deleted workspaces.</span></span>

## <span data-ttu-id="124eb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="124eb-107">EXAMPLES</span></span>

### <span data-ttu-id="124eb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="124eb-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="124eb-109">Список удаленных рабочей области.</span><span class="sxs-lookup"><span data-stu-id="124eb-109">List deleted workspaces.</span></span>

## <span data-ttu-id="124eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="124eb-110">PARAMETERS</span></span>

### <span data-ttu-id="124eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124eb-111">-DefaultProfile</span></span>
<span data-ttu-id="124eb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="124eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="124eb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124eb-113">-ResourceGroupName</span></span>
<span data-ttu-id="124eb-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="124eb-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124eb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124eb-115">CommonParameters</span></span>
<span data-ttu-id="124eb-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="124eb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124eb-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="124eb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124eb-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="124eb-118">INPUTS</span></span>

### <span data-ttu-id="124eb-119">System.String</span><span class="sxs-lookup"><span data-stu-id="124eb-119">System.String</span></span>

## <span data-ttu-id="124eb-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="124eb-120">OUTPUTS</span></span>

### <span data-ttu-id="124eb-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="124eb-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="124eb-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="124eb-122">NOTES</span></span>

## <span data-ttu-id="124eb-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="124eb-123">RELATED LINKS</span></span>
