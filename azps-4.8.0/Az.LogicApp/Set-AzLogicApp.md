---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079561"
---
# <span data-ttu-id="8ad83-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8ad83-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="8ad83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ad83-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad83-103">Изменение приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ad83-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="8ad83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ad83-104">SYNTAX</span></span>

### <span data-ttu-id="8ad83-105">Потребление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ad83-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad83-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="8ad83-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ad83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ad83-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad83-108">Командлет **Set-AzLogicApp** изменяет приложение логики с помощью функции приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8ad83-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8ad83-109">Логическое приложение — это коллекция действий или триггеров, определенных в определении логического приложения.</span><span class="sxs-lookup"><span data-stu-id="8ad83-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="8ad83-110">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="8ad83-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="8ad83-111">Вы можете изменить логическое приложение, указав имя, расположение, определение приложения логики, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="8ad83-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="8ad83-112">Логическое определение и параметры приложения форматируются в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="8ad83-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="8ad83-113">Вы можете использовать логическое приложение в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="8ad83-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="8ad83-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="8ad83-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8ad83-115">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="8ad83-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8ad83-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="8ad83-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8ad83-117">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="8ad83-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="8ad83-118">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad83-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="8ad83-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ad83-119">EXAMPLES</span></span>

### <span data-ttu-id="8ad83-120">Пример 1: изменение логики приложения</span><span class="sxs-lookup"><span data-stu-id="8ad83-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="8ad83-121">Эта команда изменяет логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="8ad83-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="8ad83-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ad83-122">PARAMETERS</span></span>

### <span data-ttu-id="8ad83-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ad83-123">-AppServicePlan</span></span>
<span data-ttu-id="8ad83-124">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="8ad83-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad83-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad83-125">-DefaultProfile</span></span>
<span data-ttu-id="8ad83-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ad83-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ad83-127">-Определение</span><span class="sxs-lookup"><span data-stu-id="8ad83-127">-Definition</span></span>
<span data-ttu-id="8ad83-128">Указывает определение приложения логики в виде объекта или строки в формате JSON (объектной нотации).</span><span class="sxs-lookup"><span data-stu-id="8ad83-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="8ad83-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="8ad83-129">-DefinitionFilePath</span></span>
<span data-ttu-id="8ad83-130">Указывает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8ad83-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="8ad83-131">-Force</span><span class="sxs-lookup"><span data-stu-id="8ad83-131">-Force</span></span>
<span data-ttu-id="8ad83-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ad83-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ad83-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="8ad83-133">-IntegrationAccountId</span></span>
<span data-ttu-id="8ad83-134">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8ad83-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="8ad83-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ad83-135">-Name</span></span>
<span data-ttu-id="8ad83-136">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8ad83-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="8ad83-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="8ad83-137">-ParameterFilePath</span></span>
<span data-ttu-id="8ad83-138">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="8ad83-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="8ad83-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="8ad83-139">-Parameters</span></span>
<span data-ttu-id="8ad83-140">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8ad83-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="8ad83-141">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="8ad83-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="8ad83-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad83-142">-ResourceGroupName</span></span>
<span data-ttu-id="8ad83-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ad83-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8ad83-144">-State</span><span class="sxs-lookup"><span data-stu-id="8ad83-144">-State</span></span>
<span data-ttu-id="8ad83-145">Указывает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8ad83-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="8ad83-146">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="8ad83-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="8ad83-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="8ad83-147">-UseConsumptionModel</span></span>
<span data-ttu-id="8ad83-148">Указывает на то, что для логики выставления счетов в приложении используется модель на основе потребления.</span><span class="sxs-lookup"><span data-stu-id="8ad83-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad83-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ad83-149">-Confirm</span></span>
<span data-ttu-id="8ad83-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ad83-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad83-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad83-151">-WhatIf</span></span>
<span data-ttu-id="8ad83-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ad83-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ad83-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ad83-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad83-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad83-154">CommonParameters</span></span>
<span data-ttu-id="8ad83-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ad83-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad83-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad83-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad83-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ad83-157">INPUTS</span></span>

### <span data-ttu-id="8ad83-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8ad83-158">System.String</span></span>

## <span data-ttu-id="8ad83-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ad83-159">OUTPUTS</span></span>

### <span data-ttu-id="8ad83-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ad83-160">System.Object</span></span>

## <span data-ttu-id="8ad83-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ad83-161">NOTES</span></span>

## <span data-ttu-id="8ad83-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ad83-162">RELATED LINKS</span></span>

[<span data-ttu-id="8ad83-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8ad83-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="8ad83-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8ad83-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="8ad83-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8ad83-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="8ad83-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8ad83-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


