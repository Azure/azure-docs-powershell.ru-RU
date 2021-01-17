---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397772"
---
# <span data-ttu-id="5fae4-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5fae4-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="5fae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fae4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fae4-103">Подробные сведения о группах управления, подключенных к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5fae4-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="5fae4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fae4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fae4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fae4-105">DESCRIPTION</span></span>
<span data-ttu-id="5fae4-106">Командлет **Get-AzOperationalInsightsWorkspaceManagementGroup** содержит список групп управления, подключенных к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5fae4-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="5fae4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fae4-107">EXAMPLES</span></span>

### <span data-ttu-id="5fae4-108">Пример 1. Получить группы управления по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="5fae4-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="5fae4-109">Эта команда получает группы управления для рабочей области MyWorkspace в группу ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5fae4-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="5fae4-110">Пример 2. Получить группы управления с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="5fae4-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="5fae4-111">Эта команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace, а затем передает ее текущему командлету, который получает группы управления для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5fae4-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="5fae4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fae4-112">PARAMETERS</span></span>

### <span data-ttu-id="5fae4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fae4-113">-DefaultProfile</span></span>
<span data-ttu-id="5fae4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5fae4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fae4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5fae4-115">-Name</span></span>
<span data-ttu-id="5fae4-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5fae4-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="5fae4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fae4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fae4-118">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5fae4-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="5fae4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fae4-119">CommonParameters</span></span>
<span data-ttu-id="5fae4-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fae4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fae4-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fae4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fae4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fae4-122">INPUTS</span></span>

### <span data-ttu-id="5fae4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5fae4-123">System.String</span></span>

## <span data-ttu-id="5fae4-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fae4-124">OUTPUTS</span></span>

### <span data-ttu-id="5fae4-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5fae4-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="5fae4-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fae4-126">NOTES</span></span>

## <span data-ttu-id="5fae4-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fae4-127">RELATED LINKS</span></span>

[<span data-ttu-id="5fae4-128">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5fae4-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="5fae4-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5fae4-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


