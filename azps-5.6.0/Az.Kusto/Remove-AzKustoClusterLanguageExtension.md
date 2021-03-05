---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 6a687139f7dec156e539c09b864a88c4e8876fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972824"
---
# <span data-ttu-id="2be8c-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="2be8c-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="2be8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2be8c-103">Удалите список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="2be8c-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="2be8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2be8c-104">SYNTAX</span></span>

### <span data-ttu-id="2be8c-105">RemoveExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2be8c-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2be8c-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2be8c-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2be8c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2be8c-107">DESCRIPTION</span></span>
<span data-ttu-id="2be8c-108">Удалите список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="2be8c-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="2be8c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2be8c-109">EXAMPLES</span></span>

### <span data-ttu-id="2be8c-110">Пример 1. Удаление списка языковых расширений из кластера</span><span class="sxs-lookup"><span data-stu-id="2be8c-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="2be8c-111">Эта команда удаляет список языковых расширений, которые могут запускаться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="2be8c-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="2be8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2be8c-112">PARAMETERS</span></span>

### <span data-ttu-id="2be8c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2be8c-113">-AsJob</span></span>
<span data-ttu-id="2be8c-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="2be8c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2be8c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2be8c-115">-ClusterName</span></span>
<span data-ttu-id="2be8c-116">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="2be8c-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be8c-117">-DefaultProfile</span></span>
<span data-ttu-id="2be8c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2be8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2be8c-119">-InputObject</span></span>
<span data-ttu-id="2be8c-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2be8c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2be8c-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2be8c-121">-NoWait</span></span>
<span data-ttu-id="2be8c-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="2be8c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2be8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2be8c-123">-PassThru</span></span>
<span data-ttu-id="2be8c-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="2be8c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2be8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="2be8c-126">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="2be8c-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2be8c-127">-SubscriptionId</span></span>
<span data-ttu-id="2be8c-128">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2be8c-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2be8c-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2be8c-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8c-130">-Значение</span><span class="sxs-lookup"><span data-stu-id="2be8c-130">-Value</span></span>
<span data-ttu-id="2be8c-131">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="2be8c-131">The list of language extensions.</span></span>
<span data-ttu-id="2be8c-132">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств VALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2be8c-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2be8c-133">-Confirm</span></span>
<span data-ttu-id="2be8c-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be8c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be8c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be8c-135">-WhatIf</span></span>
<span data-ttu-id="2be8c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be8c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be8c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2be8c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be8c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be8c-138">CommonParameters</span></span>
<span data-ttu-id="2be8c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be8c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be8c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2be8c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be8c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2be8c-141">INPUTS</span></span>

### <span data-ttu-id="2be8c-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2be8c-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2be8c-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2be8c-143">OUTPUTS</span></span>

### <span data-ttu-id="2be8c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2be8c-144">System.Boolean</span></span>

## <span data-ttu-id="2be8c-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2be8c-145">NOTES</span></span>

<span data-ttu-id="2be8c-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2be8c-146">ALIASES</span></span>

<span data-ttu-id="2be8c-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2be8c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2be8c-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2be8c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2be8c-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2be8c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2be8c-150">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2be8c-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2be8c-151">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="2be8c-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2be8c-152">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="2be8c-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2be8c-153">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="2be8c-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2be8c-154">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="2be8c-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2be8c-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2be8c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2be8c-156">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="2be8c-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2be8c-157">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="2be8c-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2be8c-158">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="2be8c-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2be8c-159">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2be8c-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2be8c-160">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2be8c-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="2be8c-161">VALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="2be8c-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="2be8c-162">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="2be8c-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="2be8c-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2be8c-163">RELATED LINKS</span></span>

