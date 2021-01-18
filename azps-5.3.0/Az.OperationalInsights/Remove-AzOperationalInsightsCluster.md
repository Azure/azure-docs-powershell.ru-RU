---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519809"
---
# <span data-ttu-id="30603-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="30603-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="30603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30603-102">SYNOPSIS</span></span>
<span data-ttu-id="30603-103">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="30603-103">Delete cluster</span></span>

## <span data-ttu-id="30603-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30603-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30603-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30603-105">DESCRIPTION</span></span>
<span data-ttu-id="30603-106">Кластер удаления применяется только к кластерам с состоянием подготовка "Успешно"</span><span class="sxs-lookup"><span data-stu-id="30603-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="30603-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30603-107">EXAMPLES</span></span>

### <span data-ttu-id="30603-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30603-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="30603-109">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="30603-109">Delete cluster</span></span>

## <span data-ttu-id="30603-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30603-110">PARAMETERS</span></span>

### <span data-ttu-id="30603-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30603-111">-AsJob</span></span>
<span data-ttu-id="30603-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="30603-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30603-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30603-113">-ClusterName</span></span>
<span data-ttu-id="30603-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="30603-114">The cluster name.</span></span>

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

### <span data-ttu-id="30603-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30603-115">-DefaultProfile</span></span>
<span data-ttu-id="30603-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30603-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30603-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30603-117">-ResourceGroupName</span></span>
<span data-ttu-id="30603-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30603-118">The resource group name.</span></span>

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

### <span data-ttu-id="30603-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30603-119">-Confirm</span></span>
<span data-ttu-id="30603-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30603-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30603-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30603-121">-WhatIf</span></span>
<span data-ttu-id="30603-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30603-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30603-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30603-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30603-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30603-124">CommonParameters</span></span>
<span data-ttu-id="30603-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30603-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30603-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30603-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30603-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30603-127">INPUTS</span></span>

### <span data-ttu-id="30603-128">System.String</span><span class="sxs-lookup"><span data-stu-id="30603-128">System.String</span></span>

## <span data-ttu-id="30603-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30603-129">OUTPUTS</span></span>

### <span data-ttu-id="30603-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30603-130">System.Boolean</span></span>

## <span data-ttu-id="30603-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30603-131">NOTES</span></span>

## <span data-ttu-id="30603-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30603-132">RELATED LINKS</span></span>
