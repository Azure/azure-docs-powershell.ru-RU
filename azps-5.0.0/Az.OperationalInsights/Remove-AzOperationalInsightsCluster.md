---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315797"
---
# <span data-ttu-id="6801e-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="6801e-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="6801e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6801e-102">SYNOPSIS</span></span>
<span data-ttu-id="6801e-103">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="6801e-103">Delete cluster</span></span>

## <span data-ttu-id="6801e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6801e-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6801e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6801e-105">DESCRIPTION</span></span>
<span data-ttu-id="6801e-106">Удаление кластера, применимо только к кластерам с состоянием подготовки "успешно завершено"</span><span class="sxs-lookup"><span data-stu-id="6801e-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="6801e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6801e-107">EXAMPLES</span></span>

### <span data-ttu-id="6801e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6801e-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="6801e-109">Удаление кластера</span><span class="sxs-lookup"><span data-stu-id="6801e-109">Delete cluster</span></span>

## <span data-ttu-id="6801e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6801e-110">PARAMETERS</span></span>

### <span data-ttu-id="6801e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6801e-111">-AsJob</span></span>
<span data-ttu-id="6801e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6801e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6801e-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="6801e-113">-ClusterName</span></span>
<span data-ttu-id="6801e-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6801e-114">The cluster name.</span></span>

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

### <span data-ttu-id="6801e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6801e-115">-DefaultProfile</span></span>
<span data-ttu-id="6801e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6801e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6801e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6801e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6801e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6801e-118">The resource group name.</span></span>

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

### <span data-ttu-id="6801e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6801e-119">-Confirm</span></span>
<span data-ttu-id="6801e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6801e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6801e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6801e-121">-WhatIf</span></span>
<span data-ttu-id="6801e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6801e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6801e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6801e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6801e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6801e-124">CommonParameters</span></span>
<span data-ttu-id="6801e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6801e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6801e-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6801e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6801e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6801e-127">INPUTS</span></span>

### <span data-ttu-id="6801e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6801e-128">System.String</span></span>

## <span data-ttu-id="6801e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6801e-129">OUTPUTS</span></span>

### <span data-ttu-id="6801e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6801e-130">System.Boolean</span></span>

## <span data-ttu-id="6801e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6801e-131">NOTES</span></span>

## <span data-ttu-id="6801e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6801e-132">RELATED LINKS</span></span>
