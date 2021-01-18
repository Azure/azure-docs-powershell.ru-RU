---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505113"
---
# <span data-ttu-id="415f8-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="415f8-101">New-AzLogicApp</span></span>

## <span data-ttu-id="415f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="415f8-102">SYNOPSIS</span></span>
<span data-ttu-id="415f8-103">Создает приложение логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415f8-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="415f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="415f8-104">SYNTAX</span></span>

### <span data-ttu-id="415f8-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="415f8-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="415f8-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="415f8-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="415f8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="415f8-107">DESCRIPTION</span></span>
<span data-ttu-id="415f8-108">С **помощью cmdlet New-AzLogicApp** создается приложение логики с помощью функции "Приложения логики".</span><span class="sxs-lookup"><span data-stu-id="415f8-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="415f8-109">Приложение логики — это набор действий или триггеров, определенных в определении приложения Logic.</span><span class="sxs-lookup"><span data-stu-id="415f8-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="415f8-110">Этот cmdlet возвращает объект **рабочего** процесса.</span><span class="sxs-lookup"><span data-stu-id="415f8-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="415f8-111">Вы можете создать приложение логики, указав имя, расположение, определение приложения Logic, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="415f8-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="415f8-112">Определение и параметры приложения Logic форматированы в нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="415f8-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="415f8-113">Приложение логики можно использовать в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="415f8-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="415f8-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="415f8-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="415f8-115">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="415f8-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="415f8-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="415f8-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="415f8-117">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="415f8-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="415f8-118">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="415f8-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="415f8-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="415f8-119">EXAMPLES</span></span>

### <span data-ttu-id="415f8-120">Пример 1. Создание приложения логики с помощью путей определения и файла параметров</span><span class="sxs-lookup"><span data-stu-id="415f8-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
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

<span data-ttu-id="415f8-121">Эта команда создает приложение логики в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415f8-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="415f8-122">Приложение логики содержит определение и параметры, задав пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="415f8-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="415f8-123">Пример 2. Создание приложения логики с использованием объектов определения и параметров</span><span class="sxs-lookup"><span data-stu-id="415f8-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
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

<span data-ttu-id="415f8-124">Эта команда создает приложение логики в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415f8-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="415f8-125">Пример 3. Создание приложения логики с помощью конвейера для указания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="415f8-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
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

<span data-ttu-id="415f8-126">Эта команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="415f8-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="415f8-127">Эта команда передает группу ресурсов текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="415f8-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="415f8-128">Текущий cmdlet создает приложение логики в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415f8-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="415f8-129">Приложение логики содержит определение и параметры, задав пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="415f8-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="415f8-130">Пример 4. Создание приложения логики на основе существующего приложения логики</span><span class="sxs-lookup"><span data-stu-id="415f8-130">Example 4: Create a logic app based on an existing logic app</span></span>
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

<span data-ttu-id="415f8-131">Первая команда получает приложение логики LogicApp03 с помощью Get-AzLogicApp командлета.</span><span class="sxs-lookup"><span data-stu-id="415f8-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="415f8-132">Команда хранит приложение логики в переменной $Workflow.</span><span class="sxs-lookup"><span data-stu-id="415f8-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="415f8-133">Вторая команда создает приложение логики, использующее определение и параметры приложения логики, храняого в $Workflow.</span><span class="sxs-lookup"><span data-stu-id="415f8-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="415f8-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="415f8-134">PARAMETERS</span></span>

### <span data-ttu-id="415f8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415f8-135">-DefaultProfile</span></span>
<span data-ttu-id="415f8-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="415f8-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="415f8-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="415f8-137">-Definition</span></span>
<span data-ttu-id="415f8-138">Определение для приложения логики в качестве объекта или строки в формате нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="415f8-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="415f8-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="415f8-139">-DefinitionFilePath</span></span>
<span data-ttu-id="415f8-140">Определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="415f8-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="415f8-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="415f8-141">-IntegrationAccountId</span></span>
<span data-ttu-id="415f8-142">Определяет ИД учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="415f8-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="415f8-143">-Location</span><span class="sxs-lookup"><span data-stu-id="415f8-143">-Location</span></span>
<span data-ttu-id="415f8-144">Определяет расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="415f8-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="415f8-145">Введите расположение центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="415f8-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="415f8-146">Приложение логики можно разместить в любом месте.</span><span class="sxs-lookup"><span data-stu-id="415f8-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="415f8-147">-Name</span><span class="sxs-lookup"><span data-stu-id="415f8-147">-Name</span></span>
<span data-ttu-id="415f8-148">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="415f8-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="415f8-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="415f8-149">-ParameterFilePath</span></span>
<span data-ttu-id="415f8-150">Путь к файлу параметров в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="415f8-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="415f8-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="415f8-151">-Parameters</span></span>
<span data-ttu-id="415f8-152">Указывает объект коллекции параметров для приложения Logic.</span><span class="sxs-lookup"><span data-stu-id="415f8-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="415f8-153">Укажите hash table, Dictionary \<string\> или Dictionary \<string, WorkflowParameter\> (Словарь).</span><span class="sxs-lookup"><span data-stu-id="415f8-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="415f8-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415f8-154">-ResourceGroupName</span></span>
<span data-ttu-id="415f8-155">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415f8-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="415f8-156">-State</span><span class="sxs-lookup"><span data-stu-id="415f8-156">-State</span></span>
<span data-ttu-id="415f8-157">Определяет состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="415f8-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="415f8-158">Допустимые значения этого параметра: Enabled (Включено) и Disabled (Отключено).</span><span class="sxs-lookup"><span data-stu-id="415f8-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="415f8-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="415f8-159">-Confirm</span></span>
<span data-ttu-id="415f8-160">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="415f8-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415f8-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415f8-161">-WhatIf</span></span>
<span data-ttu-id="415f8-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="415f8-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415f8-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="415f8-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415f8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415f8-164">CommonParameters</span></span>
<span data-ttu-id="415f8-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415f8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415f8-166">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415f8-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415f8-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="415f8-167">INPUTS</span></span>

### <span data-ttu-id="415f8-168">System.String</span><span class="sxs-lookup"><span data-stu-id="415f8-168">System.String</span></span>

## <span data-ttu-id="415f8-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="415f8-169">OUTPUTS</span></span>

### <span data-ttu-id="415f8-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="415f8-170">System.Object</span></span>

## <span data-ttu-id="415f8-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="415f8-171">NOTES</span></span>

## <span data-ttu-id="415f8-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="415f8-172">RELATED LINKS</span></span>

[<span data-ttu-id="415f8-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="415f8-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="415f8-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="415f8-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="415f8-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="415f8-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="415f8-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="415f8-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


