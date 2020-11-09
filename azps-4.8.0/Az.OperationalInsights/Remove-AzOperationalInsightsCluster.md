---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244029"
---
# <span data-ttu-id="23fd4-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="23fd4-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="23fd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="23fd4-103">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="23fd4-103">Delete cluster</span></span>

## <span data-ttu-id="23fd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23fd4-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23fd4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="23fd4-106">Удаление кластера, применимо только к кластерам с состоянием подготовки "успешно завершено"</span><span class="sxs-lookup"><span data-stu-id="23fd4-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="23fd4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="23fd4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23fd4-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="23fd4-109">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="23fd4-109">Delete cluster</span></span>

## <span data-ttu-id="23fd4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23fd4-110">PARAMETERS</span></span>

### <span data-ttu-id="23fd4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23fd4-111">-AsJob</span></span>
<span data-ttu-id="23fd4-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="23fd4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23fd4-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="23fd4-113">-ClusterName</span></span>
<span data-ttu-id="23fd4-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="23fd4-114">The cluster name.</span></span>

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

### <span data-ttu-id="23fd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fd4-115">-DefaultProfile</span></span>
<span data-ttu-id="23fd4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23fd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23fd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="23fd4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23fd4-118">The resource group name.</span></span>

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

### <span data-ttu-id="23fd4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23fd4-119">-Confirm</span></span>
<span data-ttu-id="23fd4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23fd4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fd4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fd4-121">-WhatIf</span></span>
<span data-ttu-id="23fd4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23fd4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23fd4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23fd4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23fd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fd4-124">CommonParameters</span></span>
<span data-ttu-id="23fd4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23fd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fd4-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23fd4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fd4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23fd4-127">INPUTS</span></span>

### <span data-ttu-id="23fd4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23fd4-128">System.String</span></span>

## <span data-ttu-id="23fd4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23fd4-129">OUTPUTS</span></span>

### <span data-ttu-id="23fd4-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23fd4-130">System.Boolean</span></span>

## <span data-ttu-id="23fd4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="23fd4-131">NOTES</span></span>

## <span data-ttu-id="23fd4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23fd4-132">RELATED LINKS</span></span>