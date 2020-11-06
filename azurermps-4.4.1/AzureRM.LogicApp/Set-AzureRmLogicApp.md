---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570379"
---
# <span data-ttu-id="8a8b7-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a8b7-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="8a8b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8b7-103">Изменение приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a8b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a8b7-104">SYNTAX</span></span>

### <span data-ttu-id="8a8b7-105">Потребление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a8b7-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a8b7-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="8a8b7-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a8b7-107">DESCRIPTION</span></span>
<span data-ttu-id="8a8b7-108">Командлет **Set-AzureRmLogicApp** изменяет приложение логики с помощью функции приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8a8b7-109">Логическое приложение — это коллекция действий или триггеров, определенных в определении логического приложения.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="8a8b7-110">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="8a8b7-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="8a8b7-111">Вы можете изменить логическое приложение, указав имя, расположение, определение приложения логики, группу ресурсов и план.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="8a8b7-112">Логическое определение и параметры приложения форматируются в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="8a8b7-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="8a8b7-113">Вы можете использовать логическое приложение в качестве шаблона для определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="8a8b7-114">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8a8b7-115">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8a8b7-116">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8a8b7-117">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="8a8b7-118">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="8a8b7-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a8b7-119">EXAMPLES</span></span>

### <span data-ttu-id="8a8b7-120">Пример 1: изменение логики приложения</span><span class="sxs-lookup"><span data-stu-id="8a8b7-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="8a8b7-121">Эта команда изменяет логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="8a8b7-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a8b7-122">PARAMETERS</span></span>

### <span data-ttu-id="8a8b7-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8a8b7-123">-AppServicePlan</span></span>
<span data-ttu-id="8a8b7-124">Указывает имя плана.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="8a8b7-125">-Определение</span><span class="sxs-lookup"><span data-stu-id="8a8b7-125">-Definition</span></span>
<span data-ttu-id="8a8b7-126">Указывает определение приложения логики в виде объекта или строки в формате JSON (объектной нотации).</span><span class="sxs-lookup"><span data-stu-id="8a8b7-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="8a8b7-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="8a8b7-127">-DefinitionFilePath</span></span>
<span data-ttu-id="8a8b7-128">Указывает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="8a8b7-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8a8b7-129">-Force</span></span>
<span data-ttu-id="8a8b7-130">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a8b7-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="8a8b7-131">-IntegrationAccountId</span></span>
<span data-ttu-id="8a8b7-132">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="8a8b7-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a8b7-133">-Name</span></span>
<span data-ttu-id="8a8b7-134">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="8a8b7-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="8a8b7-135">-ParameterFilePath</span></span>
<span data-ttu-id="8a8b7-136">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="8a8b7-137">-Parameters</span><span class="sxs-lookup"><span data-stu-id="8a8b7-137">-Parameters</span></span>
<span data-ttu-id="8a8b7-138">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="8a8b7-139">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="8a8b7-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="8a8b7-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a8b7-140">-ResourceGroupName</span></span>
<span data-ttu-id="8a8b7-141">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a8b7-142">-State</span><span class="sxs-lookup"><span data-stu-id="8a8b7-142">-State</span></span>
<span data-ttu-id="8a8b7-143">Указывает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="8a8b7-144">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="8a8b7-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="8a8b7-145">-UseConsumptionModel</span></span>
<span data-ttu-id="8a8b7-146">Указывает на то, что для логики выставления счетов в приложении используется модель на основе потребления.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-146">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="8a8b7-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a8b7-147">-Confirm</span></span>
<span data-ttu-id="8a8b7-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8b7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8b7-149">-WhatIf</span></span>
<span data-ttu-id="8a8b7-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a8b7-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a8b7-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8b7-152">-DefaultProfile</span></span>
<span data-ttu-id="8a8b7-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8b7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8b7-154">CommonParameters</span></span>
<span data-ttu-id="8a8b7-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a8b7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8b7-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8b7-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8b7-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a8b7-157">INPUTS</span></span>

## <span data-ttu-id="8a8b7-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a8b7-158">OUTPUTS</span></span>

### <span data-ttu-id="8a8b7-159">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="8a8b7-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="8a8b7-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a8b7-160">NOTES</span></span>

## <span data-ttu-id="8a8b7-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a8b7-161">RELATED LINKS</span></span>

[<span data-ttu-id="8a8b7-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a8b7-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="8a8b7-163">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a8b7-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="8a8b7-164">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a8b7-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="8a8b7-165">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8a8b7-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


