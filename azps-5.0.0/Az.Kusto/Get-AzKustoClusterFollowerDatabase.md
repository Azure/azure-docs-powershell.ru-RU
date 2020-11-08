---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249023"
---
# <span data-ttu-id="a075d-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="a075d-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="a075d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a075d-102">SYNOPSIS</span></span>
<span data-ttu-id="a075d-103">Возвращает список баз данных, владельцем которых является этот кластер, и за ними следуют другие кластеры.</span><span class="sxs-lookup"><span data-stu-id="a075d-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="a075d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a075d-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a075d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a075d-105">DESCRIPTION</span></span>
<span data-ttu-id="a075d-106">Возвращает список баз данных, владельцем которых является этот кластер, и за ними следуют другие кластеры.</span><span class="sxs-lookup"><span data-stu-id="a075d-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="a075d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a075d-107">EXAMPLES</span></span>

### <span data-ttu-id="a075d-108">Пример 1: список всех отслеживаемых баз данных</span><span class="sxs-lookup"><span data-stu-id="a075d-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="a075d-109">В приведенной выше команде перечислены все базы данных, которыми владеет этот кластер, и они следуют другим кластером.</span><span class="sxs-lookup"><span data-stu-id="a075d-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="a075d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a075d-110">PARAMETERS</span></span>

### <span data-ttu-id="a075d-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="a075d-111">-ClusterName</span></span>
<span data-ttu-id="a075d-112">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="a075d-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a075d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a075d-113">-DefaultProfile</span></span>
<span data-ttu-id="a075d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a075d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a075d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a075d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a075d-116">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="a075d-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a075d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a075d-117">-SubscriptionId</span></span>
<span data-ttu-id="a075d-118">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a075d-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a075d-119">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a075d-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a075d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a075d-120">-Confirm</span></span>
<span data-ttu-id="a075d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a075d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a075d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a075d-122">-WhatIf</span></span>
<span data-ttu-id="a075d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a075d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a075d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a075d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a075d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a075d-125">CommonParameters</span></span>
<span data-ttu-id="a075d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a075d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a075d-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a075d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a075d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a075d-128">INPUTS</span></span>

## <span data-ttu-id="a075d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a075d-129">OUTPUTS</span></span>

### <span data-ttu-id="a075d-130">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="a075d-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="a075d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a075d-131">NOTES</span></span>

<span data-ttu-id="a075d-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a075d-132">ALIASES</span></span>

## <span data-ttu-id="a075d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a075d-133">RELATED LINKS</span></span>

