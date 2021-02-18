---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214412"
---
# <span data-ttu-id="a521b-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="a521b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a521b-102">SYNOPSIS</span></span>
<span data-ttu-id="a521b-103">Проверяет определение приложения по логике.</span><span class="sxs-lookup"><span data-stu-id="a521b-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="a521b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a521b-104">SYNTAX</span></span>

### <span data-ttu-id="a521b-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a521b-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a521b-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a521b-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a521b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a521b-107">DESCRIPTION</span></span>
<span data-ttu-id="a521b-108">С **помощью cmdlet Test-AzLogicApp** можно проверить определение приложения по логике в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a521b-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="a521b-109">Укажите имя приложения логики, имя группы ресурсов, расположение, состояние, ИД учетной записи интеграции или параметры.</span><span class="sxs-lookup"><span data-stu-id="a521b-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="a521b-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a521b-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a521b-111">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="a521b-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a521b-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="a521b-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a521b-113">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="a521b-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a521b-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a521b-114">EXAMPLES</span></span>

### <span data-ttu-id="a521b-115">Пример 1. Проверка приложения логики с помощью путей к файлам</span><span class="sxs-lookup"><span data-stu-id="a521b-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="a521b-116">Эта команда проверяет приложение логики с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a521b-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="a521b-117">Команда определяет пути определения и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="a521b-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="a521b-118">Пример 2. Проверка приложения логики с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="a521b-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="a521b-119">Эта команда проверяет приложение логики с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a521b-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="a521b-120">Команда определяет объекты определения и параметра.</span><span class="sxs-lookup"><span data-stu-id="a521b-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="a521b-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a521b-121">Example 3</span></span>

<span data-ttu-id="a521b-122">Проверяет определение приложения по логике.</span><span class="sxs-lookup"><span data-stu-id="a521b-122">Validates a logic app definition.</span></span> <span data-ttu-id="a521b-123">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a521b-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="a521b-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a521b-124">PARAMETERS</span></span>

### <span data-ttu-id="a521b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a521b-125">-DefaultProfile</span></span>
<span data-ttu-id="a521b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a521b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a521b-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="a521b-127">-Definition</span></span>
<span data-ttu-id="a521b-128">Определение приложения логики в качестве объекта или строки в формате нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="a521b-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a521b-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="a521b-129">-DefinitionFilePath</span></span>
<span data-ttu-id="a521b-130">Определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a521b-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="a521b-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="a521b-131">-IntegrationAccountId</span></span>
<span data-ttu-id="a521b-132">Определяет ИД учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a521b-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="a521b-133">-Location</span><span class="sxs-lookup"><span data-stu-id="a521b-133">-Location</span></span>
<span data-ttu-id="a521b-134">Определяет расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a521b-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="a521b-135">Введите расположение центра обработки данных Azure, например "Западная США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="a521b-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="a521b-136">Приложение логики можно разместить в любом месте.</span><span class="sxs-lookup"><span data-stu-id="a521b-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="a521b-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a521b-137">-Name</span></span>
<span data-ttu-id="a521b-138">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a521b-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="a521b-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="a521b-139">-ParameterFilePath</span></span>
<span data-ttu-id="a521b-140">Путь к файлу параметров в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a521b-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="a521b-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="a521b-141">-Parameters</span></span>
<span data-ttu-id="a521b-142">Определяет объект коллекции параметров приложения logic.</span><span class="sxs-lookup"><span data-stu-id="a521b-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a521b-143">Укажите hash table, Dictionary \<string\> или Dictionary \<string, WorkflowParameter\> (Словарь).</span><span class="sxs-lookup"><span data-stu-id="a521b-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="a521b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a521b-144">-ResourceGroupName</span></span>
<span data-ttu-id="a521b-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a521b-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a521b-146">-State</span><span class="sxs-lookup"><span data-stu-id="a521b-146">-State</span></span>
<span data-ttu-id="a521b-147">Указывает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="a521b-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="a521b-148">Допустимые значения этого параметра: Enabled (Включено) и Disabled (Отключено).</span><span class="sxs-lookup"><span data-stu-id="a521b-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="a521b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a521b-149">CommonParameters</span></span>
<span data-ttu-id="a521b-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a521b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a521b-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a521b-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a521b-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a521b-152">INPUTS</span></span>

### <span data-ttu-id="a521b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="a521b-153">System.String</span></span>

## <span data-ttu-id="a521b-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a521b-154">OUTPUTS</span></span>

### <span data-ttu-id="a521b-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="a521b-155">System.Void</span></span>

## <span data-ttu-id="a521b-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a521b-156">NOTES</span></span>

## <span data-ttu-id="a521b-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a521b-157">RELATED LINKS</span></span>

[<span data-ttu-id="a521b-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="a521b-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="a521b-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="a521b-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="a521b-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a521b-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


