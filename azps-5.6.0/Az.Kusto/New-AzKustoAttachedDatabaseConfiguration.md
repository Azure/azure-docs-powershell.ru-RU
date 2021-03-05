---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983480"
---
# <span data-ttu-id="c6341-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6341-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="c6341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6341-102">SYNOPSIS</span></span>
<span data-ttu-id="c6341-103">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c6341-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="c6341-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6341-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6341-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6341-105">DESCRIPTION</span></span>
<span data-ttu-id="c6341-106">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c6341-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="c6341-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6341-107">EXAMPLES</span></span>

### <span data-ttu-id="c6341-108">Пример 1. Создание новой вложенной базы данныхConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6341-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="c6341-109">С этой командой создается база данных ReadOnly "mykustodatabase" в кластере "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="c6341-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="c6341-110">Он следует за базой данных mykustodatabase из кластера "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="c6341-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="c6341-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6341-111">PARAMETERS</span></span>

### <span data-ttu-id="c6341-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6341-112">-AsJob</span></span>
<span data-ttu-id="c6341-113">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c6341-113">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c6341-114">-ClusterName</span></span>
<span data-ttu-id="c6341-115">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="c6341-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6341-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="c6341-116">-ClusterResourceId</span></span>
<span data-ttu-id="c6341-117">ИД ресурса кластера, в котором находятся базы данных, которые вы хотите прикрепить.</span><span class="sxs-lookup"><span data-stu-id="c6341-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6341-118">-DatabaseName</span></span>
<span data-ttu-id="c6341-119">Имя базы данных, которую вы хотите встроить, используйте \*, если вы хотите следить за всеми текущими и будущими базами данных.</span><span class="sxs-lookup"><span data-stu-id="c6341-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="c6341-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="c6341-121">Тип изменения по умолчанию для основной суммы</span><span class="sxs-lookup"><span data-stu-id="c6341-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6341-122">-DefaultProfile</span></span>
<span data-ttu-id="c6341-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6341-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6341-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c6341-124">-Location</span></span>
<span data-ttu-id="c6341-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6341-125">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c6341-126">-Name</span></span>
<span data-ttu-id="c6341-127">Имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c6341-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6341-128">-NoWait</span></span>
<span data-ttu-id="c6341-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c6341-129">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6341-130">-ResourceGroupName</span></span>
<span data-ttu-id="c6341-131">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="c6341-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c6341-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6341-132">-SubscriptionId</span></span>
<span data-ttu-id="c6341-133">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6341-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6341-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c6341-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6341-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6341-135">-Confirm</span></span>
<span data-ttu-id="c6341-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c6341-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6341-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6341-137">-WhatIf</span></span>
<span data-ttu-id="c6341-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6341-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6341-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6341-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6341-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6341-140">CommonParameters</span></span>
<span data-ttu-id="c6341-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6341-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6341-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6341-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6341-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6341-143">INPUTS</span></span>

## <span data-ttu-id="c6341-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6341-144">OUTPUTS</span></span>

### <span data-ttu-id="c6341-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6341-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="c6341-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6341-146">NOTES</span></span>

<span data-ttu-id="c6341-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c6341-147">ALIASES</span></span>

## <span data-ttu-id="c6341-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6341-148">RELATED LINKS</span></span>

