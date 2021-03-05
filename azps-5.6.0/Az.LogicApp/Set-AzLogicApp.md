---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: fcd2a09d9e335265d4e66a0c2ccde654f7122dcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003976"
---
# <span data-ttu-id="fe0dc-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe0dc-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="fe0dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0dc-103">Изменяет приложение логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="fe0dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe0dc-104">SYNTAX</span></span>

### <span data-ttu-id="fe0dc-105">Потребление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe0dc-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe0dc-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="fe0dc-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe0dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe0dc-107">DESCRIPTION</span></span>
<span data-ttu-id="fe0dc-108">**Cmdlet Set-AzLogicApp** изменяет приложение логики с помощью функции "Приложения логики".</span><span class="sxs-lookup"><span data-stu-id="fe0dc-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="fe0dc-109">Приложение логики — это набор действий или триггеров, определенных в определении приложения Logic.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="fe0dc-110">Этот cmdlet возвращает объект **рабочего** процесса.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="fe0dc-111">Вы можете изменить приложение логики, указав имя, расположение, определение приложения Logic, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="fe0dc-112">Определение и параметры приложения Logic форматированы в нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="fe0dc-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="fe0dc-113">Приложение логики можно использовать в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="fe0dc-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fe0dc-115">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fe0dc-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fe0dc-117">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="fe0dc-118">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="fe0dc-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe0dc-119">EXAMPLES</span></span>

### <span data-ttu-id="fe0dc-120">Пример 1. Изменение приложения логики</span><span class="sxs-lookup"><span data-stu-id="fe0dc-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="fe0dc-121">Эта команда изменяет приложение логики.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="fe0dc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe0dc-122">PARAMETERS</span></span>

### <span data-ttu-id="fe0dc-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe0dc-123">-AppServicePlan</span></span>
<span data-ttu-id="fe0dc-124">Название плана.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="fe0dc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0dc-125">-DefaultProfile</span></span>
<span data-ttu-id="fe0dc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe0dc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe0dc-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="fe0dc-127">-Definition</span></span>
<span data-ttu-id="fe0dc-128">Определение приложения логики в качестве объекта или строки в формате нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="fe0dc-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="fe0dc-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="fe0dc-129">-DefinitionFilePath</span></span>
<span data-ttu-id="fe0dc-130">Определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="fe0dc-131">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0dc-131">-Force</span></span>
<span data-ttu-id="fe0dc-132">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe0dc-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="fe0dc-133">-IntegrationAccountId</span></span>
<span data-ttu-id="fe0dc-134">Определяет ИД учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="fe0dc-135">-Name</span><span class="sxs-lookup"><span data-stu-id="fe0dc-135">-Name</span></span>
<span data-ttu-id="fe0dc-136">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="fe0dc-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="fe0dc-137">-ParameterFilePath</span></span>
<span data-ttu-id="fe0dc-138">Путь к файлу параметров в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="fe0dc-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="fe0dc-139">-Parameters</span></span>
<span data-ttu-id="fe0dc-140">Указывает объект коллекции параметров для приложения Logic.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="fe0dc-141">Укажите hash table, Dictionary \<string\> или Dictionary \<string, WorkflowParameter\> (Словарь).</span><span class="sxs-lookup"><span data-stu-id="fe0dc-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="fe0dc-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0dc-142">-ResourceGroupName</span></span>
<span data-ttu-id="fe0dc-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fe0dc-144">-State</span><span class="sxs-lookup"><span data-stu-id="fe0dc-144">-State</span></span>
<span data-ttu-id="fe0dc-145">Определяет состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="fe0dc-146">Допустимые значения этого параметра: Enabled (Включено) и Disabled (Отключено).</span><span class="sxs-lookup"><span data-stu-id="fe0dc-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="fe0dc-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="fe0dc-147">-UseConsumptionModel</span></span>
<span data-ttu-id="fe0dc-148">Указывает на то, что при выставлении счета за использование логики используется модель на основе потребления.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="fe0dc-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe0dc-149">-Confirm</span></span>
<span data-ttu-id="fe0dc-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0dc-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0dc-151">-WhatIf</span></span>
<span data-ttu-id="fe0dc-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0dc-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0dc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0dc-154">CommonParameters</span></span>
<span data-ttu-id="fe0dc-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0dc-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0dc-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0dc-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe0dc-157">INPUTS</span></span>

### <span data-ttu-id="fe0dc-158">System.String</span><span class="sxs-lookup"><span data-stu-id="fe0dc-158">System.String</span></span>

## <span data-ttu-id="fe0dc-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe0dc-159">OUTPUTS</span></span>

### <span data-ttu-id="fe0dc-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="fe0dc-160">System.Object</span></span>

## <span data-ttu-id="fe0dc-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe0dc-161">NOTES</span></span>

## <span data-ttu-id="fe0dc-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe0dc-162">RELATED LINKS</span></span>

[<span data-ttu-id="fe0dc-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe0dc-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="fe0dc-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe0dc-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="fe0dc-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe0dc-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="fe0dc-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe0dc-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


