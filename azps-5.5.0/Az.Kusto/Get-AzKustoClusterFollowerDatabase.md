---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: ecc811e98545816e69f7baa6fc96ea92fbeb43d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219353"
---
# <span data-ttu-id="b7121-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="b7121-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="b7121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7121-102">SYNOPSIS</span></span>
<span data-ttu-id="b7121-103">Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.</span><span class="sxs-lookup"><span data-stu-id="b7121-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="b7121-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7121-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7121-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7121-105">DESCRIPTION</span></span>
<span data-ttu-id="b7121-106">Возвращает список баз данных, которые принадлежат этому кластеру и за которыми следует другой кластер.</span><span class="sxs-lookup"><span data-stu-id="b7121-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="b7121-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7121-107">EXAMPLES</span></span>

### <span data-ttu-id="b7121-108">Пример 1. Список всех баз данных, на которые вы на которые следуете</span><span class="sxs-lookup"><span data-stu-id="b7121-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="b7121-109">Указанная выше команда содержит список всех баз данных, которые принадлежат этому кластеру и за которыми следует еще один кластер.</span><span class="sxs-lookup"><span data-stu-id="b7121-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="b7121-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7121-110">PARAMETERS</span></span>

### <span data-ttu-id="b7121-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7121-111">-ClusterName</span></span>
<span data-ttu-id="b7121-112">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="b7121-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7121-113">-DefaultProfile</span></span>
<span data-ttu-id="b7121-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7121-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7121-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7121-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7121-116">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="b7121-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7121-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7121-117">-SubscriptionId</span></span>
<span data-ttu-id="b7121-118">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7121-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7121-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b7121-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7121-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7121-120">-Confirm</span></span>
<span data-ttu-id="b7121-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7121-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7121-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7121-122">-WhatIf</span></span>
<span data-ttu-id="b7121-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7121-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7121-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7121-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7121-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7121-125">CommonParameters</span></span>
<span data-ttu-id="b7121-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7121-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7121-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7121-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7121-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7121-128">INPUTS</span></span>

## <span data-ttu-id="b7121-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7121-129">OUTPUTS</span></span>

### <span data-ttu-id="b7121-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="b7121-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="b7121-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7121-131">NOTES</span></span>

<span data-ttu-id="b7121-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b7121-132">ALIASES</span></span>

## <span data-ttu-id="b7121-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7121-133">RELATED LINKS</span></span>

