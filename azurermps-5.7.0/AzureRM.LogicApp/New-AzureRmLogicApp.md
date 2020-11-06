---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 1d2c39fcb22dfcf554487318a3a8f0a0b114fe11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566168"
---
# <span data-ttu-id="8c69e-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c69e-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="8c69e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c69e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c69e-103">Создает логическое приложение в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c69e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c69e-104">SYNTAX</span></span>

### <span data-ttu-id="8c69e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c69e-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c69e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c69e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c69e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c69e-107">DESCRIPTION</span></span>
<span data-ttu-id="8c69e-108">Командлет **New-AzureRmLogicApp** создает логическое приложение с помощью функции "приложения логики".</span><span class="sxs-lookup"><span data-stu-id="8c69e-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8c69e-109">Логическое приложение — это коллекция действий или триггеров, определенных в определении логического приложения.</span><span class="sxs-lookup"><span data-stu-id="8c69e-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="8c69e-110">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="8c69e-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="8c69e-111">Вы можете создать логическое приложение, указав имя, расположение, определение приложения логики, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="8c69e-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="8c69e-112">Логическое определение и параметры приложения форматируются в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="8c69e-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="8c69e-113">Вы можете использовать логическое приложение в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="8c69e-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="8c69e-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="8c69e-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8c69e-115">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="8c69e-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8c69e-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="8c69e-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8c69e-117">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="8c69e-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="8c69e-118">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="8c69e-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="8c69e-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c69e-119">EXAMPLES</span></span>

### <span data-ttu-id="8c69e-120">Пример 1: создание логики приложения с помощью путей к файлам определения и параметров</span><span class="sxs-lookup"><span data-stu-id="8c69e-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="8c69e-121">Эта команда создает логическое приложение в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="8c69e-122">Логическое приложение включает определение и параметры, указанные путями файлов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="8c69e-123">Пример 2: создание приложения логики с помощью объектов определения и параметров</span><span class="sxs-lookup"><span data-stu-id="8c69e-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="8c69e-124">Эта команда создает логическое приложение в указанной группе ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="8c69e-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="8c69e-125">Пример 3: создание логики приложения с помощью конвейера для указания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8c69e-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="8c69e-126">Эта команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c69e-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="8c69e-127">Команда передает эту группу ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8c69e-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8c69e-128">Текущий командлет создает логическое приложение в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="8c69e-129">Логическое приложение включает определение и параметры, указанные путями файлов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="8c69e-130">Пример 4: создание приложения логики на основе существующего приложения логики</span><span class="sxs-lookup"><span data-stu-id="8c69e-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="8c69e-131">Первая команда получает логическое приложение с именем LogicApp03 с помощью командлета Get-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="8c69e-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="8c69e-132">Команда хранит логическое приложение в переменной $Workflow.</span><span class="sxs-lookup"><span data-stu-id="8c69e-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="8c69e-133">Вторая команда создает новое логическое приложение, которое использует определение и параметры приложения логики, которое хранится в $Workflow.</span><span class="sxs-lookup"><span data-stu-id="8c69e-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="8c69e-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c69e-134">PARAMETERS</span></span>

### <span data-ttu-id="8c69e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c69e-135">-DefaultProfile</span></span>
<span data-ttu-id="8c69e-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c69e-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-137">-Определение</span><span class="sxs-lookup"><span data-stu-id="8c69e-137">-Definition</span></span>
<span data-ttu-id="8c69e-138">Указывает определение приложения логики в виде объекта или строки в формате JavaScript Object Notataion (JSON).</span><span class="sxs-lookup"><span data-stu-id="8c69e-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="8c69e-139">-DefinitionFilePath</span></span>
<span data-ttu-id="8c69e-140">Указывает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8c69e-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="8c69e-141">-IntegrationAccountId</span></span>
<span data-ttu-id="8c69e-142">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8c69e-142">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-143">-Location</span><span class="sxs-lookup"><span data-stu-id="8c69e-143">-Location</span></span>
<span data-ttu-id="8c69e-144">Указывает расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8c69e-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="8c69e-145">Введите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="8c69e-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="8c69e-146">Вы можете поместить логику приложения в любое место.</span><span class="sxs-lookup"><span data-stu-id="8c69e-146">You can place a logic app in any location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c69e-147">-Name</span></span>
<span data-ttu-id="8c69e-148">Задает имя для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8c69e-148">Specifies the name for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="8c69e-149">-ParameterFilePath</span></span>
<span data-ttu-id="8c69e-150">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="8c69e-150">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="8c69e-151">-Parameters</span></span>
<span data-ttu-id="8c69e-152">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8c69e-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="8c69e-153">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="8c69e-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c69e-154">-ResourceGroupName</span></span>
<span data-ttu-id="8c69e-155">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c69e-155">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-156">-State</span><span class="sxs-lookup"><span data-stu-id="8c69e-156">-State</span></span>
<span data-ttu-id="8c69e-157">Указывает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8c69e-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="8c69e-158">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="8c69e-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c69e-159">-Confirm</span></span>
<span data-ttu-id="8c69e-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c69e-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c69e-161">-WhatIf</span></span>
<span data-ttu-id="8c69e-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c69e-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c69e-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c69e-163">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c69e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c69e-164">CommonParameters</span></span>
<span data-ttu-id="8c69e-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c69e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c69e-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c69e-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c69e-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c69e-167">INPUTS</span></span>

### <span data-ttu-id="8c69e-168">Ничего</span><span class="sxs-lookup"><span data-stu-id="8c69e-168">None</span></span>

## <span data-ttu-id="8c69e-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c69e-169">OUTPUTS</span></span>

### <span data-ttu-id="8c69e-170">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="8c69e-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="8c69e-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c69e-171">NOTES</span></span>

## <span data-ttu-id="8c69e-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c69e-172">RELATED LINKS</span></span>

[<span data-ttu-id="8c69e-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c69e-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="8c69e-174">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c69e-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="8c69e-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c69e-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="8c69e-176">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c69e-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


