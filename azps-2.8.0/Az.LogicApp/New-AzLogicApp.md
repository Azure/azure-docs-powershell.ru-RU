---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 7b76428452f8671e6f5112ec3ea429c6e3f5fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720510"
---
# <span data-ttu-id="e2091-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e2091-101">New-AzLogicApp</span></span>

## <span data-ttu-id="e2091-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2091-102">SYNOPSIS</span></span>
<span data-ttu-id="e2091-103">Создает логическое приложение в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2091-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="e2091-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2091-104">SYNTAX</span></span>

### <span data-ttu-id="e2091-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2091-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2091-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2091-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2091-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2091-107">DESCRIPTION</span></span>
<span data-ttu-id="e2091-108">Командлет **New-AzLogicApp** создает логическое приложение с помощью функции "приложения логики".</span><span class="sxs-lookup"><span data-stu-id="e2091-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="e2091-109">Логическое приложение — это коллекция действий или триггеров, определенных в определении логического приложения.</span><span class="sxs-lookup"><span data-stu-id="e2091-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="e2091-110">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="e2091-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="e2091-111">Вы можете создать логическое приложение, указав имя, расположение, определение приложения логики, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="e2091-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="e2091-112">Логическое определение и параметры приложения форматируются в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="e2091-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="e2091-113">Вы можете использовать логическое приложение в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="e2091-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="e2091-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e2091-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e2091-115">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="e2091-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e2091-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="e2091-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e2091-117">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="e2091-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e2091-118">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="e2091-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="e2091-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2091-119">EXAMPLES</span></span>

### <span data-ttu-id="e2091-120">Пример 1: создание логики приложения с помощью путей к файлам определения и параметров</span><span class="sxs-lookup"><span data-stu-id="e2091-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="e2091-121">Эта команда создает логическое приложение в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2091-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="e2091-122">Логическое приложение включает определение и параметры, указанные путями файлов.</span><span class="sxs-lookup"><span data-stu-id="e2091-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e2091-123">Пример 2: создание приложения логики с помощью объектов определения и параметров</span><span class="sxs-lookup"><span data-stu-id="e2091-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="e2091-124">Эта команда создает логическое приложение в указанной группе ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="e2091-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="e2091-125">Пример 3: создание логики приложения с помощью конвейера для указания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2091-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="e2091-126">Эта команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e2091-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e2091-127">Команда передает эту группу ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e2091-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e2091-128">Текущий командлет создает логическое приложение в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2091-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="e2091-129">Логическое приложение включает определение и параметры, указанные путями файлов.</span><span class="sxs-lookup"><span data-stu-id="e2091-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e2091-130">Пример 4: создание приложения логики на основе существующего приложения логики</span><span class="sxs-lookup"><span data-stu-id="e2091-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="e2091-131">Первая команда получает логическое приложение с именем LogicApp03 с помощью командлета Get-AzLogicApp.</span><span class="sxs-lookup"><span data-stu-id="e2091-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="e2091-132">Команда хранит логическое приложение в переменной $Workflow.</span><span class="sxs-lookup"><span data-stu-id="e2091-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="e2091-133">Вторая команда создает новое логическое приложение, которое использует определение и параметры приложения логики, которое хранится в $Workflow.</span><span class="sxs-lookup"><span data-stu-id="e2091-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="e2091-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2091-134">PARAMETERS</span></span>

### <span data-ttu-id="e2091-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2091-135">-DefaultProfile</span></span>
<span data-ttu-id="e2091-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2091-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-137">-Определение</span><span class="sxs-lookup"><span data-stu-id="e2091-137">-Definition</span></span>
<span data-ttu-id="e2091-138">Задает определение для приложения логики в виде объекта или строки в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="e2091-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="e2091-139">-DefinitionFilePath</span></span>
<span data-ttu-id="e2091-140">Указывает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e2091-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="e2091-141">-IntegrationAccountId</span></span>
<span data-ttu-id="e2091-142">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e2091-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="e2091-143">-Location</span><span class="sxs-lookup"><span data-stu-id="e2091-143">-Location</span></span>
<span data-ttu-id="e2091-144">Указывает расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e2091-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="e2091-145">Введите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="e2091-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="e2091-146">Вы можете поместить логику приложения в любое место.</span><span class="sxs-lookup"><span data-stu-id="e2091-146">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2091-147">-Name</span></span>
<span data-ttu-id="e2091-148">Задает имя для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e2091-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="e2091-149">-ParameterFilePath</span></span>
<span data-ttu-id="e2091-150">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="e2091-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="e2091-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e2091-151">-Parameters</span></span>
<span data-ttu-id="e2091-152">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e2091-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="e2091-153">Укажите хэш-таблицу, \< строку словаря \> или строку словаря \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="e2091-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2091-154">-ResourceGroupName</span></span>
<span data-ttu-id="e2091-155">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2091-155">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-156">-State</span><span class="sxs-lookup"><span data-stu-id="e2091-156">-State</span></span>
<span data-ttu-id="e2091-157">Указывает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="e2091-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="e2091-158">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="e2091-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2091-159">-Confirm</span></span>
<span data-ttu-id="e2091-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2091-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2091-161">-WhatIf</span></span>
<span data-ttu-id="e2091-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2091-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2091-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2091-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2091-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2091-164">CommonParameters</span></span>
<span data-ttu-id="e2091-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2091-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2091-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2091-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2091-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2091-167">INPUTS</span></span>

### <span data-ttu-id="e2091-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e2091-168">System.String</span></span>

## <span data-ttu-id="e2091-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2091-169">OUTPUTS</span></span>

### <span data-ttu-id="e2091-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2091-170">System.Object</span></span>

## <span data-ttu-id="e2091-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2091-171">NOTES</span></span>

## <span data-ttu-id="e2091-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2091-172">RELATED LINKS</span></span>

[<span data-ttu-id="e2091-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e2091-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="e2091-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e2091-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="e2091-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e2091-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="e2091-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e2091-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


