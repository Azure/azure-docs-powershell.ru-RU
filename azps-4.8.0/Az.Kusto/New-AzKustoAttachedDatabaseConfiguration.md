---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243550"
---
# <span data-ttu-id="5aa49-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aa49-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="5aa49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5aa49-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa49-103">Создание или обновление конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5aa49-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="5aa49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5aa49-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5aa49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa49-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa49-106">Создание или обновление конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5aa49-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="5aa49-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5aa49-107">EXAMPLES</span></span>

### <span data-ttu-id="5aa49-108">Пример 1: создание нового AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aa49-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="5aa49-109">Вышеприведенная команда создает базу данных ReadOnly "mykustodatabase" в Cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="5aa49-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="5aa49-110">Оно следует за базой данных "mykustodatabase" из кластера "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="5aa49-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="5aa49-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5aa49-111">PARAMETERS</span></span>

### <span data-ttu-id="5aa49-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aa49-112">-AsJob</span></span>
<span data-ttu-id="5aa49-113">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5aa49-113">Run the command as a job</span></span>

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

### <span data-ttu-id="5aa49-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="5aa49-114">-ClusterName</span></span>
<span data-ttu-id="5aa49-115">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="5aa49-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5aa49-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="5aa49-116">-ClusterResourceId</span></span>
<span data-ttu-id="5aa49-117">Идентификатор ресурса кластера, на котором находятся базы данных, которые вы хотите прикрепить.</span><span class="sxs-lookup"><span data-stu-id="5aa49-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="5aa49-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5aa49-118">-DatabaseName</span></span>
<span data-ttu-id="5aa49-119">Имя базы данных, которую вы хотите прикрепить, используйте \*, если вы хотите подписаться на все текущие и будущие базы данных.</span><span class="sxs-lookup"><span data-stu-id="5aa49-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="5aa49-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="5aa49-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="5aa49-121">Изменение типов участников по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aa49-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="5aa49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa49-122">-DefaultProfile</span></span>
<span data-ttu-id="5aa49-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa49-124">-Location</span><span class="sxs-lookup"><span data-stu-id="5aa49-124">-Location</span></span>
<span data-ttu-id="5aa49-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5aa49-125">Resource location.</span></span>

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

### <span data-ttu-id="5aa49-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5aa49-126">-Name</span></span>
<span data-ttu-id="5aa49-127">Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5aa49-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="5aa49-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="5aa49-128">-NoWait</span></span>
<span data-ttu-id="5aa49-129">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="5aa49-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5aa49-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa49-130">-ResourceGroupName</span></span>
<span data-ttu-id="5aa49-131">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="5aa49-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5aa49-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5aa49-132">-SubscriptionId</span></span>
<span data-ttu-id="5aa49-133">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa49-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5aa49-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="5aa49-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5aa49-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aa49-135">-Confirm</span></span>
<span data-ttu-id="5aa49-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5aa49-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa49-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa49-137">-WhatIf</span></span>
<span data-ttu-id="5aa49-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5aa49-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa49-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5aa49-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa49-140">CommonParameters</span></span>
<span data-ttu-id="5aa49-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5aa49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa49-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aa49-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa49-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5aa49-143">INPUTS</span></span>

## <span data-ttu-id="5aa49-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa49-144">OUTPUTS</span></span>

### <span data-ttu-id="5aa49-145">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aa49-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="5aa49-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="5aa49-146">NOTES</span></span>

<span data-ttu-id="5aa49-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5aa49-147">ALIASES</span></span>

## <span data-ttu-id="5aa49-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5aa49-148">RELATED LINKS</span></span>

