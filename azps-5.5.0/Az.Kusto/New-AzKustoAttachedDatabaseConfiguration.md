---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 09284a91c5ea2f7561a867250a92c4cd0d96e8e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243325"
---
# <span data-ttu-id="095dc-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="095dc-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="095dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="095dc-102">SYNOPSIS</span></span>
<span data-ttu-id="095dc-103">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="095dc-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="095dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="095dc-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="095dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="095dc-105">DESCRIPTION</span></span>
<span data-ttu-id="095dc-106">Создание или обновление конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="095dc-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="095dc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="095dc-107">EXAMPLES</span></span>

### <span data-ttu-id="095dc-108">Пример 1. Создание новой вложенной базы данныхConfiguration</span><span class="sxs-lookup"><span data-stu-id="095dc-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="095dc-109">С этой командой создается база данных ReadOnly "mykustodatabase" в кластере "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="095dc-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="095dc-110">Она следует за базой данных mykustodatabase из кластера "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="095dc-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="095dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="095dc-111">PARAMETERS</span></span>

### <span data-ttu-id="095dc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="095dc-112">-AsJob</span></span>
<span data-ttu-id="095dc-113">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="095dc-113">Run the command as a job</span></span>

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

### <span data-ttu-id="095dc-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="095dc-114">-ClusterName</span></span>
<span data-ttu-id="095dc-115">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="095dc-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="095dc-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="095dc-116">-ClusterResourceId</span></span>
<span data-ttu-id="095dc-117">ИД ресурса кластера, в котором находятся базы данных, которые вы хотите прикрепить.</span><span class="sxs-lookup"><span data-stu-id="095dc-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="095dc-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="095dc-118">-DatabaseName</span></span>
<span data-ttu-id="095dc-119">Имя базы данных, которую вы хотите встроить, используйте \*, если вы хотите следить за всеми текущими и будущими базами данных.</span><span class="sxs-lookup"><span data-stu-id="095dc-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="095dc-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="095dc-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="095dc-121">Тип изменения по умолчанию для основной суммы</span><span class="sxs-lookup"><span data-stu-id="095dc-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="095dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095dc-122">-DefaultProfile</span></span>
<span data-ttu-id="095dc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="095dc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095dc-124">-Location</span><span class="sxs-lookup"><span data-stu-id="095dc-124">-Location</span></span>
<span data-ttu-id="095dc-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="095dc-125">Resource location.</span></span>

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

### <span data-ttu-id="095dc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="095dc-126">-Name</span></span>
<span data-ttu-id="095dc-127">Имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="095dc-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="095dc-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="095dc-128">-NoWait</span></span>
<span data-ttu-id="095dc-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="095dc-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="095dc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095dc-130">-ResourceGroupName</span></span>
<span data-ttu-id="095dc-131">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="095dc-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="095dc-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="095dc-132">-SubscriptionId</span></span>
<span data-ttu-id="095dc-133">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="095dc-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="095dc-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="095dc-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="095dc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="095dc-135">-Confirm</span></span>
<span data-ttu-id="095dc-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="095dc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095dc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095dc-137">-WhatIf</span></span>
<span data-ttu-id="095dc-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095dc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095dc-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="095dc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095dc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095dc-140">CommonParameters</span></span>
<span data-ttu-id="095dc-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095dc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095dc-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="095dc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095dc-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="095dc-143">INPUTS</span></span>

## <span data-ttu-id="095dc-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="095dc-144">OUTPUTS</span></span>

### <span data-ttu-id="095dc-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="095dc-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="095dc-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="095dc-146">NOTES</span></span>

<span data-ttu-id="095dc-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="095dc-147">ALIASES</span></span>

## <span data-ttu-id="095dc-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="095dc-148">RELATED LINKS</span></span>

