---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243546"
---
# <span data-ttu-id="3fdbb-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="3fdbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fdbb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdbb-103">Проверка определения логического приложения.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="3fdbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fdbb-104">SYNTAX</span></span>

### <span data-ttu-id="3fdbb-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fdbb-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fdbb-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fdbb-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fdbb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdbb-107">DESCRIPTION</span></span>
<span data-ttu-id="3fdbb-108">Командлет **Test-AzLogicApp** проверяет определение приложения логики в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="3fdbb-109">Укажите имя логики приложения, имя группы ресурсов, расположение, состояние, идентификатор учетной записи для интеграции или параметры.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="3fdbb-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3fdbb-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3fdbb-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3fdbb-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3fdbb-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fdbb-114">EXAMPLES</span></span>

### <span data-ttu-id="3fdbb-115">Пример 1: проверка логического приложения с помощью путей к файлам</span><span class="sxs-lookup"><span data-stu-id="3fdbb-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="3fdbb-116">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="3fdbb-117">Команда задает пути к файлу определения и параметров.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="3fdbb-118">Пример 2: проверка логического приложения с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="3fdbb-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="3fdbb-119">Эта команда проверяет логическое приложение с именем LogicApp01 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="3fdbb-120">Команда задает определение и объекты параметров.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="3fdbb-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3fdbb-121">Example 3</span></span>

<span data-ttu-id="3fdbb-122">Проверка определения логического приложения.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-122">Validates a logic app definition.</span></span> <span data-ttu-id="3fdbb-123">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="3fdbb-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="3fdbb-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fdbb-124">PARAMETERS</span></span>

### <span data-ttu-id="3fdbb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdbb-125">-DefaultProfile</span></span>
<span data-ttu-id="3fdbb-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3fdbb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fdbb-127">-Определение</span><span class="sxs-lookup"><span data-stu-id="3fdbb-127">-Definition</span></span>
<span data-ttu-id="3fdbb-128">Указывает определение приложения логики в виде объекта или строки в формате JSON (объектной нотации).</span><span class="sxs-lookup"><span data-stu-id="3fdbb-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="3fdbb-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="3fdbb-129">-DefinitionFilePath</span></span>
<span data-ttu-id="3fdbb-130">Задает определение приложения логики в качестве пути к файлу определения в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="3fdbb-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="3fdbb-131">-IntegrationAccountId</span></span>
<span data-ttu-id="3fdbb-132">Указывает идентификатор учетной записи интеграции для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="3fdbb-133">-Location</span><span class="sxs-lookup"><span data-stu-id="3fdbb-133">-Location</span></span>
<span data-ttu-id="3fdbb-134">Указывает расположение приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="3fdbb-135">Введите расположение центра обработки данных Azure, например Западная часть США или Юго-Восток Азии.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="3fdbb-136">Вы можете поместить логику приложения в любое место.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="3fdbb-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3fdbb-137">-Name</span></span>
<span data-ttu-id="3fdbb-138">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="3fdbb-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="3fdbb-139">-ParameterFilePath</span></span>
<span data-ttu-id="3fdbb-140">Задает путь к файлу форматированного параметра JSON.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="3fdbb-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="3fdbb-141">-Parameters</span></span>
<span data-ttu-id="3fdbb-142">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="3fdbb-143">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="3fdbb-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="3fdbb-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdbb-144">-ResourceGroupName</span></span>
<span data-ttu-id="3fdbb-145">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3fdbb-146">-State</span><span class="sxs-lookup"><span data-stu-id="3fdbb-146">-State</span></span>
<span data-ttu-id="3fdbb-147">Задает состояние приложения логики.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="3fdbb-148">Допустимые значения этого параметра: включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="3fdbb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdbb-149">CommonParameters</span></span>
<span data-ttu-id="3fdbb-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fdbb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdbb-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdbb-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdbb-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fdbb-152">INPUTS</span></span>

### <span data-ttu-id="3fdbb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3fdbb-153">System.String</span></span>

## <span data-ttu-id="3fdbb-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdbb-154">OUTPUTS</span></span>

### <span data-ttu-id="3fdbb-155">System. void</span><span class="sxs-lookup"><span data-stu-id="3fdbb-155">System.Void</span></span>

## <span data-ttu-id="3fdbb-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fdbb-156">NOTES</span></span>

## <span data-ttu-id="3fdbb-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fdbb-157">RELATED LINKS</span></span>

[<span data-ttu-id="3fdbb-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="3fdbb-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="3fdbb-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="3fdbb-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="3fdbb-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3fdbb-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


