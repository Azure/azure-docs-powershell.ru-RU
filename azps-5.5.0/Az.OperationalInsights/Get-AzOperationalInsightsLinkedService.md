---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218180"
---
# <span data-ttu-id="5f570-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="5f570-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="5f570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f570-102">SYNOPSIS</span></span>
<span data-ttu-id="5f570-103">Получить или перечислить связанную службу для рабочей области</span><span class="sxs-lookup"><span data-stu-id="5f570-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="5f570-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f570-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f570-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f570-105">DESCRIPTION</span></span>
<span data-ttu-id="5f570-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span><span class="sxs-lookup"><span data-stu-id="5f570-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="5f570-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f570-107">EXAMPLES</span></span>

### <span data-ttu-id="5f570-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f570-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="5f570-109">Получить связанную службу для рабочей области</span><span class="sxs-lookup"><span data-stu-id="5f570-109">Get linked service for workspace</span></span>

## <span data-ttu-id="5f570-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f570-110">PARAMETERS</span></span>

### <span data-ttu-id="5f570-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f570-111">-DefaultProfile</span></span>
<span data-ttu-id="5f570-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f570-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f570-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="5f570-113">-LinkedServiceName</span></span>
<span data-ttu-id="5f570-114">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="5f570-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f570-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f570-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f570-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f570-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f570-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f570-117">-WorkspaceName</span></span>
<span data-ttu-id="5f570-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5f570-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f570-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f570-119">CommonParameters</span></span>
<span data-ttu-id="5f570-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f570-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f570-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f570-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f570-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f570-122">INPUTS</span></span>

### <span data-ttu-id="5f570-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5f570-123">System.String</span></span>

## <span data-ttu-id="5f570-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f570-124">OUTPUTS</span></span>

### <span data-ttu-id="5f570-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5f570-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="5f570-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f570-126">NOTES</span></span>

## <span data-ttu-id="5f570-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f570-127">RELATED LINKS</span></span>
