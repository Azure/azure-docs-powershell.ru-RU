---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249033"
---
# <span data-ttu-id="b9228-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="b9228-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="b9228-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9228-102">SYNOPSIS</span></span>
<span data-ttu-id="b9228-103">Добавьте список расширений языка, которые могут выполняться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="b9228-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b9228-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9228-104">SYNTAX</span></span>

### <span data-ttu-id="b9228-105">AddExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9228-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9228-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b9228-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9228-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9228-107">DESCRIPTION</span></span>
<span data-ttu-id="b9228-108">Добавьте список расширений языка, которые могут выполняться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="b9228-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b9228-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9228-109">EXAMPLES</span></span>

### <span data-ttu-id="b9228-110">Пример 1: Добавление списка расширений языка</span><span class="sxs-lookup"><span data-stu-id="b9228-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="b9228-111">Приведенная выше команда добавляет список расширений языка, которые могут выполняться в запросах KQL</span><span class="sxs-lookup"><span data-stu-id="b9228-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="b9228-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9228-112">PARAMETERS</span></span>

### <span data-ttu-id="b9228-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9228-113">-AsJob</span></span>
<span data-ttu-id="b9228-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b9228-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b9228-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b9228-115">-ClusterName</span></span>
<span data-ttu-id="b9228-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="b9228-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b9228-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9228-117">-DefaultProfile</span></span>
<span data-ttu-id="b9228-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9228-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9228-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9228-119">-InputObject</span></span>
<span data-ttu-id="b9228-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b9228-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9228-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="b9228-121">-NoWait</span></span>
<span data-ttu-id="b9228-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="b9228-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9228-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9228-123">-PassThru</span></span>
<span data-ttu-id="b9228-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b9228-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9228-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9228-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9228-126">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="b9228-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b9228-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9228-127">-SubscriptionId</span></span>
<span data-ttu-id="b9228-128">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9228-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9228-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b9228-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9228-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b9228-130">-Value</span></span>
<span data-ttu-id="b9228-131">Список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="b9228-131">The list of language extensions.</span></span>
<span data-ttu-id="b9228-132">Для конструирования ознакомьтесь с разделом "Заметки" для свойств значения и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b9228-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9228-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9228-133">-Confirm</span></span>
<span data-ttu-id="b9228-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9228-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9228-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9228-135">-WhatIf</span></span>
<span data-ttu-id="b9228-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9228-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9228-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9228-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9228-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9228-138">CommonParameters</span></span>
<span data-ttu-id="b9228-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9228-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9228-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9228-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9228-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9228-141">INPUTS</span></span>

### <span data-ttu-id="b9228-142">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b9228-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b9228-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9228-143">OUTPUTS</span></span>

### <span data-ttu-id="b9228-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9228-144">System.Boolean</span></span>

## <span data-ttu-id="b9228-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9228-145">NOTES</span></span>

<span data-ttu-id="b9228-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b9228-146">ALIASES</span></span>

<span data-ttu-id="b9228-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b9228-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9228-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b9228-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9228-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9228-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9228-150">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="b9228-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9228-151">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b9228-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b9228-152">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="b9228-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b9228-153">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="b9228-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b9228-154">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="b9228-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b9228-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="b9228-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9228-156">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="b9228-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b9228-157">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b9228-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b9228-158">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="b9228-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b9228-159">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9228-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b9228-160">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b9228-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b9228-161">VALUE (значение) <ILanguageExtension [] >: список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="b9228-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="b9228-162">`[Name <LanguageExtensionName?>]`: Имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="b9228-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="b9228-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9228-163">RELATED LINKS</span></span>

