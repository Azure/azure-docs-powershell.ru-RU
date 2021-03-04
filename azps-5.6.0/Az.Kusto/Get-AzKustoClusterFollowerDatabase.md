---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: 5b53c9806fa541c28b7f318f464a26e9a88104e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964515"
---
# <span data-ttu-id="898db-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="898db-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="898db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="898db-102">SYNOPSIS</span></span>
<span data-ttu-id="898db-103">Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.</span><span class="sxs-lookup"><span data-stu-id="898db-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="898db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="898db-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="898db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="898db-105">DESCRIPTION</span></span>
<span data-ttu-id="898db-106">Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.</span><span class="sxs-lookup"><span data-stu-id="898db-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="898db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="898db-107">EXAMPLES</span></span>

### <span data-ttu-id="898db-108">Пример 1. Список всех баз данных, на которые вы на которые следуете</span><span class="sxs-lookup"><span data-stu-id="898db-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="898db-109">Указанная выше команда содержит список всех баз данных, которые принадлежат этому кластеру и за которыми следует еще один кластер.</span><span class="sxs-lookup"><span data-stu-id="898db-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="898db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="898db-110">PARAMETERS</span></span>

### <span data-ttu-id="898db-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="898db-111">-ClusterName</span></span>
<span data-ttu-id="898db-112">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="898db-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898db-113">-DefaultProfile</span></span>
<span data-ttu-id="898db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="898db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898db-115">-ResourceGroupName</span></span>
<span data-ttu-id="898db-116">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="898db-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="898db-117">-SubscriptionId</span></span>
<span data-ttu-id="898db-118">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="898db-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="898db-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="898db-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="898db-120">-Confirm</span></span>
<span data-ttu-id="898db-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898db-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="898db-122">-WhatIf</span></span>
<span data-ttu-id="898db-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898db-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="898db-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="898db-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898db-125">CommonParameters</span></span>
<span data-ttu-id="898db-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898db-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="898db-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898db-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="898db-128">INPUTS</span></span>

## <span data-ttu-id="898db-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="898db-129">OUTPUTS</span></span>

### <span data-ttu-id="898db-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="898db-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="898db-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="898db-131">NOTES</span></span>

<span data-ttu-id="898db-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="898db-132">ALIASES</span></span>

## <span data-ttu-id="898db-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="898db-133">RELATED LINKS</span></span>

