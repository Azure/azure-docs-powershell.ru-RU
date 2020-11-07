---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: aa1a4148da7958c587363bcfdc11d53ae7a25b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720463"
---
# <span data-ttu-id="74943-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="74943-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74943-102">SYNOPSIS</span></span>
<span data-ttu-id="74943-103">Проверка определения логического приложения.</span><span class="sxs-lookup"><span data-stu-id="74943-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="74943-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74943-104">SYNTAX</span></span>

### <span data-ttu-id="74943-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="74943-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74943-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="74943-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74943-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74943-107">DESCRIPTION</span></span>
<span data-ttu-id="74943-108">Командлет **Test-AzLogicApp** проверяет определение приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74943-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="74943-109">Укажите имя логики приложения, имя группы ресурсов, расположение, состояние, идентификатор учетной записи для интеграции или параметры.</span><span class="sxs-lookup"><span data-stu-id="74943-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="74943-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="74943-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="74943-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="74943-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="74943-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="74943-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="74943-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="74943-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="74943-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74943-114">EXAMPLES</span></span>

### <span data-ttu-id="74943-115">Пример 1: проверка логического приложения с помощью путей к файлам</span><span class="sxs-lookup"><span data-stu-id="74943-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="74943-116">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74943-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="74943-117">Команда задает пути к файлу определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="74943-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="74943-118">Пример 2: проверка логического приложения с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="74943-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="74943-119">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74943-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="74943-120">Команда задает определение и объекты параметров.</span><span class="sxs-lookup"><span data-stu-id="74943-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="74943-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74943-121">PARAMETERS</span></span>

### <span data-ttu-id="74943-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74943-122">-DefaultProfile</span></span>
<span data-ttu-id="74943-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="74943-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74943-124">-Определение</span><span class="sxs-lookup"><span data-stu-id="74943-124">-Definition</span></span>
<span data-ttu-id="74943-125">Указывает определение приложения логики в виде объекта или строки в формате JSON (объектной нотации).</span><span class="sxs-lookup"><span data-stu-id="74943-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74943-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="74943-126">-DefinitionFilePath</span></span>
<span data-ttu-id="74943-127">Задает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="74943-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74943-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="74943-128">-IntegrationAccountId</span></span>
<span data-ttu-id="74943-129">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="74943-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="74943-130">-Location</span><span class="sxs-lookup"><span data-stu-id="74943-130">-Location</span></span>
<span data-ttu-id="74943-131">Указывает расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="74943-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="74943-132">Введите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="74943-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="74943-133">Вы можете поместить логику приложения в любое место.</span><span class="sxs-lookup"><span data-stu-id="74943-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="74943-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74943-134">-Name</span></span>
<span data-ttu-id="74943-135">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="74943-135">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74943-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="74943-136">-ParameterFilePath</span></span>
<span data-ttu-id="74943-137">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="74943-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="74943-138">-Parameters</span><span class="sxs-lookup"><span data-stu-id="74943-138">-Parameters</span></span>
<span data-ttu-id="74943-139">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="74943-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="74943-140">Укажите хэш-таблицу, \< строку словаря \> или строку словаря \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="74943-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="74943-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74943-141">-ResourceGroupName</span></span>
<span data-ttu-id="74943-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74943-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="74943-143">-State</span><span class="sxs-lookup"><span data-stu-id="74943-143">-State</span></span>
<span data-ttu-id="74943-144">Задает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="74943-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="74943-145">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="74943-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="74943-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74943-146">CommonParameters</span></span>
<span data-ttu-id="74943-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74943-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74943-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74943-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74943-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74943-149">INPUTS</span></span>

### <span data-ttu-id="74943-150">System. String</span><span class="sxs-lookup"><span data-stu-id="74943-150">System.String</span></span>

## <span data-ttu-id="74943-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74943-151">OUTPUTS</span></span>

### <span data-ttu-id="74943-152">System. void</span><span class="sxs-lookup"><span data-stu-id="74943-152">System.Void</span></span>

## <span data-ttu-id="74943-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="74943-153">NOTES</span></span>

## <span data-ttu-id="74943-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74943-154">RELATED LINKS</span></span>

[<span data-ttu-id="74943-155">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-155">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="74943-156">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-156">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="74943-157">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-157">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="74943-158">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-158">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="74943-159">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="74943-159">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


