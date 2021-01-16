---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409012"
---
# <span data-ttu-id="299e9-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="299e9-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="299e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299e9-102">SYNOPSIS</span></span>
<span data-ttu-id="299e9-103">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="299e9-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="299e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="299e9-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="299e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="299e9-105">DESCRIPTION</span></span>
<span data-ttu-id="299e9-106">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="299e9-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="299e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="299e9-107">EXAMPLES</span></span>

### <span data-ttu-id="299e9-108">Пример 1. Создание новой вложенной базы данныхConfiguration</span><span class="sxs-lookup"><span data-stu-id="299e9-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="299e9-109">С этой командой создается база данных ReadOnly "mykustodatabase" в кластере testnewkustoclusterf.</span><span class="sxs-lookup"><span data-stu-id="299e9-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="299e9-110">Она следует за базой данных mykustodatabase из кластера "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="299e9-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="299e9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="299e9-111">PARAMETERS</span></span>

### <span data-ttu-id="299e9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="299e9-112">-AsJob</span></span>
<span data-ttu-id="299e9-113">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="299e9-113">Run the command as a job</span></span>

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

### <span data-ttu-id="299e9-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="299e9-114">-ClusterName</span></span>
<span data-ttu-id="299e9-115">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="299e9-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="299e9-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="299e9-116">-ClusterResourceId</span></span>
<span data-ttu-id="299e9-117">ИД ресурса кластера, в котором находятся базы данных, которые вы хотите прикрепить.</span><span class="sxs-lookup"><span data-stu-id="299e9-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="299e9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="299e9-118">-DatabaseName</span></span>
<span data-ttu-id="299e9-119">Имя базы данных, которую вы хотите встроить, используйте \*, если вы хотите следить за всеми текущими и будущими базами данных.</span><span class="sxs-lookup"><span data-stu-id="299e9-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="299e9-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="299e9-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="299e9-121">Тип изменения по умолчанию для основной суммы</span><span class="sxs-lookup"><span data-stu-id="299e9-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="299e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299e9-122">-DefaultProfile</span></span>
<span data-ttu-id="299e9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="299e9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299e9-124">-Location</span><span class="sxs-lookup"><span data-stu-id="299e9-124">-Location</span></span>
<span data-ttu-id="299e9-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="299e9-125">Resource location.</span></span>

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

### <span data-ttu-id="299e9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="299e9-126">-Name</span></span>
<span data-ttu-id="299e9-127">Имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="299e9-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="299e9-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="299e9-128">-NoWait</span></span>
<span data-ttu-id="299e9-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="299e9-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="299e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="299e9-131">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="299e9-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="299e9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="299e9-132">-SubscriptionId</span></span>
<span data-ttu-id="299e9-133">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="299e9-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="299e9-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="299e9-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="299e9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="299e9-135">-Confirm</span></span>
<span data-ttu-id="299e9-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="299e9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299e9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299e9-137">-WhatIf</span></span>
<span data-ttu-id="299e9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="299e9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="299e9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="299e9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299e9-140">CommonParameters</span></span>
<span data-ttu-id="299e9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299e9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="299e9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299e9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="299e9-143">INPUTS</span></span>

## <span data-ttu-id="299e9-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="299e9-144">OUTPUTS</span></span>

### <span data-ttu-id="299e9-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="299e9-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="299e9-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="299e9-146">NOTES</span></span>

<span data-ttu-id="299e9-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="299e9-147">ALIASES</span></span>

## <span data-ttu-id="299e9-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="299e9-148">RELATED LINKS</span></span>
