---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411711"
---
# <span data-ttu-id="63f3d-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="63f3d-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="63f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="63f3d-103">Добавьте список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="63f3d-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="63f3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63f3d-104">SYNTAX</span></span>

### <span data-ttu-id="63f3d-105">AddExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63f3d-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="63f3d-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="63f3d-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63f3d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63f3d-107">DESCRIPTION</span></span>
<span data-ttu-id="63f3d-108">Добавьте список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="63f3d-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="63f3d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63f3d-109">EXAMPLES</span></span>

### <span data-ttu-id="63f3d-110">Пример 1. Добавление списка языковых расширений</span><span class="sxs-lookup"><span data-stu-id="63f3d-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="63f3d-111">Вышеуказанная команда добавляет список языковых расширений, которые могут запускаться в запросах KQL</span><span class="sxs-lookup"><span data-stu-id="63f3d-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="63f3d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63f3d-112">PARAMETERS</span></span>

### <span data-ttu-id="63f3d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63f3d-113">-AsJob</span></span>
<span data-ttu-id="63f3d-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="63f3d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="63f3d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63f3d-115">-ClusterName</span></span>
<span data-ttu-id="63f3d-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="63f3d-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f3d-117">-DefaultProfile</span></span>
<span data-ttu-id="63f3d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63f3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f3d-119">-InputObject</span></span>
<span data-ttu-id="63f3d-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="63f3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f3d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="63f3d-121">-NoWait</span></span>
<span data-ttu-id="63f3d-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="63f3d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="63f3d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63f3d-123">-PassThru</span></span>
<span data-ttu-id="63f3d-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="63f3d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="63f3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="63f3d-126">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="63f3d-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f3d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63f3d-127">-SubscriptionId</span></span>
<span data-ttu-id="63f3d-128">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="63f3d-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="63f3d-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="63f3d-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f3d-130">-Value</span><span class="sxs-lookup"><span data-stu-id="63f3d-130">-Value</span></span>
<span data-ttu-id="63f3d-131">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="63f3d-131">The list of language extensions.</span></span>
<span data-ttu-id="63f3d-132">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств VALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="63f3d-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f3d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63f3d-133">-Confirm</span></span>
<span data-ttu-id="63f3d-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="63f3d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f3d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f3d-135">-WhatIf</span></span>
<span data-ttu-id="63f3d-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f3d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f3d-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="63f3d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f3d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f3d-138">CommonParameters</span></span>
<span data-ttu-id="63f3d-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f3d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f3d-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63f3d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f3d-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63f3d-141">INPUTS</span></span>

### <span data-ttu-id="63f3d-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="63f3d-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="63f3d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63f3d-143">OUTPUTS</span></span>

### <span data-ttu-id="63f3d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63f3d-144">System.Boolean</span></span>

## <span data-ttu-id="63f3d-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63f3d-145">NOTES</span></span>

<span data-ttu-id="63f3d-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="63f3d-146">ALIASES</span></span>

<span data-ttu-id="63f3d-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="63f3d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63f3d-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="63f3d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63f3d-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63f3d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63f3d-150">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="63f3d-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63f3d-151">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="63f3d-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="63f3d-152">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="63f3d-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="63f3d-153">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="63f3d-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="63f3d-154">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="63f3d-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="63f3d-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="63f3d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63f3d-156">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="63f3d-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="63f3d-157">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="63f3d-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="63f3d-158">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="63f3d-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="63f3d-159">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="63f3d-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="63f3d-160">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="63f3d-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="63f3d-161">VALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="63f3d-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="63f3d-162">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="63f3d-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="63f3d-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63f3d-163">RELATED LINKS</span></span>

