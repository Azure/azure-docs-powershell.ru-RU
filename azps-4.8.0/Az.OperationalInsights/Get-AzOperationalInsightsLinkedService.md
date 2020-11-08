---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242962"
---
# <span data-ttu-id="cf225-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="cf225-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="cf225-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf225-102">SYNOPSIS</span></span>
<span data-ttu-id="cf225-103">Получение и перечисление связанной службы для рабочей области</span><span class="sxs-lookup"><span data-stu-id="cf225-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="cf225-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf225-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf225-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf225-105">DESCRIPTION</span></span>
<span data-ttu-id="cf225-106">Получение или перечисление связанной службы для рабочей области, список, если не указан "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="cf225-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="cf225-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf225-107">EXAMPLES</span></span>

### <span data-ttu-id="cf225-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf225-108">Example 1</span></span>
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

<span data-ttu-id="cf225-109">Получение связанной службы для рабочей области</span><span class="sxs-lookup"><span data-stu-id="cf225-109">Get linked service for workspace</span></span>

## <span data-ttu-id="cf225-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf225-110">PARAMETERS</span></span>

### <span data-ttu-id="cf225-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf225-111">-DefaultProfile</span></span>
<span data-ttu-id="cf225-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf225-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf225-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="cf225-113">-LinkedServiceName</span></span>
<span data-ttu-id="cf225-114">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="cf225-114">The linked service name.</span></span>

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

### <span data-ttu-id="cf225-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf225-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf225-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf225-116">The resource group name.</span></span>

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

### <span data-ttu-id="cf225-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf225-117">-WorkspaceName</span></span>
<span data-ttu-id="cf225-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cf225-118">The workspace name.</span></span>

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

### <span data-ttu-id="cf225-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf225-119">CommonParameters</span></span>
<span data-ttu-id="cf225-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf225-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf225-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf225-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf225-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf225-122">INPUTS</span></span>

### <span data-ttu-id="cf225-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cf225-123">System.String</span></span>

## <span data-ttu-id="cf225-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf225-124">OUTPUTS</span></span>

### <span data-ttu-id="cf225-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="cf225-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="cf225-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf225-126">NOTES</span></span>

## <span data-ttu-id="cf225-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf225-127">RELATED LINKS</span></span>
